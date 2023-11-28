# aman# so-uasp-2023
# [github](https://github.com/auriza/os-lab/blob/master/13-shell-script.md)
# BAB 8

---

```bash
# echo
Menampilkan satu baris teks.
echo [OPTION] [STRING]
-n : newline
contoh : echo "Hello World"


# hostname
Menampilkan nama host sistem.
hostname [OPTION]
-I: tampilkan alamat IP


# uname
Menampilkan informasi kernel sistem.
uname [OPTION]
-a: all; semua info


# date
Mencetak tanggal dan waktu sistem.
date [+FORMAT]
contoh : date


# cal
Menampilkan kalender.
cal [[MONTH] YEAR]
contoh : cal 6 2012

#who
Menampilkan siapa yang sedang login.
who [OPTION]
-q: quantity; jumlah user yang sedang login
-w: write status untuk pesan (+, -, ?)

```

# BAB 9

---

```bash
# cd
Mengganti direktori (default ke direktori home).
cd [DIR]


# pwd
Mencetak nama direktori saat ini.
pwd

# ls
Menampilkan daftar isi direktori.
ls [OPTION] [FILE]
-a: all; tampilkan semua
-l: long; format panjang
-h: human-readable; format ukuran
-i: inode; cetak nomor inode file


# touch
Meng-update waktu akses dan modifikasi suatu FILE.
touch FILE
Jika FILE belum ada, maka touch akan membuat FILE kosong.


# cp
Menyalin file dan direktori.
cp [OPTION] SOURCE DEST
cp [OPTION] SOURCES... DIR
-r: recursive; salin direktori seisinya
-f: force; tanpa konfirmasi jika overwrite
-i: interactive; konfirmasi sebelum overwrite

#mv
Memindahkan (mengganti nama) file.
mv [OPTION] SOURCE DEST
mv [OPTION] SOURCES... DIR
-f: force; tanpa konfirmasi jika overwrite
-i: interactive; konfirmasi sebelum overwrite


#rm
Menghapus file atau direktori.
rm [OPTION] FILE...
-r: recursive; hapus direktori seisinya
-f: force; tanpa konfirmasi jika error
-i: interactive; konfirmasi sebelum menghapus


#mkdir
Membuat direktori.
mkdir [OPTION] DIR
-p: parent; buat direktori parent jika diperlukan


#rmdir
Menghapus direktori kosong.
rmdir [OPTION] DIR...
-p: parent; hapus beserta direktori parent-nya

#chmod
Mengubah mode permission suatu file.
chmod [OPTION] MODE FILE...
-R: recursive; ubah direktori seisinya


#ln
Membuat link antar-file.
ln [OPTION] TARGET LINK-NAME
-s: symbolic; buat symlink

```

# BAB 10

---

