## 2.1

server:
    ![ss1](images/ss1.png)

client 1:
    ![ss2](images/ss2.png)

client 2:
    ![ss3](images/ss3.png)

client 3:
    ![ss4](images/ss4.png)

Pada server dapat dilihat setiap kali ada client yang jalan dan connect ke server. Setiap kali client mengirimkan pesan akan terlihat di server ip client yang mengirimkan pesan dan pesannya. Selain itu server juga akan mengirimkan kembali pesan yang dikirimkan oleh client tersebut ke semua client yang connect ke server.


## 2.2

Pada client menggunakan websocket, tapi pada server menggunakan TCP. TCP sendiri adalah dasar dari websocket.

## 2.3

server:
    ![ss5](images/ss5.png)

client 1:
    ![ss6](images/ss6.png)

client 2:
    ![ss7](images/ss7.png)

Pada server.rs dimodifikasi bagian untuk mengembalikan pesan kepada client menjadi : 
    let message = format!("{addr}: {text}");
    bcast_tx.send(message.into())?;
Yang sebelumnya hanya isi pesan saja yaitu text, sekarang ditambahkan dengan ip client yaitu addr. 
