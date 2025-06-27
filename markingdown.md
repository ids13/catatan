 Heading
-
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6




Paragraf
---
untuk membuat membuat paragraf, tambahkan "blank line".untuk memisahkan baris.  

contoh :

**ini paragraf pertama**. asdf asdfsadfasdf sadfsadf asdf asdfasdf asdf.sadfsadf asdfasdf asdfasdf.

**ini paragraf kedua**. asdfasdf asdf asdffasdff assf asdfsadf  asdf asdfasdf asdfasdffsadff asdfffdsaasdffdsa .

indentasi
---
untuk menambahkan indentasi gunakan `&nbsp;`
contoh:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ini contoh paragraf dengan indentasi (bagian paragraf yang menjorok ke dalam).asdfasdfasfs asdfasdf asdfasdf asdfasdf asdffasdfasdf sdfasdf asdfsadf sadfdfsa fdsaasdf 

Baris baru
---
untuk membuat baris baru,di bagian akhir baris tambahkan dua atau lebih spasi kemudian tekan enter. contoh:  

baris pertama  
baris kedua  


Format text 
---
**Tebal**  
*miring*  
***Tebaldan miring***  
~~strike~~  

> quote

> multiple
> 
> quote

> nested
> 
>> quote
>
> block


> ### block quote
> - dengan
> - elemen
> 
> **di** dalam *nya*

disarankan untuk menambahakn "blank line" sesudah dan sebelum quote  

Garis Horizontal
---
untuk menampilkan garis horizontal gunakan `---`.tambahkan blank line di sebelum dan sesudahnya, jika tidak ini akan menjadi "heading line" contoh:  

blank line:  

garis

---

no blank line:  

garis
---


Ordered List
-
1. satu
2. dua
   1. dua satu
   2. dua dua
3. tiga

Unodered List
---
- satu
- dua
  - dua satu
  - dua dua
- tiga


Menambahkan elemen ke dalam list
---
untuk menambahkan elemen ke dalam list dan menjaga konsistensinya. tambahakn 4 spasi atau 1 tab  
contoh:  
1. ini baris pertama
2. ini baris kedua
    
   > ini hal lain yang saya lakukan di baris ke dua

3. ini  

contoh lain:
- ini baris pertama
- ini baris kedua
    
    > ini hal lain yang saya lakukan di baris ke dua

- ini

list todo
---
- [x] Menulis artikel 
- [ ] Belajar Git 

Code
---
gunakan backticks untuk menampilkan code  
contoh:  
`selec * from tabel`
untuk escape backticks gunakan double backticks  
contoh:  
``menggunakan `select * from tabel` untuk menampilkan data di tabel``

Fenced Code Block 
---
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
``` 

Menambah link
------------------------

langsung tanpa samaran

https://en.wikipedia.org/wiki/Markdown

akan ada tulisan "link ke petani kode"

[link ke petanikode](https://www.petanikode.com/)


ini dengan tambahan title(ketiak cursor di arahkan ke link)

[link ke petanikode](https://www.petanikode.com/ "salah satu favorit saya")

merubah email dant tautan dengan cepat

<https://www.markdownguide.org>  
<fake@example.com>

Menambahkan gambar
---
![alt text](https://www.petanikode.com/img/markdown/markdown-vscode.png)

bedanya dengan menambahkan link adalah di bagian depannya ada tanda seru

<h2 id="custom-id">table</h2>

---

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

alignment table
---

| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |



Tanda ``` berfungsi untuk menulis source code. Lalu pada pembuka kita tambahkan nama bahasanya agar teksnya berwarna (syntax highligting).

Footnote
---
Here's a sentence with a footnote. [^1]

[^1]: This is the footnote. 

cross reference
---
Heading id :

`<h2 id="custom-id">table</h2>`  

Link to id :

`[ke bagian table](#custom-id)`  

[ke bagian table](#custom-id)



