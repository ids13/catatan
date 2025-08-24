# 📘 Git Cheatsheet

## 1. Pengaturan Akun Git
Git punya 3 tingkatan konfigurasi:
- `--local` → hanya untuk repository aktif
- `--global` → berlaku untuk user saat ini
- `--system` → berlaku untuk semua user di komputer  
*(Jika tidak dideklarasikan, default = `--local`)*
```bash
git config --global user.name "Nama Anda"       # mengatur user
git config --global user.email "email@anda.com" # mengatur email
git config --list                               # melihat semua config aktif
git config --global --list                      # melihat config global
```
## Inisialisasi Repositori
```bash
git init                          # membuat repository baru
git clone <url_repository>        # clone repository dari remote
```
## Menambahkan dan Merubah File
```bash
git add nama_file                 # tambahkan file ke staging area
git add .                         # tambahkan semua perubahan
git commit -m "Pesan commit"      # membuat commit baru
git commit -am "Pesan commit"     # add & commit sekaligus (untuk file yg sudah pernah ditrack)
```
## Melihat dan Mengecek Status
```bash
git status                        # lihat status perubahan
git diff                          # lihat perbedaan working dir ↔ staging area
git diff --staged                 # lihat perbedaan staging area ↔ last commit
```
# Cabang (Branch)
```bash
git branch                        # daftar branch
git branch nama_cabang            # buat branch baru
git checkout nama_cabang          # pindah branch
git checkout -b nama_cabang       # buat + pindah branch baru
git branch -d nama_cabang         # hapus branch lokal
git push origin --delete nama_cabang  # hapus branch di remote
```
## Menggabungkan (Merge) Cabang
```bash
git checkout branch_tujuan
git merge branch_asal             # gabungkan branch_asal → branch_tujuan
git rebase branch_tujuan          # memindahkan commit ke atas branch_tujuan
git rebase -i HEAD~3              # interactive rebase (edit/squash commit)
```
# Remote Repository
```bash
git remote -v                              # lihat daftar remote
git remote add origin <url_repository>     # tambah remote
git remote show origin                     # info detail remote
git remote show nama_remote                # menampilkan informasi terkait remote repository
git fetch                                  # ambil update tanpa merge
git pull origin nama_cabang                # ambil + merge perubahan
git push origin nama_cabang                # kirim commit ke remote
git push origin --delete branch            # delete branch di remote
git push origin --delete tag               # delete tag di remote
```
# Reset, Revert, Checkout
```bash
git checkout <branch/commit_hash>   # pindah branch atau commit
git reset <commit_hash>             # reset ke commit tertentu
  --soft   # simpan perubahan di staging
  --mixed  # default, simpan perubahan di working dir
  --hard   # hapus semua perubahan
git revert <commit_hash>            # buat commit baru yg membatalkan commit tertentu, tanpa mengubah sejarah commit sebelumnya
```
# log
```bash
git log                           # lihat log lengkap
git log -p                        # lihat log + perubahan
git log --oneline                 # ringkas dalam satu baris
git log --graph                   # tampilkan pohon branch/merge
git log <commit_hash>             # log berdasar commit tertentu
git log <nama_file>               # log perubahan file tertentu
git log --author="nama"           # log commit oleh author tertentu
git log HEAD..origin/nama-branch  # ini ntuk melihat perbedaan antara lokal branch dan remote branch
```
# ls-remote
```bash
git ls-remote --tags      # manmpilkan ref ke tag
git ls-remote --refs      # menampilkan semua ref (tidak hanya branch)
git ls-remote --heads     # menampikan semua ref ke branch
git blame nama_file       # lihat siapa yang terakhir ubah tiap baris
git shortlog -s -n        # ringkas kontribusi per penulis
```
# Tag
```bash
git tag                              # daftar tag
git tag v1.0.0                       # buat tag baru
git tag <tag> <commit_hash>          # buat tag di commit tertentu
git tag -a v1.0.0 -m "Pesan"         # annotated tag
git show v1.0.0                      # lihat info tag
git tag -d v1.0.0                    # hapus tag lokal
git push origin v1.0.0               # push tag ke remote
git push --tags                      # push semua tag
git push --delete origin v1.0.0      # hapus tag di remote
```
# stash
```bash
git stash save "pesan opsional"      # simpan perubahan sementara
git stash list                       # daftar stash
git stash apply                      # terapkan stash terakhir
git stash pop                        # apply + hapus stash
git stash drop stash@{0}             # hapus stash tertentu
```
# clean
```bash
git clean -n   # lihat file yg akan dihapus (untracked)
git clean -f   # hapus file untracked
git clean -fd  # hapus file & folder untracked
```
# undo
```bash
git restore nama_file                # kembalikan file dari staging
git restore --staged nama_file       # unstage file dari staging area
git commit --amend                   # ubah commit terakhir (pesan/isi)
```