# CTF Writeups

## picoCTF - Piece by Piece

**Category:** General Skills  
**Difficulty:** Easy  

### โจทย์
ไฟล์ถูกตัดออกเป็นหลายชิ้น ต้องรวมกันแล้วแตกไฟล์เพื่อหา flag

### วิธีแก้
1. SSH เข้าเซิร์ฟเวอร์
2. รวมไฟล์ด้วย cat
3. แตกไฟล์ zip ด้วย unzip
4. อ่าน flag.txt

### คำสั่งที่ใช้
ssh ctf-player@dolphin-cove.picoctf.net -p XXXXX
cat part_aa part_ab part_ac part_ad part_ae > flag.zip
unzip flag.zip
cat flag.txt
### Flag
picoCTF{...}
