markdown
=======

membuat heading
----------------------------
# Heading 1
## Heading 2
### Heading 3
sama seperti html, ada 6 level

horizontal
---------------
---
harus ada space antara atas bawah


format text 
------------------
**Tebal**
*miring*
~~strike~~
> quote

menambah link
------------------------
https://en.wikipedia.org/wiki/Markdown : langsung tanpa samaran
[link ke petanikode](https://www.petanikode.com/) : akan ada tulisan "link ke petani kode"

menambahkan gambar
------------------------------------
![Gambar teks editor VS Code](https://www.petanikode.com/img/markdown/markdown-vscode.png)
bedanya dengan menambahkan link adalah di bagian depannya ada tanda seru

cross reference
-----------------------
[Chapter 1](#chapter-1)
## Chapter 1 <a name="chapter-1"></a>


list
------
- naga
  - langit
- putra
- raja

list todo
-------------
- [x] Menulis artikel 
- [ ] Belajar Git 

Inline Code (code dalamsatu baris)
-----------------------------------------------------
contoh `apt update` adalah command linux

source code (multiline)
-----------------------------------

```java
isi cource code
```

Tanda ``` berfungsi untuk menulis source code. Lalu pada pembuka kita tambahkan nama bahasanya agar teksnya berwarna (syntax highligting).
