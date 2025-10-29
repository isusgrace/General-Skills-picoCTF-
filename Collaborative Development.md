Hi, Can you speak Thai ?

Yes, I can speak Thai.

มา วันนี้เราจะมาทำข้อ Collaborative Development หมวด General Skills

Step 1 สร้าง Directory และนำเข้าไฟล์

ใช้คำสั่ง mkdir ใช้สำหรับสร้างไดเรกทอรี (หรือโฟลเดอร์) ใหม่บนระบบไฟล์
```
mkdir <new directory>
```
ตามด้วย คำสั่ง cd ใช้สำหรับเปลี่ยนไดเรกทอรีหรือโฟลเดอร์ปัจจุบันในเทอร์มินัล
```
cd <new directory>
```
ตามด้วย คำสั่ง wget ใช้สำหรับดาวน์โหลดไฟล์จากอินเทอร์เน็ตโดยตรงผ่านบรรทัดคำสั่ง
```
wget <URL>
```
```
┌──(kali㉿kali)-[~]
└─$ mkdir isusgrace03   
                                                                                             
┌──(kali㉿kali)-[~]
└─$ cd isusgrace03

┌──(kali㉿kali)-[~/isusgrace03]
└─$ wget https://artifacts.picoctf.net/c_titan/176/challenge.zip
--2025-10-26 01:45:38--  https://artifacts.picoctf.net/c_titan/176/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 54.230.42.13, 54.230.42.116, 54.230.42.41, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|54.230.42.13|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24474 (24K) [application/octet-stream]
Saving to: ‘challenge.zip’

challenge.zip           100%[============================>]  23.90K   133KB/s    in 0.2s    

2025-10-26 01:45:39 (133 KB/s) - ‘challenge.zip’ saved [24474/24474]
```

Step 2 unzip
```
┌──(kali㉿kali)-[~/isusgrace03]
└─$ unzip challenge.zip       
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/main  
   creating: drop-in/.git/refs/heads/feature/
 extracting: drop-in/.git/refs/heads/feature/part-1  
 extracting: drop-in/.git/refs/heads/feature/part-2  
 extracting: drop-in/.git/refs/heads/feature/part-3  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/77/
 extracting: drop-in/.git/objects/77/d6ceca6fe23b57d88cf16f20003e10d6715690  
   creating: drop-in/.git/objects/b9/
 extracting: drop-in/.git/objects/b9/32e8c048154a46d224cd7691c99dc8cb88164a  
   creating: drop-in/.git/objects/eb/
 extracting: drop-in/.git/objects/eb/19d0e3c28278752f0735c4451b885136a24105  
   creating: drop-in/.git/objects/6e/
 extracting: drop-in/.git/objects/6e/17fb3a35364b4f9bb8bef8b5e6a5af2d3e7dfa  
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/e44dd37ba0c0adc3d78d0b85d699859ec8d75c  
   creating: drop-in/.git/objects/0c/
 extracting: drop-in/.git/objects/0c/d57e0aedc31a1a92e0b79235c818de437cde8e  
   creating: drop-in/.git/objects/7a/
 extracting: drop-in/.git/objects/7a/b4e25c0cd108374b2275fdb1fcdf635e591833  
 extracting: drop-in/.git/objects/7a/7534d2ed05e1637c5ea21d0981646444c2c9f9  
   creating: drop-in/.git/objects/d1/
 extracting: drop-in/.git/objects/d1/f3407cee4479c075997b497fa290ca636fe258  
   creating: drop-in/.git/objects/70/
 extracting: drop-in/.git/objects/70/64732e2fd39d2247bd6ba2ccc4cf9576974d38  
   creating: drop-in/.git/objects/46/
 extracting: drop-in/.git/objects/46/72a5cadb0c545e90d476f0783c9d0874512b0e  
   creating: drop-in/.git/objects/83/
 extracting: drop-in/.git/objects/83/95824cc0ce486d1be9ab874bfedb2cec2ea398  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/main  
   creating: drop-in/.git/logs/refs/heads/feature/
  inflating: drop-in/.git/logs/refs/heads/feature/part-1  
  inflating: drop-in/.git/logs/refs/heads/feature/part-2  
  inflating: drop-in/.git/logs/refs/heads/feature/part-3  
  inflating: drop-in/flag.py 
```
คำสั่ง unzip ใช้สำหรับแตกไฟล์ที่ถูกบีบอัดในรูปแบบ .zip เพื่อดึงไฟล์และโฟลเดอร์ทั้งหมดออกมาจากไฟล์เก็บถาวรนั้น (ไฟล์ที่เราเลือกจะแตก)
```
┌──(kali㉿kali)-[~/isusgrace03]
└─$ ls -la
total 52
drwxrwxr-x   3 kali kali  4096 Oct 26 01:46 .
drwx------ 178 kali kali 20480 Oct 26 01:44 ..
-rw-rw-r--   1 kali kali 24474 Mar 11  2024 challenge.zip
drwxr-xr-x   3 kali kali  4096 Mar 11  2024 drop-in
```
คำสั่ง ls ใช้แสดงรายการไฟล์และไดเร็กทอรีที่มีอยู่ในไดเร็กทอรีปัจจุบัน

