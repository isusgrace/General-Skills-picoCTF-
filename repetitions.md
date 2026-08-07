Hi, Can you speak Thai ?

Yes, I can speak Thai.

มา วันนี้เราจะมาทำข้อ repetitions หมวด General Skills 

# Step 1 Notepad

ข้อนี้จะให้ไฟล์มา 1 ไฟล์ ให้เราทำการดาวน์โหลดแล้วเปิดไฟล์ใน Notepad หรือเปิดที่อื่นก็ได้ ไฟล์นี้ไม่เสียหาย สามารถเปิดดูได้ปกติ

```
ดาวน์โหลดไฟล์ ➜ เปิดใน Notepad ➜ ดูเนื้อหาในไฟล์
```

# Step 2 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ee90aa54-1833-4b6d-b4b8-21526d7cd574" />

ภาพที่ 1

```
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKVVZXMTRWMDVHV2toalJYUlhDazFyV25sVVZXaHpWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
```

เนื้อหาที่อยู่ในไฟล์เป็นดังภาพที่ 1 ตัว Flag ถูกเข้ารหัสด้วย Base64 อยู่ ฉันมี 2 วิธีที่ที่จะใช้ในการถอดรหัส คือ ใช้ CyberChef กับ Kali Linux สามารถเลือกใช้วิธีใดวิธีหนึ่งได้เลย

## วิธีที่ 1

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f249d9f9-ea60-4361-b41b-340da516c7d9" />

ภาพที่ 2

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b79d28cd-ab0b-4e20-b8a1-21ba273c007c" />

ภาพที่ 3

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/79a2d38a-7995-4970-b868-90bc5bf154be" />

ภาพที่ 4

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b5315a44-1e36-4c92-9283-062153117a6b" />

ภาพที่ 5

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7de1255d-55cd-4e54-8ee7-1853797849cc" />

ภาพที่ 6

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e16782bf-9789-4894-bf34-8dc37a67504f" />

ภาพที่ 7

## วิธีที่ 2

ในวิธีที่ 2 ก็มีทางเลือกอีก 2 วิธี

### 2.1

นี่คือ process ที่เราใช้ทั้งหมดใน 2.1
```
┌──(kali㉿kali)-[~/Downloads/isusgrace03]
└─$ base64 -d enc_flag.txt | base64 -d | base64 -d
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aTwpSRlV4VGpKV2FrMHlWamxEWnowOUNnPT0K

┌──(kali㉿kali)-[~/Downloads/isusgrace03]
└─$ base64 -d enc_flag.txt | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{XXXXX}
```

มาโฟกัสกันทีละจุด

```
┌──(kali㉿kali)-[~/Downloads/isusgrace03]
└─$ base64 -d enc_flag.txt | base64 -d | base64 -d
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aTwpSRlV4VGpKV2FrMHlWamxEWnowOUNnPT0K
```

ฉันสมมติว่าตัวฉันเองไม่รู้ว่ามันถูกเข้ารหัสซ้อนไว้กี่ชั้นนะ ในตัวอย่างนี้ฉันสั่งให้ถอดรหัส 3 ชั้น ปรากฏว่าตัว Flag ยังถูกเข้ารหัสไว้อีก เราสามารถเพิ่มคำสั่งไปได้อีก จนกว่า flag จะออก จะได้แบบนี้

```
┌──(kali㉿kali)-[~/Downloads/isusgrace03]
└─$ base64 -d enc_flag.txt | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{XXXXX}
```




### 2.2
```
┌──(kali㉿kali)-[~/Downloads/isusgrace03]
└─$ echo "WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aTwpSRlV4VGpKV2FrMHlWamxEWnowOUNnPT0K" | base64 -d
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZO
RFUxTjJWak0yVjlDZz09Cg==
                                                                                                       
┌──(kali㉿kali)-[~/Downloads/isusgrace03]
└─$ echo "Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZO
RFUxTjJWak0yVjlDZz09Cg==" | base64 -d | base64 -d                        
picoCTF{XXXXX}
```


# อธิบาย

โจทย์ข้อนี้มีลักษณะเป็น Base64 ที่ถูกเข้ารหัสซ้อนหลายชั้น
