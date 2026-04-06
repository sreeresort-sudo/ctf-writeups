# CTF Portfolio

สร้างโดยนักเรียนไทย ม.2 ที่กำลังเรียน CTF และ Cybersecurity

---

## โจทย์ที่ผ่านแล้ว

### picoCTF - Piece by Piece
**Category:** General Skills | **Difficulty:** Easy

**โจทย์:** ไฟล์ถูกตัดออกเป็นหลายชิ้น ต้องรวมกันแล้วแตกไฟล์เพื่อหา flag

**วิธีแก้:**
1. SSH เข้าเซิร์ฟเวอร์
2. รวมไฟล์ด้วย cat
3. แตกไฟล์ zip ด้วย unzip
4. อ่าน flag.txt

**คำสั่งที่ใช้:**
ssh ctf-player@dolphin-cove.picoctf.net -p XXXXX
cat part_aa part_ab part_ac part_ad part_ae > flag.zip
unzip flag.zip
cat flag.txt

---

### picoCTF - MY GIT
**Category:** General Skills | **Difficulty:** Easy

**โจทย์:** Clone repository แล้ว push flag กลับไป

**วิธีแก้:**
1. git clone repository
2. ตั้งค่า git config
3. สร้าง flag.txt
4. git add, commit, push

**คำสั่งที่ใช้:**
git clone ssh://git@foggy-cliff.picoctf.net:53109/git/challenge.git
git config user.name "root"
git config user.email "root@picoctf"
touch flag.txt
git add flag.txt
git commit -m "flag"
git push

---

### picoCTF - Printer Shares
**Category:** General Skills | **Difficulty:** Easy

**โจทย์:** มีคนส่งไฟล์ไปเครื่องพิมพ์ผิด ให้ดึงไฟล์กลับมา

**วิธีแก้:**
1. เชื่อมต่อเซิร์ฟเวอร์ด้วย nc
2. ดึงข้อมูลจาก print server

**คำสั่งที่ใช้:**
nc mysterious-sea.picoctf.net XXXXX

---

### picoCTF - Undo
**Category:** General Skills | **Difficulty:** Easy

**โจทย์:** ย้อนกลับการแปลงข้อความ Linux หลายๆ อย่างเพื่อกู้ flag

**วิธีแก้:**
1. เชื่อมต่อด้วย nc
2. ถอดรหัส base64
3. กลับข้อความด้วย rev
4. แทนที่ตัวอักษรด้วย tr

**คำสั่งที่ใช้:**
nc foggy-cliff.picoctf.net XXXXX
base64 -d
rev
tr '-' '_'
---

## Linux Commands

| คำสั่ง | ความหมาย |
|--------|----------|
| pwd | ดูว่าอยู่ที่ไหน |
| ls | ดูไฟล์และโฟลเดอร์ |
| cd | เข้าโฟลเดอร์ |
| cd .. | ออกไปชั้นบน |
| mkdir | สร้างโฟลเดอร์ |
| cat | อ่านไฟล์ทุกอย่าง |
| echo > ไฟล์ | เขียนทับ |
| echo >> ไฟล์ | เพิ่มต่อท้าย |
| rm | ลบไฟล์ถาวร |
| rm -r | ลบโฟลเดอร์ถาวร |
| file | บอกความจริงของไฟล์ |
| strings | อ่านไฟล์ไม่รวมขยะ |
| grep | ค้นหาข้อความในไฟล์ |
| xxd | แปลงไฟล์เป็น Hex |
| wget | ดาวน์โหลดไฟล์จาก link |
| nc | เชื่อมต่อเซิร์ฟเวอร์ |
| base64 -d | ถอดรหัส Base64 |
| rev | กลับข้อความ |
| tr | แทนที่ตัวอักษร |

---

## Git Commands

| คำสั่ง | ความหมาย |
|--------|----------|
| git clone | โหลดโปรเจคจากเซิร์ฟเวอร์ |
| git log | ดูประวัติการแก้ไข |
| git add | เลือกไฟล์ที่จะบันทึก |
| git commit -m | บันทึกพร้อมข้อความ |
| git config | ตั้งค่าชื่อและอีเมล |
| git push | ส่งไฟล์ขึ้นเซิร์ฟเวอร์ |

---

## Python สำหรับ CTF

### ord() และ chr()
- ord() → แปลงตัวอักษรเป็นเลข
- chr() → แปลงเลขเป็นตัวอักษร

### Caesar Cipher
เข้ารหัสโดยเลื่อนตัวอักษรตาม shift
ถอดรหัสด้วย Brute Force ลองทุก shift 1-25

### ROT13
Caesar Cipher shift 13

### Base64
แปลงข้อความเป็นตัวอักษรพิเศษ
ลงท้ายด้วย = หรือ ==

### Hex Encoding
แปลงข้อความเป็น hex
---

## ความสามารถ

### Cybersecurity
- ทำ CTF สาย General Skills และ Cryptography
- ใช้ Linux Terminal ได้คล่อง
- เข้าใจการเข้ารหัสพื้นฐาน เช่น Caesar Cipher, Base64, Hex

### Programming
- Python ระดับเริ่มต้น-กลาง
- เขียนโปรแกรมถอดรหัสได้เอง
- โปรเจคที่ทำแล้ว: เครื่องคิดเลข, เกมทายตัวเลข, สมุดบันทึก, Voice Assistant

### Linux
- ใช้ Ubuntu เป็นประจำ
- รู้คำสั่งพื้นฐานและคำสั่ง CTF ครบ

### Tools
- picoCTF
- PyCharm
- GitHub
- Linux Terminal
- ---

## เป้าหมาย

- สอบเข้า KVIS หรือ MWIT (ม.4)
- แข่ง CTF ระดับประเทศและนานาชาติ
- เรียนมหาวิทยาลัยด้าน Cybersecurity

---

## ติดต่อ

- GitHub: github.com/sreeresort-sudo
- picoCTF: sreeresort