คำสั่ง -l ออปชันนี้สั่งให้ ls แสดงผลในรูปแบบ "ยาว" (Long Listing Format) ซึ่งจะให้ข้อมูลรายละเอียดของไฟล์แต่ละไฟล์ดังนี้

- สิทธิ์ — เช่น drwxr-xr-x 

  ตัวแรกระบุชนิดไฟล์: d = directory, - = regular file, l = symlink

  ตัวต่อมาแบ่งเป็น 3 ชุด แต่ละชุด r=read w=write x=execute

- จำนวนลิงก์ — จำนวน hard links

- เจ้าของไฟล์ — ชื่อผู้ใช้ที่เป็นเจ้าของไฟล์

- กลุ่ม — ชื่อกลุ่มของไฟล์

- ขนาดไฟล์ — ขนาดเป็น bytes

- วันที่และเวลา — วันที่และเวลาที่มีการแก้ไขไฟล์ล่าสุด

- ชื่อไฟล์/ไดเร็กทอรี — ชื่อจริงของไฟล์หรือไดเร็กทอรี

สรุปก็คือ คำสั่ง ls -la แสดงรายการทั้งหมด (รวมไฟล์ที่ซ่อน) ในรูปแบบละเอียด

ในส่วนนี้เราจะเห็น 1 ไฟล์ คือ challenge.zip และ 1 ไดเรกทอรี คือ drop-in

Step 3 drop-in
```
┌──(kali㉿kali)-[~/isusgrace03]
└─$ cd drop-in    
                                                                                             
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ ls    
flag.py
                                                                                             
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ cat flag.py              
print("Printing the flag...")
```
ในส่วนนี้ไม่มีอะไรน่าสนใจ

Step 4 git log
```
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ git log                                   
commit eb19d0e3c28278752f0735c4451b885136a24105 (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:49 2024 +0000

    init flag printer
```
คำสั่ง git log ใช้สำหรับแสดงประวัติการเปลี่ยนแปลงใน Git ซึ่งจะแสดงรายการ commit ทั้งหมดตามลำดับเวลา โดยแต่ละ commit จะประกอบด้วยข้อมูลสำคัญ เช่น แฮชคอมมิต (commit hash), ผู้เขียน, วันที่ และข้อความ commit

ในส่วนนี้ไม่มีอะไรน่าสนใจเช่นกัน

Step 5 git reflog
```
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ git reflog
eb19d0e (HEAD -> main) HEAD@{0}: checkout: moving from feature/part-3 to main
8395824 (feature/part-3) HEAD@{1}: commit: add part 3
eb19d0e (HEAD -> main) HEAD@{2}: checkout: moving from main to feature/part-3
eb19d0e (HEAD -> main) HEAD@{3}: checkout: moving from feature/part-2 to main
7064732 (feature/part-2) HEAD@{4}: commit: add part 2
eb19d0e (HEAD -> main) HEAD@{5}: checkout: moving from main to feature/part-2
eb19d0e (HEAD -> main) HEAD@{6}: checkout: moving from feature/part-1 to main
0cd57e0 (feature/part-1) HEAD@{7}: commit: add part 1
eb19d0e (HEAD -> main) HEAD@{8}: checkout: moving from main to feature/part-1
eb19d0e (HEAD -> main) HEAD@{9}: commit (initial): init flag printer
```
คำสั่ง git reflog ใช้เพื่อแสดงรายการการเปลี่ยนแปลงล่าสุดที่เกิดขึ้นกับ HEAD (ส่วนชี้ไปยัง commit) ของคลังเก็บ Git ซึ่งเปรียบเสมือน "สมุดบันทึก" ที่ช่วยให้เราสามารถย้อนกลับไปดูและกู้คืนสถานะของโปรเจกต์ได้ แม้จะมีการแก้ไขประวัติ เช่น การ commit, การ merge, หรือการลบสาขาโดยไม่ได้ตั้งใจ

