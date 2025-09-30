# binhexa
## Thông tin về bài

```text
Level: Easy
Tags: General Skills, browser_webshell_solvable
Author: Nana Ama Atombo-Sackey

Description:
How well can you perfom basic binary operations? Start searching for the flag here nc titan.picoctf.net 49538

Hints: None
```
Link bài: https://play.picoctf.org/practice/challenge/404?category=5&page=1
## Lời giải
Bài này bắt chúng ta phải thực hiện 6 phép toán nhị phân. Phép 1 là phép AND bits (&), kết quả chỉ bằng 1 khi cả 2 bit bằng 1. Phép 2 là phép dịch trái bits (<<), ta mang tất cả các bit dịch sang trái 1 ô, ô phải ngoài cùng sẽ là bit 0. Phép 3 là phép OR bits (|), kết quả chỉ bằng 0 khi cả 2 bit bằng 0. Phép 4 là nhân nhị phân, ta chỉ cần đổi 2 số sang thập phân sau đó nhân rồi lại chuyển kết quả sang số nhị phân. Phép thứ 5 là cộng nhị phân, ta cộng như số thập phân bình thường. Phép thứ sau là dịch phải (>>), ta chỉ cần bỏ số ở cuối đi. Cuối cùng bài toán bắt ta chuyển phép thứ 6 sang số hexa.
```text
nc titan.picoctf.net 51482

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01000100
Binary Number 2: 00111001


Question 1/6:
Operation 1: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0
Correct!

Question 2/6:
Operation 2: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10001000
Correct!

Question 3/6:
Operation 3: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1111101
Correct!

Question 4/6:
Operation 4: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1111101
Incorrect. Try again
Enter the binary result: 111100100100
Correct!

Question 5/6:
Operation 5: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1111101     
Correct!                                                                     
                                                                             
Question 6/6:                                                                
Operation 6: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 11100
Correct!

Enter the results of the last operation in hexadecimal: 1C

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_6ab1ad84}
```
Vậy là chúng ta đã có flag.