# The Internship Season 4 : Developer Exam
# [ตอนที่ 1]
ให้ผู้สมัครเขียนโปรแกรมต่อไปนี้โดยใช้ภาษาโปรแกรมอะไรก็ได้ (สามารถเลือกภาษาในการเขียนโปรแกรมได้ตามต้องการ เลือกได้มากกว่า 1 ภาษา แต่ไม่ เกิน 3 ภาษา/ข้อ)

## โปรแกรมที่ 1
เขียนโปรแกรมที่รับข้อความจาก Command Line Argument 2 ข้อความ โดยข้อความที่ 1 มีค่าเป็น vowel / alphabet (ไม่นับตัวที่เป็นสระ) / digit / lowercase / uppercase อย่างใดอย่างหนึ่ง
ข้อความที่ 2 เป็น alphanumeric
และแสดงจำนวนตัวอักษร ในข้อความที่ 2 ตามที่ข้อความที่ 1 กำหนด ทาง Standard Output

ตัวอย่างการรันโปรแกรม

```
> count vowel Rawitat
3
```

```
> count alphabet Rawitat
4
```

```
> count digit Rawitat
0
```

```
> count lowercase Rawitat
6
```

```
> count uppercase Rawitat
1
```

## โปรแกรมที่ 2
เขียนโปรแกรมที่รับข้อความจาก Command Line Argument 2 ข้อความ โดยข้อความที่ 1 เป็นตัวเลข ข้อความที่ 2 เป็นรูปแบบใดๆ
และแสดงข้อความที่ 1 ตามรูปแบบในข้อความที่ 2 ทาง Standard Output

ตัวอย่างการรันโปรแกรม

```
> formatter 0912345678 xxx-xxx-xxxx
091-234-5678
```

```
> formatter 1234567890123 x-xxxx-xxxxx-xx-x
1-2345-67890-12-3
```

# [ตอนที่ 2]
ให้ผู้สมัคร **“ปรับปรุงคุณภาพของโค้ด”** โปรแกรมเก่า ซึ่งโปรแกรมเมอร์ในอดีตของบริษัทหนึ่งเขียนด้วยภาษา C (C99) ต่อไปนี้โดย ให้ **“ปรับปรุงให้ดีที่สุดเท่าที่จะทำได้”** โดยผู้สมัครสามารถเขียนใหม่เป็นภาษาที่ผู้สมัครถนัดก็ได้ (โดยผู้สมัครจะต้อง **“เดา”** วัตถุประสงค์รวมถึงขอบเขตต่างๆ ของโปรแกรมนี้เอง ... เนื่องจากโปรแกรมเมอร์ที่เขียนโปรแกรมนี้ได้ลาออกไปแล้ว) ทั้งนี้ผู้สมัครสามารถถือได้ว่า **“โปรแกรมเหล่านี้ทดสอบแล้วว่าไม่มีข้อผิดพลาด (Bug) และสามารถทำงานได้ตามวัตถุประสงค์/ขอบเขตการทำงานอยู่แล้ว”** (ปรับปรุงคุณภาพโค้ดอย่างเดียว ไม่ต้องหาหรือแก้ข้อผิดพลาด)

```c
#include<stdio.h>
#include<stdlib.h>
#include<stdbool.h>
int n;
bool prime[1000000];
void delete(int i) 
{
    for (int index = i + 1; index <= n; ++index) 
    {
        if (index % i == 0) 
        {
            prime[index] = false;
        }
    }
}

//ไม่ได้ใช้แล้วค่ะ
int show_prime() {
    
    
    return 0;
}

int main(int argc, char* argv[]) {
  n = atoi(argv[1]);
  
  for(int i=2;i<=n;i+=1){
      prime[i] = true;
  }
  for(int i=2;i<=n; i++){
	if (prime[i]==true) delete(i);
  }
  
  // โชว์ค่าoutput
  for(int i=2;i<=n;i++) {
	if (prime[i]==true){
	    printf("%d " , i);
	}
  }
	
  return 0;
}
```

# [ตอนที่ 3]
ให้ผู้สมัคร “เลือก” โค้ดโปรแกรม ที่ผู้สมัครเคยเขียน มา 1 ไฟล์ เช่น my_program.c, my_program.js, MyProgram.java, my_program.rb, my_program.py
โดยให้เป็นโค้ดที่ผู้สมัครเขียนเองทั้งหมดไม่มีส่วนที่คัดลอกจากหนังสือ เว็บไซต์เอกสารประกอบการสอน ฯลฯ ใดๆ ทั้งสิ้น ไม่จำเป็นว่าต้องเป็นไฟล์ใหญ่หรือโปรแกรมที่ยาก

# การส่งคำตอบ
1. ให้ผู้สมัครแยกคำตอบทั้ง 3 ตอน ลงใน 3 Folders (Directory) โดยตั้งชื่อ Folder เป็น 1, 2 และ 3 ตามลำดับ
2. ชื่อไฟล์ในแต่ละตอนให้ตั้งตามความเหมาะสม เช่น program1.c, program1.js, Count.java, count.rb, count.py เป็นต้น
3. เตรียมไฟล์ชื่อ Readme.txt ที่ระบุชื่อ เบอร์โทรศัพท์ e-mail ไว้ในไฟล์โดยเตรียมไฟล์นี้ไว้นอก Folder ทั้ง 3
4. ZIP ทั้งโฟลเดอร์กับไฟล์ Readme.txt โดยตั้งชื่อ Internship2018.zip (ย้ำ: ZIP เท่านั้น ห้าม RAR)
5. Submit ในระบบ หรือส่งไฟล์ตามที่ระบุในเว็บไซต์

ตัวอย่าง Folder Structure ที่มี Readme.txt ด้วย

![Folder Structure](https://github.com/theinternship-program/The-Internship-2018-Developer-Exam/blob/master/folder-structure.png?raw=true)