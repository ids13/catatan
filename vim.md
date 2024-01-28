# Vim

## NORMAL MODE
- ### **Movement (Pemindahan)**
  - h, j, k, l: Gerak kursor ke kiri, bawah, atas, dan kanan.
  - w, e, b: Pindah ke awal kata berikutnya, akhir kata berikutnya, dan awal kata sebelumnya.
  - 0, ^, $: Pindah ke awal baris, awal non-whitespace karakter, dan akhir baris.
*(jika 0 akan ke awal baris meskipun ada sepasi akan berpindah ke awal baris,sedangkan ^ akan berpindah ke awal char yang bukan whitespace)*
- **Edit (Penyuntingan)**
  - i, I: Masuk mode penyuntingan sebelum dan di awal baris.
  - a, A: Masuk mode penyuntingan setelah dan di akhir baris.
  - o, O: Membuat baris baru di bawah atau di atas posisi kursor dan masuk mode penyuntingan.
  - x, X: Menghapus karakter di bawah (x) atau di sebelah kiri (X) kursor.
- **Search (Pencarian)**
  - /pattern: Mencari pola ke depan.
  - ?pattern: Mencari pola ke belakang.
  - n, N: Melanjutkan pencarian ke depan dan ke belakang.
- **Replace (Penggantian)**
  - :s/old/new/g: Mengganti semua kemunculan "old" dengan "new" pada baris saat ini.
  - :%s/old/new/g: Mengganti semua kemunculan "old" dengan "new" di seluruh file.
Lainnya
  - dd: Menghapus baris saat ini.
  - yy: Menyalin baris saat ini.
  - p, P: Menyisipkan (paste) teks setelah atau sebelum posisi kursor.
- **undo dan redo**
  - u untuk undo
  - ctrl + r untuk redo

## VISUAL MODE
- Tekan v untuk masuk ke mode visual karakter.
- Tekan V (huruf besar) untuk masuk ke mode visual baris.
- Tekan Ctrl + q untuk masuk ke mode visual blok.
d cut,y copy,p paste
