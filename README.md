# Dockerfile dan Contoh Penggunaannya

== Pengertian Dockerfile

Dockerfile merupakan skrip yang terdiri dari serangkaian perintah, instruksi yang akan dieksekusi secara otomatisasi dan berurutan untuk membangun sebuah image.

== Contoh penggunaan dockerfile untuk membuat aplikasi node js. 

1. Langkah pertama buat folder dengan nama dockerummah atau bisa bebas. 
2. Kemudian ke direktori aplikasi yang baru saja dibuat lalu buat file dengan nama package.json(terlampir)
3. Kemudian membuat file index.js(terlampir)
4. Membuat file document dockerfile lalu membuat baris instruksi dasar yang tersedia di Dockerfile.Berikut instruksi dasarnya :

* FROM node:6.11.2-alpine

FROM adalah instruksi tahap awal ketika menginisialisasi project baru dengan docker.

* WORKDIR /app

WORKDIR adalah instruksi untuk mendefinisikan direktori kerja atau area kerja yang nantinya seluruh instruksi yang ada di Dockerfile akan di jalankan di area kerja yang kita setup di WORKDIR.

* COPY package.json /app

COPY adalah instruksi untuk meng copy file baru atau direktori dari <src> dan menambahkannya ke filesystem container path <dest>.

* RUN npm install

RUN adalah instruksi untuk mengekesekusi perintah, misalnya seperti perintah install nodejs dan lain sebagainya.

* COPY . /app

* EXPOSE 8080

EXPOSE adalah perintah untuk me listen nework port .

* CMD [ "npm", "start" ]

CMD adalah instruksi untuk mengeksekusi container. 

5. Selanjutnya membuat container image dengan menuju ke direktori dimana menyimpan dockerfile lalu untuk jalankan perintah "docker build -t <Rohmatul1>/dockerummah".

6. Lalu jalankan perintah docker images untuk melihat container yang telah tersedia.

7. Selanjutnya untuk menjalankan aplikasi nodejs dengan menjalankan perintah "docker run -p 8080:8080 <Rohmatul1>/dockerummah". Hasilnya adalah untuk menampilkan "Hello World".

==Sumber : ==

https://medium.com/tutorjs/setup-aplikasi-nodejs-menggunakan-docker-aba52781869b