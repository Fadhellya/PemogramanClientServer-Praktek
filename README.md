# PemogramanClientServer-Praktek
## Langkah - Langkah Membuat Latihan 1
### Langkah 1 : 
####  Buat proyek web menggunakan link berikut [start.spring.io](https://start.spring.io/)  kemudian pilih Spring web dan kemudian bahasa java dan sesuaikan versinya dengan device (disini saya menggunakan jdk 17  kemudian isi artifactnya(saya menggunakan latihan1-service) kemudian spring bootversinya pakai yang versi 2.6.11(yang saya pakai) dan untuk grubnya isi dengan com.fadhel kemudian download dan extrack dari zip menjadi file kemudian import ke dalam apache netbean 
### Langkah 2 :
#### Kemudian cari proyek yang bernama LatihanServiceApplication dibawah package com.fadhel.latihan.service kemudian pada proyek itu masukkan code berikut :
```java
package com.fadhel.latihan.service;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
@RestController
public class LatihanServiceApplication {

    public static void main(String[] args) {
        SpringApplication.run(LatihanServiceApplication.class, args);
    }

    @GetMapping("/hello")
    public String hello(@RequestParam(value = "name", defaultValue = "World") String name) {
        return String.format("Hello %s!", name);
    }
}
```
### Langkah 3 :
##### Kemudian cari proyek aplication.properties yang berada di Other Source >> src/main/resources >> <default package> >> aplication.properties kemudian masukkan code berikut :
```java
server.port=8010
```
### Langkah 4 :
##### setelah itu coba di buka link berikut [http://localhost:8010/hello](http://localhost:8010/hello)
##### dan akan muncul Output seperti berikut
![1](https://user-images.githubusercontent.com/113502315/192090587-5687bb5e-b361-40e5-9d8f-61e8d3dab2a5.png)