```bash
# locate
Mencari file berdasarkan namanya.
locate [OPTION] 'PATTERN'
-c: count; tampilkan jumlah file yang ditemukan
-i: ignore-case


# find
Mencari file pada sebuah hierarki direktori.
find [PATH] [TEST]...
-name 'PATTERN'
-iname 'PATTERN'
-size [+-]N[kMG]
-atime [+-]N
-mtime [+-]N
-empty
-type [dfl] file 


# wc
Mencetak jumlah baris, kata, dan karakter dari suatu file.
wc [OPTION] [FILE...]
-c: char; cetak jumlah karakter
-l: line; cetak jumlah baris
-w: word; cetak jumlah kata

# cat
Menggabungkan file dan menampilkan isinya ke layar.
cat [FILE]...

# head
Menampilkan bagian awal file (default: 10 baris).
head [OPTION] [FILE]
-c: chars; tampilkan sekian karakter pertama
-n: lines; tampilkan sekian baris pertama

# tail
Menampilkan bagian akhir file (default: 10 baris).
tail [OPTION] [FILE]
-c: chars; tampilkan sekian karakter terakhir
-n: lines; tampilkan sekian baris terakhir


# sort
Mengurutkan baris teks pada file.
sort [OPTION] [FILE]
-n: numeric; urutkan secara numerik
-r: reverse; urutkan terbalik
-k: key; urutkan berdasarkan kolom ke-sekian
-t: karakter pemisah antarkolom

# uniq
Menghilangkan baris teks yang berulang.
uniq [OPTION] [FILE]
-c: count; tampilkan jumlah kemunculan
-i: ignore-case

# cut
Mengambil karakter/kolom tertentu dari tiap baris teks.
cut OPTION [FILE]
-c: char; cetak karakter ke-sekian
-f: field; cetak kolom ke-sekian
-d: delimiter; pemisah antarkolom

# tr
Translasi karakter dari set pertama ke set kedua.
tr [OPTION] SET1 [SET2]
-d: delete; hapus karakter pada SET1
-s: squeeze; hapus karakter yang berulang pada SET1

# grep
Mencetak baris teks yang cocok dengan suatu pola.
grep [OPTION] 'PATTERN' FILE
-c: count; tampilkan jumlah baris
-i: ignore-case
-r: rekursif
-v: invert; kebalikan dari pola yang diberikan
-E: extended regex

# sed
Stream editor, manipulasi baris teks dengan regular expression.
sed [OPTION] 's/SEARCH/REPLACE/' [FILE]
-e: execute; tambahkan perintah untuk dieksekusi
-i: in-place; edit file langsung
-E: extended regex

```

# BAB 11

---

```bash
# ps
Menampilkan cuplikan informasi proses yang sedang berjalan.
ps [OPTION]
-A: all; tampilkan semua proses
-F: full; tampilkan format lengkap
-L: light-weight process; tampilkan info thread


# nice
Menjalankan program dengan prioritas nice[^12-nice] tertentu (default: 10).
nice [-n NICE] COMMAND
[^12-nice]: nilai nice antara -20 (prioritas tinggi) sampai 19 (prioritas rendah)

# renice
Mengubah prioritas proses yang sudah berjalan.
renice [-n] NICE PID

# pidof
Mendapatkan PID dari nama program yang sedang berjalan.
pidof PROGRAM


# kill
Mengirim sinyal ke suatu proses (default: SIGTERM).
kill [-SIG] PID...
-INT
-KILL
-STOP
-CONT

# & 
Untuk menjalankan proses di background, tambahkan tanda & pada akhir perintah.
COMMAND... &


# jobs
Menampilkan daftar job yang sedang aktif.
jobs


# fg
Memindahkan job ke foreground.
fg %JOB


# bg
Memindahkan job ke background.
bg %JOB

```

# Latihan UASP

---

```bash
# pindah ke direktori home anda
cd

# buat satu folder kosong 'test'
mkdir test

# masuk ke direktori 'test'
cd test

# tampilkan path direktori saat ini
pwd

# buat file kosong bernama 'empty.txt'
touch empty.txt
```

---

```bash
# copy file '/etc/timezone' ke direktori ini
cp /etc/timezone

# ubah nama file 'timezone' menjadi 'tz.txt'
mv timezone tz.txt

# list isi direktori ini
ls

# pindah ke direktori parent
mv * ../

# hapus direktori 'test' seisinya
rm -r test
```

---

```bash
# temukan file dengan nama 'fdisk' memakai `locate`
locate 'fdisk'

# temukan file dengan nama 'fdisk' memakai `find`
find /home -name fdisk

# temukan file pada home anda yang ukurannya > 200 MB
find ./ -type f -size +200M

# temukan file pada home anda yang diubah < 3 hari
find ./ -type f -mtime -3

# temukan file pada home anda yang diakses > 30 hari
find ./ -type f -atime +30
```

---

