# Reflection

## Commit 1 Reflection 'handle_connection'

1. TcpStream
Method 'handle_connection' mempunyai TcpStream dimana ini digunakan untuk membaca data yang dikirim oleh user melalui koneksi TCP.

2. BufReader
BufReader adalah wrapper untuk stream yang membuat membaca data yang dikirim dari stream secara lebih efisien.

3. http_request
http_request, 'lines' adalah membaca data dari stream. 'map(|line| line.unwrap()) digunakan untuk membaca data lalu mengubah menjadi string. 'take_while()' digunakan agar program mengambil baris-baris hingga menemukan baris kosong. 'collect' mengumpulkan semua baris ke sebuah vektor. 

## Commit 2 Reflection 'handle_connection'

1. status_line
Beris ini mendifinikasikan status HTTP yang dikirim kepada klien. HTTP/1.1 200 OK menunjukkan bahwa permintaan klien berhasil di proses.

2. contents
Baris ini membaca isi dari file 'hello.html', dan fs::read_to_string membaca isi file sebagai string.

3. length
Baris ini menghitung besar(dalam byte) dari isi file 'hello.html'

4. response
Baris ini membuat respons HTTP lengkap dalam bentuk string. 

5. stream.write_all
Baris ini mengirim respon HTTP ke klien melalui stream.

![Commit 2 screen capture](/assets/images/commit2.png)

## Commit 3 Reflection 

1. request_line
Method sekarang akan memeriksa request line. Server akan memeriksa apakah request line yang diterima adalah HTTP 1.1 200 OK jika benar maka server akan menampilkan 'hello.html', dan jika tidak maka server akan menampilkan '404.html'

2. Pemisahan logic
Sebelumnya server memberikan halaman yang sama untuk semua request, sekarang server memberikan response sesuai dengan pilihan yang diberikan(if else). 

![Commit 3 screen capture](/assets/images/commit3.png)

## Commit 4 Reflection

1. Dampak pada '/sleep'
Ketika mengakses url dengan '/sleep' dapat terlihat bahwa browser membutuhkan waktu yang lebih lama agar websitenya loading, saat saya membuka websitenya pada window lain tanpa '/sleep' responsenya cukup lama karena harus menyelesaikan request pertama.

