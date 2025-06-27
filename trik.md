setting konek ssh otomatis
------------------------------
- **server (contoh termux)**
  - install openssh
  - cari ip termux kita(ifonfig)
- **client (contoh windows menggunakan powershell)**
    - `ssh-keygen -t rsa` ( membuat kunci ssh,nanti akan mucul beberapa pertanyaan silakan enter enter saja)
    - `Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub" | ssh username@hostname "cat >> ~/.ssh/authorized_keys"`
    *( ganti username dan hostname dengan user dan alamat ip ssh server.perintah di atas akan menampilkan isi id_rsa.pub kita,kemudian hasil outputnya akan di jadi kan input untuk cat.yang di mana perintah cat ini akan di eksekusi oleh server (bukan client) untuk menambahkan rsa yang di ijin kan ke dalam file authorized_key)*
    - `ssh username@host -p port`*(konek ke server seperti biasa)*
    - `ssh-copy-id username@hostname` (jika di linux gunakan perintah ini untuk menyalin rsa kita ke authorized_rsa ke server,karena di windows tidak ada perintah ini.

