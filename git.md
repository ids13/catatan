# Pengaturan Akun Git
### Mengatur nama pengguna
    git config --global user.name "Nama Anda"
### Mengatur alamat email
    git config --global user.email "email@anda.com"

# Inisialisasi Repositori
### Buat repositori baru
    git init
### Clone repositori yang sudah ada dari remote repository
    git clone <url_repository>

# Menambahkan dan Merubah File
### Menambahkan file ke staging area
    git add nama_file
### Menambahkan semua perubahan ke staging area
    git add .
### Membuat commit dengan pesan
    git commit -m "Pesan commit disini"

# Melihat dan Mengecek Status
### Melihat status perubahan
    git status
### Melihat perbedaan antara working directory dan staging area
    git diff
### Melihat perbedaan antara staging area dan last commit
    git diff --staged

# Cabang (Branch)
### Membuat cabang baru
    git branch nama_cabang
### Pindah ke cabang tertentu
    git checkout nama_cabang
### Membuat dan pindah ke cabang baru dalam satu langkah
    git checkout -b nama_cabang

# Menggabungkan (Merge) Cabang
### Pindah ke branch tujuan
    git checkout branch_tujuan
### Melakukan merge branch yang akan digabung
    git merge branch_yang_ingin_digabung

# Remote Repository
### Menampilkan remote repository yang terhubung
    git remote -v
### Menambahkan remote repository
    git remote add nama_remote <url_repository>
### Mengambil perubahan dari remote repository
    git pull origin nama_cabang
### Mengirim perubahan ke remote repository
    git push origin nama_cabang

# Catatan Tambahan

- Perintah `git remote show nama_remote` menampilkan informasi terkait remote repository.
- Penggunaan `.gitignore` untuk mengabaikan file atau direktori dari tracking.
- **git log**
  - `git log` : melihat catatan log
  - `git log -p` : melihat perubahannya
  - `git log --graph` : pohon log
  - `git log --oneline` : melihat log lebih pendek (dalam satu baris)
  - `git log commithash` : melihat log bedasarkan no commit
  - `git log nama_file` : melihat log yang terjadi di file tertentu
  - `git lof --author='nama_author'` : melihat log yang di lakukan oleh author tertentu
- **git config**
  - `git config --list` : melihat daftar pengaturan 
  - `git config --global --list` : melihat daftar pengaturan yang di set secara global

- **git checkout**
  - digunakan untuk beralih branch atau commit dan mengubah working directory.
  - `git checkout nama-cabang/commit-hash`
- **git reset**
  - digunakan untuk mengubah keadaan branch dan indeks, dan dapat diatur untuk mempengaruhi working directory.
  - `git reset commit-hash`
    - `--soft`: Mengganti keadaan branch dan indeks, tetapi meninggalkan perubahan di working directory.
    - `--mixed` (default): Mengganti keadaan branch, mereset indeks, tetapi meninggalkan perubahan di working directory.
    - `--hard`: Mengganti keadaan branch, mereset indeks, dan menghapus perubahan di working directory.
- **git revert**
  - digunakan untuk membuat commit baru yang membatalkan perubahan dari commit tertentu, tanpa mengubah sejarah commit sebelumnya
  - `git revert commit-hash`
- **git fetch**
  - `git fetch` : Git fetch mengambil semua perubahan dari remote repository ke branch remote tracking lokal tanpa menggabungkannya ke dalam branch lokal atau membuat perubahan di working directory.
  - `git log HEAD..origin/nama-branch` : ini ntuk melihat perbedaan antara lokal branch dan remote branch,tanda .. di antara HEAD dan origin maksudnya oprator rentang yang di gunakan git ,berguna untuk melakukan perbandingan(ini disarankan).jika sudah yakin lakukan `git merge origin/nama-branch`
- **git ls-remote**
  - git ls-remote --tags
    manmpilkan ref ke tag
  - git ls-remote --refs
    menampilkan semua ref (tidak hanya branch)
  - git ls-remote --heads
    menampikan semua ref ke branch
    
menampilkan nama tag
`git tag`
membuat tag baru
`git tag "versitag"`
membuat tag di commit tertentu
`git tag <tag_name> <commit_hash>`
membuat anotasi di tag
git tag -a <tag_name> -m "Annotated tag message"
menampilkan informasi tag
git show <tag_name>
menghapus tag di lokal
git tag -d <tag_name>
menghapus tag di remote
git push --delete origin <tag_name>
push tag tertentu ke remote
git push origin <tag_name>
push semua tag ke remote
git push --tags

delete branch di remote
git push origin --delete branch
delete tag di remote
git push origin --delete tag

