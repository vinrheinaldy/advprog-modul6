# Reflection

## Commit 1 Reflection 'handle_connection'

1. TcpStream
Method 'handle_connection' mempunyai TcpStream dimana ini digunakan untuk membaca data yang dikirim oleh user melalui koneksi TCP.

2. BufReader
BufReader adalah wrapper untuk stream yang membuat membaca data yang dikirim dari stream secara lebih efisien.

3. http_request
http_request, 'lines' adalah membaca data dari stream. 'map(|line| line.unwrap()) digunakan untuk membaca data lalu mengubah menjadi string. 'take_while()' digunakan agar program mengambil baris-baris hingga menemukan baris kosong. 'collect' mengumpulkan semua baris ke sebuah vektor. 