```bash
# tampilkan 5 baris pertama keluaran perintah `last`
last | head -n 5

# tampilkan dua baris terakhir file '/etc/passwd'
tail -2 /etc/passwd

# cari file di '/usr/include' yang memuat kata 'sem_post'
grep -r "sem_post" /usr/include

# tampilkan kolom 1 dan 5 dari file '/etc/passwd'
cut -f 1,5 -d ':' /etc/passwd

# tampilkan isi file '/etc/motd' dalam huruf kapital
cat /etc/motd | tr "[a-z]" "[A-Z]"
```

---

```bash
# jalankan `cat /dev/random > rand.txt` di background
cat /dev/random > rand.txt &

# tampilkan daftar job
jobs

# kirim sinyal STOP ke job tersebut
kill -n 19 $(eval 'jobs -p')

# lanjutkan job tersebut di background
bg 1

# kirim sinyal TERM ke job tersebut
kill -n 15 $(eval 'jobs -p')
```

## Kisi-kisi

```
echo hostname uname date cal who
cd pwd ls touch
cp mv rm mkdir rmdir
chmod ln
locate find wc
cat head tail sort uniq cut tr grep sed
ps nice renice pidof kill
& jobs fg bg
```

# Contoh penggunaan [test case]

```

```
# echo
Menampilkan satu baris teks.
echo [OPTION] [STRING]
-n : newline
contoh : 
1. `echo "Hello World"` 
   - Menampilkan "Hello World" di layar.
2. `echo -n "Hello " && echo "World"`
   - Menampilkan "Hello World" tanpa newline di antara "Hello" dan "World".

# hostname
Menampilkan nama host sistem.
hostname [OPTION]
-I: tampilkan alamat IP
contoh : 
1. `hostname`
   - Menampilkan nama host.
2. `hostname -I`
   - Menampilkan alamat IP host.

# uname
Menampilkan informasi kernel sistem.
uname [OPTION]
-a: all; semua info
contoh : 
1. `uname`
   - Menampilkan nama kernel.
2. `uname -a`
   - Menampilkan semua informasi kernel.

# date
Mencetak tanggal dan waktu sistem.
date [+FORMAT]
contoh : 
1. `date`
   - Menampilkan tanggal dan waktu saat ini.
2. `date "+%Y-%m-%d %H:%M:%S"`
   - Menampilkan tanggal dan waktu dalam format kustom.

# cal
Menampilkan kalender.
cal [[MONTH] YEAR]
contoh : 
1. `cal`
   - Menampilkan kalender bulan ini.
2. `cal 6 2012`
   - Menampilkan kalender bulan Juni tahun 2012.

# who
Menampilkan siapa yang sedang login.
who [OPTION]
-q: quantity; jumlah user yang sedang login
-w: write status untuk pesan (+, -, ?)
contoh : 
1. `who`
   - Menampilkan pengguna yang sedang login.
2. `who -q`
   - Menampilkan jumlah pengguna yang sedang login.
3. `who -w`
   - Menampilkan status tulisan untuk pesan.

# cd
Mengganti direktori (default ke direktori home).
cd [DIR]
contoh : 
1. `cd /path/to/directory`
   - Pindah ke direktori tertentu.
2. `cd ~`
   - Pindah ke direktori home.

# pwd
Mencetak nama direktori saat ini.
pwd
contoh :
1. `pwd`
   - Menampilkan path direktori saat ini.

# ls
Menampilkan daftar isi direktori.
ls [OPTION] [FILE]
-a: all; tampilkan semua
-l: long; format panjang
-h: human-readable; format ukuran
-i: inode; cetak nomor inode file
contoh :
1. `ls`
   - Menampilkan daftar isi direktori.
2. `ls -l -a`
   - Menampilkan daftar isi direktori dengan format panjang dan semua file.

# touch
Meng-update waktu akses dan modifikasi suatu FILE.
touch FILE
Jika FILE belum ada, maka touch akan membuat FILE kosong.
contoh :
1. `touch example.txt`
   - Membuat file baru atau mengupdate waktu modifikasi file yang sudah ada.

