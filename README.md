# Ahmad Farrel Aly
# 09011282328045
# SK3C
# Praktikum Sistem Operasi

1. Eksekusi seluruh profile yang ada :
a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : echo “Profile dari /etc/profile” 
 ![1](./Tugas6/1.png)  ![1a-1](./Tugas6/1a-1.png)  ![1a-2](./Tugas6/1a-2.png)

b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :
/home/stD02001/.bash_profile
/home/. stD02001/.bash_login
/home/mahasiswa/.profile
/home/mahasiswa/.bashrc
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : echo “Profile dari .bash_profile” Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan. ![1b](./Tugas6/1b.png) ![1b-1](./Tugas6/1b-1.png)  ![1b-1-1](./Tugas6/1b-1-1.png)
# ############
![1b-2](./Tugas6/1b-2.png)  ![1b-2-2](./Tugas6/1b-2-2.png)
# ############
![1b-3](./Tugas6/1b-3.png)  ![1b-3-2](./Tugas6/1b-3-2.png)
# ############
![1b-4](./Tugas6/1b-4.png)  ![1b-4-2](./Tugas6/1b-4-2.png)
# ############
c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:
$ su mahasiswa
$ exit
kemudian gunakan opsi – sebagai berikut :
$ su – mahasiswa
$ exit
Jelaskan perbedaan kedua utilitas tersebut. ![1c](./Tugas6/1c.png)
# ############
2. Prompt String (PS) 
# ############
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell
PS1=‟> „
export PS1
# ############
![2a](./Tugas6/2a.png)
b. Eksperimen hasil PS1 : $ PS1=“\! > “
69 > PS1=”\d > “
Mon Sep 23 > PS1=”\t > “
10:10:20 > PS1=”Saya=\u > “
Saya=mahasiswa > PS1=”\w >”
~ > PS1=\h >” ![2b](./Tugas6/2b.png)
# ############
3. Logout
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout
Echo “Terima kasih atas sesi yang diberikan”
Sleep 5
clear ![3](./Tugas6/3.png)
![3-2](./Tugas6/3-2.png)
# #############
4. Bash script
a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :
p1.sh
#! /bin/bash
echo “Program p1”
ls –l
p2.sh
#! /bin/bash
echo “Program p2”
who
p3.sh
#! /bin/bash
echo “Program p3”
ps x
![4a](./Tugas6/4a.png)
###
![4a-1](./Tugas6/4a-1.png)
###
![4a-2](./Tugas6/4a-2.png)
###
![4a-3](./Tugas6/4a-3.png)
###
b. Jalankan script tersebut sebagai berikut :
$ ./p1.sh ; ./p3.sh ; ./p2.sh
$ ./p1.sh &
$ ./p1.sh $ ./p2.sh & ./p3.sh &
$ ( ./p1.sh ; ./p3.sh ) & 
![4b-1](./Tugas6/4b-1.png)
###
![4b-1-2](./Tugas6/4b-1-2.png)
###
![4b-2](./Tugas6/4b-2.png)
###
![4b-3](./Tugas6/4b-3.png)
###
![4b-4](./Tugas6/4b-4.png)
###
![4b-5](./Tugas6/4b-5.png)
###
5. Jobs
### 
a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. #!/bin/bash
while [ true ]
do
date >> hasil
sleep 10
done 
![5a](./Tugas6/5a.png)
###
b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background
sebagai berikut :
$ jobs
$ find / -print > files 2>/dev/null &
$ jobs
![5b](./Tugas6/5b.png)
###
c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke
background
$ fg %1
$ bg
![5c](./Tugas6/5c.png)
###
d. Stop program background dengan utilitas kil
$ ps x
$ kill [Nomor PID] 
![5d](./Tugas6/5d.png)
![5cd](./Tugas6/5cd.png)
###
6. History
###
a. Ganti nilai HISTSIZE dari 1000 menjadi 20
$ HISTSIZE=20
$ h
![6a](./Tugas6/6a.png)
###
b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir
dilakukan
$ !-5
![6b](./Tugas6/6b.png)
###
c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer
$ !! 
![6c](./Tugas6/6c.png)
###
d. Ulangi instruksi pada history bufer nomor 150
$ !150
![6d](./Tugas6/6d.png)
###
e. Ulangi instruksi dengan prefix “ls”
$ !ls
![6e](./Tugas6/6e.png)
