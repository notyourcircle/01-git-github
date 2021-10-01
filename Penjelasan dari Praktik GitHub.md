# Langkah-Langkah Praktik GitHub

Nama : Imanuel Puspa Wardaya
NIM	 : 5200411349

Disini saya akan menjelaskan langkah-langkah untuk membuat repo.</br>
Daftar Langkah-Langkahnya :
1. Instalasi Git
2. Pembuatan Akun GitHub
3. Konfigurasi Akun GitHub
4. Membuat Repo

## Instalasi Git

Langakah awal, kita akan menginstal Git itu sendiri. Karena saya menggunakan windows, maka saya melakukan instalasi git terlebih dahulu seperti yang telah dicontohkan pada [GitHub ini](https://github.com/zimera-systems/petunjuk-git-github/blob/main/01-install-git.md)
. Tetapi karena terdapat perbedaan versi maka terdapat pilihan yang berbeda dari tutorial tersebut.
salah satunya adalah ini</br>
![instalasi git](/Gambar/2.jpg)</br>
Kalian tinggal pilih yang **Default**</br>
![instalasi git2](/Gambar/1.jpeg)</br>
Untuk yang ini, kalian bisa pilih **Git Creditial Manager Core** atau **Git Credential Manager**.

## Pembuatan Akun GitHub

Lalu karena saya belum memiliki akun GitHub, maka selanjutnya kita akan melakukan Sign Up
(jika kalian sudah memiliki akun Git Hub maka kalian cukup sign in dan lanjut ke tahap selanjutnya)
Kalian cukup menuju ke [link GitHub](https://github.com/). </br>
Selanjutnya akan muncul tampilan seperti ini </br>
![sign up git 1](/Gambar/SignUp1.png)</br>
Kalian bisa memilih **Sing Up** yang berada di pojok kanan atas atau mengetikkan **email address** kalian lalu klik **Sing Up for GitHub** (jika kalian memilih opsi mengetikkan email address maka pada langkah selanjutnya kalian tidak perlu mengetikkan email address</br>
![sign up git 2](/Gambar/SignUp2.png)</br>
Selanjutnya kalian diminta untuk mengetikkan email address yang akan digunakan untuk akun GitHub, email disini bebas
bisa dari gmail, yahoo, dll lalu klik **continue**</br>
![sign up git 3](/Gambar/SignUp3.png)</br>
Berikutnya kita diminta untuk membuat password GitHub kita, silahkan diisi sesuai dengan keinginan lalu kita klik **continue** lagi</br>
![sign up git 4](/Gambar/SignUp4.png)</br>
Berikutnya kita diminta untuk membuat username GitHub kita, silahkan diisi sesuai dengan keinginan lalu kita klik **continue** lagi</br>
![sign up git 5](/Gambar/SignUp5.png)</br>
Selanjutnya kalian diberi pilihan untuk menerima pembaruan produk dan pengumuman pembaruan via email. Kalian bisa ketik **y** (setuju) ataupun **n** (tidak setuju)
sesuai keinginan kalian.</br>
Dan yang terakhir kalian tinggal verify account kita dan tinggal klik **create account**. Selesai

## Konfigurasi Akun GitHub

Setelah melakukan pembuatan akun, berikutnya kita tinggal melakukan Konfigurasi Git, tentu saja kita harus memiliki akun GitHub sebelum melakukan 
konfigurasi git. 
Caranya cukup mudah yaitu kita tinggal menuliskan code pada **cmd** kita ataupun pada **Git Bash** kita

```bash
$ git config --global user.name "username yang telah kalian buat sebelumnya"
$ git config --global user.email emailkalian
```

(jika pada cmd tidak perlu $)
dimana username dan email yang diisi harus username dan email yang telah dibuat sebelumnya.</br>

lalu untuk mengecek apakah konfigurasi akun GitHub kita sudah benar cukup mengetikkan code 

```bash
$ git config --list
```

Tentu saja hal ini cukup dilakukan satu kali saja, kecuali jika kita ingin melakukan perubahan username dan email.

## Membuat Repo

Untuk membuat repo, pertama kita harus login ke akun GitHub kita.</br>
![repo git 1](/Gambar/Repo 1.png)</br>
Pertama kita klik tanda **+** seperti pada gambar diatas, lalu klik **New repository**.</br>
![repo git 1](/Gambar/Repo 2.png)</br>
Selanjutnya kita isi nama repo yang akan kita buat pada kolom Repository name. Lalu kita 
juga diberi pilihan untuk membuat repo secara **Public** atau **Private** sesuai dengan keinginan kalian.
kita juga bisa membuat **README file** secara otomatis dengan mencentang kota **Add a README file**. Setelah semua selesai 
diatur maka klik **Create repository**.</br>
Langkah selanjutnya kita perlu melakukan **Clone Repo** untuk mengatur file .md yang akan kita buat pada pc kita. Untuk melakukan `clone`
diperlukan perintah 

```bash
$ git clone https://github.com/username-kalian/nama-repo-kalian
```

Repo yang telah kita clone akan sama seperti repo yang ada pada pc kita. Selanjutnya 
kita akan mengubah status repo local kita yang ada dipc dari **main** menjadi **master** dengan menggunakan code

```bash
$ cd nama-repo-kalian
$ git branch -m main
```

Setelah itu kita dapat mengelola repo kita melalui pc kita secara manual menggunakan text editor yang kita minati. Lalu untuk 
mengupload (push) ke repo kita. Kita mempunyai 2 cara, yaitu **cara push tanpa branching dan merging** dan **push dengan branching dan merging**
Saya sendiri menggunakan cara push tanpa branching dan merging walaupun memiliki kelemahan jika terdapat kesalahan pada pengeditan repo, maka kita perlu 
menggedit repo tersebut ke pc kita lalu kita push lagi dan jika terjadi banyak kesalahan kita akan sering sekali melakukan push yang sedikit merepotkan.</br>
Caranya melakukan **push tanpa branching dan merging** yaitu 

```bash
$ cd 01-git-github
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Penjelasan dari Praktik GitHub.md
        deleted:    logo.png

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Gambar/

no changes added to commit (use "git add" and/or "git commit -a")

$ git add -A

$ git commit -m "Add: Penjelasan"
[main 8fbf621] Add: Penjelasan
 11 files changed, 91 insertions(+), 1 deletion(-)
 create mode 100644 Gambar/1.jpeg
 create mode 100644 Gambar/2.jpg
 create mode 100644 Gambar/Repo 1.png
 create mode 100644 Gambar/Repo 2.png
 create mode 100644 Gambar/SignUp 1.png
 create mode 100644 Gambar/SignUp 2.png
 create mode 100644 Gambar/SignUp 3.png
 create mode 100644 Gambar/SignUp 4.png
 create mode 100644 Gambar/SignUp 5.png
 rename logo.png => Gambar/logo.png (100%)

$ git push origin main
Enumerating objects: 15, done.
Counting objects: 100% (15/15), done.
Delta compression using up to 12 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (13/13), 2.22 MiB | 750.00 KiB/s, done.
Total 13 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/notyourcircle/01-git-github.git
   1255f8c..8fbf621  main -> main
```