# cp
Menyalin file dan direktori.
cp [OPTION] SOURCE DEST
cp [OPTION] SOURCES... DIR
-r: recursive; salin direktori seisinya
-f: force; tanpa konfirmasi jika overwrite
-i: interactive; konfirmasi sebelum overwrite
contoh :
1. `cp file.txt /path/to/destination/`
   - Menyalin file ke direktori tujuan.
2. `cp -r directory1 directory2`
   - Menyalin direktori beserta isinya ke direktori lain.

# mv
Memindahkan (mengganti nama) file.
mv [OPTION] SOURCE DEST
mv [OPTION] SOURCES... DIR
-f: force; tanpa konfirmasi jika overwrite
-i: interactive; konfirmasi sebelum overwrite
contoh :
1. `mv file.txt /path/to/destination/`
   - Memindahkan file ke direktori tujuan.
2. `mv oldname.txt newname.txt`
   - Mengganti nama file.

# rm
Menghapus file atau direktori.
rm [OPTION] FILE...
-r: recursive; hapus direktori seisinya
-f: force; tanpa konfirmasi jika error
-i: interactive; konfirmasi sebelum menghapus
contoh :
1. `rm file.txt`
   - Menghapus file.
2. `rm -r directory`
   - Menghapus direktori beserta isinya.

# mkdir
Membuat direktori.
mkdir [OPTION] DIR
-p: parent; buat direktori parent jika diperlukan
contoh :
1. `mkdir new_directory`
   - Membuat direktori baru bernama "new_directory".
2. `mkdir -p /path/to/new/directory`
   - Membuat direktori baru beserta parentnya jika belum ada.

# rmdir
Menghapus direktori kosong.
rmdir [OPTION] DIR...
-p: parent; hapus beserta direktori parent-nya
contoh :
1. `rmdir empty_directory`
   - Menghapus direktori kosong bernama "empty_directory".

# chmod
Mengubah mode permission suatu file.
chmod [OPTION] MODE FILE...
-R: recursive; ubah direktori seisinya
contoh :
1. `chmod +x script.sh`
   - Memberikan permission eksekusi pada file "script.sh".
2. `chmod -R 755 directory`
   - Memberikan permission rekursif pada direktori dan isinya.

# ln
Membuat link antar-file.
ln [OPTION] TARGET LINK-NAME
-s: symbolic; buat symlink
contoh :
1. `ln -s /path/to/target link_name`
   - Membuat symlink dengan nama "link_name" yang menuju ke target.

# locate
Mencari file berdasarkan namanya.
locate [OPTION] 'PATTERN'
-c: count; tampilkan jumlah file yang ditemukan
-i: ignore-case
contoh :
1. `locate filename`
   - Menampilkan path file yang sesuai dengan pola "filename".
2. `locate -c filename`
   - Menampilkan jumlah file yang sesuai dengan pola "filename".

# find
Mencari file pada sebuah hierarki direktori.
find [PATH] [TEST]...
-name 'PATTERN'
-iname 'PATTERN'
-size [+-]N[kMG]
-atime [+-]N
-mtime [+-]N
-empty
-type [dfl] file
contoh :
1. `find /path/to/search -name "*.txt"`
   - Mencari file dengan ekstensi ".txt" pada direktori tertentu.
2. `find /path/to/search -type d -empty`
   - Mencari direktori kosong pada direktori tertentu.

# wc
Mencetak jumlah baris, kata, dan karakter dari suatu file.
wc [OPTION] [FILE...]
-c: char; cetak jumlah karakter
-l: line; cetak jumlah baris
-w: word; cetak jumlah kata
contoh :
1. `wc file.txt`
   - Menampilkan jumlah baris, kata, dan karakter dalam file "file.txt".
2. `wc -l *.txt`
   - Menampilkan jumlah baris dalam semua file dengan ekstensi ".txt".

# cat
Menggabungkan file dan menampilkan isinya ke layar.
cat [FILE]...
contoh :
1. `cat file1.txt file2.txt`
   - Menggabungkan isi dari "file1.txt" dan "file2.txt" ke layar.