Step 6 git branch -a
```
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
```
คำสั่ง git branch -a ใช้สำหรับแสดงรายการ Branch ทั้งหมด ใน Repository ของเรา

Step 7 git checkout feature/part-1
```
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ git checkout feature/part-1
Switched to branch 'feature/part-1'
```
คำสั่ง git checkout เป็นคำสั่งที่ใช้ในการเปลี่ยนเวอร์ชันหรือสถานะการทำงาน ภายใน Git Repository ของเรา หน้าที่หลักของมันคือการย้ายตัวชี้ HEAD ไปยังตำแหน่งที่ระบุ ซึ่งทำให้เราสามารถทำงานกับ Branch, Commit, หรือ Tag ที่แตกต่างกันได้

ในส่วนนี้ มันจะย้ายตัวชี้ HEAD ไปยัง Commit ล่าสุดของ Branch ปลายทาง และอัปเดตไฟล์ทั้งหมดในพื้นที่ทำงานของเราให้ตรงกับสถานะโค้ดของ Branch นั้น นั่นก็คือ feature/part-1 (ชื่อ Branch ปลายทางที่ต้องการสลับไปทำงาน)
```
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ ls -la
total 16
drwxr-xr-x 3 kali kali 4096 Oct 26 02:27 .
drwxrwxr-x 3 kali kali 4096 Oct 26 01:46 ..
-rw-rw-r-- 1 kali kali   64 Oct 26 02:27 flag.py
drwxr-xr-x 8 kali kali 4096 Oct 26 02:28 .git
                                                                                             
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ cat flag.py
print("Printing the flag...")
print("picoCTF{XXXXX_1", end='')
```
คำสั่ง cat ใช้เพื่อแสดงเนื้อหาของไฟล์

พอเรา cat flag.py เราก็จะเห็น flag ส่วนที่ 1 ปรากฏออกมาให้เห็น

Step 8 git checkout feature/part-2
```
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ git checkout feature/part-2
Switched to branch 'feature/part-2'
                                                                                             
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ ls -la
total 16
drwxr-xr-x 3 kali kali 4096 Oct 26 02:43 .
drwxrwxr-x 3 kali kali 4096 Oct 26 01:46 ..
-rw-rw-r-- 1 kali kali   64 Oct 26 02:43 flag.py
drwxr-xr-x 8 kali kali 4096 Oct 26 02:43 .git
                                                                                             
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ cat flag.py
print("Printing the flag...")

print("XXXXX_2", end='') 
```
ทำเหมือน Step 7

เราก็จะเห็น flag ส่วนที่ 2 ปรากฏออกมาให้เห็น

Step 9 git checkout feature/part-3
```
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ git checkout feature/part-3
Switched to branch 'feature/part-3'
                                                                                             
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ ls -la
total 16
drwxr-xr-x 3 kali kali 4096 Oct 26 02:43 .
drwxrwxr-x 3 kali kali 4096 Oct 26 01:46 ..
-rw-rw-r-- 1 kali kali   55 Oct 26 02:43 flag.py
drwxr-xr-x 8 kali kali 4096 Oct 26 02:43 .git
                                                                                             
┌──(kali㉿kali)-[~/isusgrace03/drop-in]
└─$ cat flag.py
print("Printing the flag...")

print("XXXXX_3")
```
ทำเหมือน Step 7 

เราก็จะเห็น flag ส่วนที่ 3 ปรากฏออกมาให้เห็น

XXXXX_1 = flag ส่วนที่ 1

XXXXX_2 = flag ส่วนที่ 2

XXXXX_3 = flag ส่วนที่ 3

XXXXX ไม่ใช่ flag นะ คือปิดไว้ จะได้ทำเอง
