# 程式閱讀題
```
1.print("3*2*(17-4)")會印出甚麼結果:
(A)0   (B)90  (C)出現錯誤,無法印出  (D)3*2*(17-4)
答案是:D
("3*2*(17-4)"印出中間的數值)17-2)

2.print(3*8*(22-2))會印出甚麼結果:
(A)0   (B)480  (C)出現錯誤,無法印出  (D)3*8*(22-2)
答案是:B
(3*8*20)
3.print("abc""+""def""+""ghi")會印出甚麼結果:
(A)出現錯誤,無法印出   (B)abc+def+ghi (C)abc""+""def""+""ghi" (D)abcdef
答案是:B
(列印"A"==A" "+"==+ "B"==B)
print("abc"+"def"+"ghi")會印出甚麼結果:
(A)出現錯誤,無法印出   (B)abc+def+ghi  (C)abc""+""def"+""ghi"  (D)abcdefghi
答案是:D
("A"+"B"==AB)
5.底下程式執行後結果為何?
word = "arttarataaa"
print(word.replace("a", "z",3))
(A)出現錯誤,無法印出   (B)arttarataaa  (C)zrttzrztaaa (D)zrttzrztzzz
答案是:B
(前三個a替換成z)
6.底下程式執行後結果為何?
word = "arttarataaa"
print(word.replace("a", "z"))
(A)出現錯誤,無法印出   (B)arttarataaa  (C)zrttzrztaaa (D)zrttzrztzzz
答案是:D
7根據底下程式,下列敘述何者為非?[複選題]

names = ['你', '好']
index = 0

while index < len(names):
    name = names[index]
    print(name)
    index = index + 1
    
(A)len(names)=2  
(B)names[1]是 你 
(C)程式執行完後,index最後為2
(D)如果把條件改成 index > len(names),中index最後為2
答案是:A,D
```
# 程式設計題
```
for 迴圈(loop)的技巧
1.使用for 迴圈(loop)計算1+2+3+.....100
2.使用for 迴圈(loop)計算1+3+5+7.....+99
3.使用for 迴圈(loop)計算1*3*5*7.....*99

while 迴圈(loop)的技巧
3.使用for 迴圈(loop)計算1+2+3+.....100
4.使用for 迴圈(loop)計算1+3+5+7.....+99
```


# 程式設計題解答(有各種寫法,找寫最快的分數最高)

### 使用for 迴圈(loop)計算1+2+3+.....100
```
sum=0

for x in range(1,100):
  sum +=x
  
print(sum)
答案是:4950
```
### 使用for 迴圈(loop)計算1+3+5+7.....+99
```
sum=0

for x in range(1,99,2):
  sum +=x
  
print(sum)
答案是:2402
```
### 使用for 迴圈(loop)計算
```
1*3*5*7.....*99
答案是:
```
```
total=1

for x in range(1,99,2):
  total *=x
  
print(total)
答案是:27529213532835651545259729751524430639300973035816196098326553772152587890625
```