2. `cat *.txt > combined.txt`
   - Menggabungkan isi semua file dengan ekstensi ".txt" ke dalam file "combined.txt".

# head
Menampilkan bagian awal file (default: 10 baris).
head [OPTION] [FILE]
-c: chars; tampilkan sekian karakter pertama
-n: lines; tampilkan sekian baris pertama
contoh :
1. `head file.txt`
   - Menampilkan 10 baris pertama dari file "file.txt".
2. `head -n 20 file.txt`
   - Menampilkan 20 baris pertama dari file "file.txt".

# tail
Menampilkan bagian akhir file (default: 10 baris).
tail [OPTION] [FILE]
-c: chars; tampilkan sekian karakter terakhir
-n: lines; tampilkan sekian baris terakhir
contoh :
1. `tail file.txt`
   - Menampilkan 10 baris terakhir dari file "file.txt".
2. `tail -n 15 file.txt`
   - Menampilkan 15 baris terakhir dari file "file.txt".

# sort
Mengurutkan baris teks pada file.
sort [OPTION] [FILE]
-n: numeric; urutkan secara numerik
-r: reverse; urutkan terbalik
-k: key; urutkan berdasarkan kolom ke-sekian
-t: karakter pemisah antarkolom
contoh :
1. `sort file.txt`
   - Mengurutkan baris teks dalam file "file.txt" secara alfabetis.
2. `sort -n -k2,2 data.csv`
   - Mengurutkan file CSV berdasarkan kolom numerik kedua.

# uniq
Menghilangkan baris teks yang berulang.
uniq [OPTION] [FILE]
-c: count; tampilkan jumlah kemunculan
-i: ignore-case
contoh :
1. `uniq names.txt`
   - Menghilangkan baris duplikat dari file "names.txt".
2. `sort file.txt | uniq -c`
   - Menghitung jumlah kemunculan setiap baris dalam file yang sudah diurutkan.

# cut
Mengambil karakter/kolom tertentu dari tiap baris teks.
cut OPTION [FILE]
-c: char; cetak karakter ke-sekian
-f: field; cetak kolom ke-sekian
-d: delimiter; pemisah antarkolom
contoh :
1. `cut -f1,3 data.txt`
   - Menampilkan kolom pertama dan ketiga dari file "data.txt".
2. `cut -d"," -f2,4 data.csv`
   - Menampilkan kolom kedua dan keempat dari file CSV dengan delimiter koma.

# tr
Translasi karakter dari set pertama ke set kedua.
tr [OPTION] SET1 [SET2]
-d: delete; hapus karakter pada SET1
-s: squeeze; hapus karakter yang berulang pada SET1
contoh :
1. `echo "hello" | tr 'a-z' 'A-Z'`
   - Mengonversi teks "hello" menjadi huruf kapital.
2. `echo "aaabbbccc" | tr -s 'a-c'`
   - Menghapus karakter berulang dari set 'a' sampai 'c'.

# grep
Mencetak baris teks yang cocok dengan suatu pola.
grep [OPTION] 'PATTERN' FILE
-c: count; tampilkan jumlah baris
-i: ignore-case
-r: rekursif
-v: invert; kebalikan dari pola yang diberikan
-E: extended regex
contoh :
1. `grep "error" logfile.txt`
   - Menampilkan baris yang mengandung kata "error" dari file log.
2. `grep -r "pattern" /path/to/search`
   - Mencari pola secara rekursif dalam direktori tertentu.

# sed
Stream editor, manipulasi baris teks dengan regular expression.
sed [OPTION] 's/SEARCH/REPLACE/' [FILE]
-e: execute; tambahkan perintah untuk dieksekusi
-i: in-place; edit file langsung
-E: extended regex
contoh :
1. `sed 's/apple/orange/' fruits.txt`
   - Menggantikan setiap kemunculan "apple" dengan "orange" dalam file "fruits.txt".
2. `sed -i 's/old/new/g' data.txt`
   - Mengganti setiap kemunculan "old" dengan "new" dalam file "data.txt" secara langsung.

# ps
Menampilkan cuplikan informasi proses yang sedang berjalan.
ps [OPTION]
-A: all; tampilkan semua proses
-F: full; tampilkan format lengkap
-L: light-weight process; tampilkan info thread
contoh :
1. `ps`
   - Menampilkan daftar proses yang sedang berjalan.
2. `ps -A -F`
   - Menampilkan format lengkap dari semua proses.

# nice
Menjalankan program dengan prioritas nice[^12-nice] tertentu (default: 10).
nice [-n NICE] COMMAND
[^12-nice]: nilai nice antara -20 (prioritas tinggi) sampai 19 (prioritas rendah)
contoh :
1. `nice -n 5 command`
   - Menjalankan perintah dengan prioritas nice +5.
2. `nice -n -10 command`
   - Menjalankan perintah dengan prioritas nice -10.

# renice
Mengubah prioritas proses yang sudah berjalan.
renice [-n] NICE PID
contoh :
1. `renice -n 10 1234`
   - Mengubah prioritas proses dengan PID 1234 menjadi +10.
2. `renice --priority 5 -p 5678`
   - Mengubah prioritas proses dengan PID 5678 menjadi +5.

# pidof
Mendapatkan PID dari nama program yang sedang berjalan.
pidof PROGRAM
contoh :
1. `pidof firefox`
   - Menampilkan PID dari proses Firefox.
2. `pidof -s chrome`
   - Menampilkan satu PID dari proses Chrome.

# kill
Mengirim sinyal ke suatu proses (default: SIGTERM).
kill [-SIG
```
# Mengirim sinyal SIGTERM ke proses dengan PID 1234
kill 1234

# Mengirim sinyal SIGKILL ke proses dengan PID 5678
kill -KILL 5678

```


# Latihan UASP
```
# Pindah ke direktori home
cd ~

# Buat satu folder kosong 'test'
mkdir test

# Masuk ke direktori 'test'
cd test

# Tampilkan path direktori saat ini
pwd

# Buat file kosong bernama 'empty.txt'
touch empty.txt

# Copy file '/etc/timezone' ke direktori ini
cp /etc/timezone .

# Ubah nama file 'timezone' menjadi 'tz.txt'
mv timezone tz.txt

# List isi direktori ini
ls

# Pindah ke direktori parent
cd ..

# Hapus direktori 'test' beserta isinya
rm -r test

# Temukan file dengan nama 'fdisk' memakai `locate`
locate fdisk

# Temukan file dengan nama 'fdisk' memakai `find`
find / -name fdisk

# Temukan file pada home anda yang ukurannya > 200 MB
find ~ -size +200M

# Temukan file pada home anda yang diubah < 3 hari
find ~ -mtime -3

# Temukan file pada home anda yang diakses > 30 hari
find ~ -atime +30

# Tampilkan 5 baris pertama keluaran perintah `last`
last | head -n 5

# Tampilkan dua baris terakhir file '/etc/passwd'
tail -n 2 /etc/passwd

# Cari file di '/usr/include' yang memuat kata 'sem_post'
grep -rl 'sem_post' /usr/include

# Tampilkan kolom 1 dan 5 dari file '/etc/passwd'
cut -f 1,5 -d : /etc/passwd

# Tampilkan isi file '/etc/motd' dalam huruf kapital
cat /etc/motd | tr 'a-z' 'A-Z'

# Jalankan `cat /dev/random > rand.txt` di background
cat /dev/random > rand.txt &

# Tampilkan daftar job
jobs

# Kirim sinyal STOP ke job tersebut
kill -STOP %1

# Lanjutkan job tersebut di background
bg %1

# Kirim sinyal TERM ke job tersebut
kill %1

```
