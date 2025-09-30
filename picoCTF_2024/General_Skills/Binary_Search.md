# Binary Search
## Thông tin về bài

```text
Level: Easy
Tags: picoCTF 2024, General Skills, shell, browser_webshell_solvable, ls
Author: JEFFERY JOHN

Description:
Want to play a game? As you use more of the shell, you might be interested in how they work! 

Binary search is a classic algorithm used to quickly find an item in a sorted list. 
Can you find the flag? You'll have 1000 possibilities and only 10 guesses.

Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, 
and forensics. Practicing the fundamentals manually might help you in the future when you have to 
write your own tools!

You can download the challenge files here:
challenge.zip

ssh -p 55705 ctf-player@atlas.picoctf.net
Using the password 83dcefb7. Accept the fingerprint with yes, and ls once connected to begin. 
Remember, in a shell, passwords are hidden!

Hints:
1. Have you ever played hot or cold? Binary search is a bit like that.
2. You have a very limited number of guesses. Try larger jumps between numbers!
3. The program will randomly choose a new number each time you connect. You can always try again, 
   but you should start your binary search over from the beginning - try around 500. 
   Can you think of why?
```
Link bài: https://play.picoctf.org/practice/challenge/442?category=5&page=1
## Lời giải
Dựa vào thông tin ở phần mô tả của bài toán, ta sẽ giải bằng thuật toán [Tìm kiếm nhị phân](https://wiki.vnoi.info/algo/basic/Binary-Search)
Ta kết nối bằng SSH và với số đoán ban đầu là 500:
```text
ssh -p 51682 ctf-player@atlas.picoctf.net                             ⌂ 12:06
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess:
```
Dựa vào số đã đoán trước đó và kết quả server trả, ta sẽ có thể đoán số tiếp theo. Nếu kết quả là higher, biên dưới sẽ là vừa đoán, nếu kết quả là lower, biên trên sẽ là số vừa đoán.  Số đoán tiếp theo sẽ là (biên dưới + biên trên) / 2.
```text
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Lower! Try again.
Enter your guess: 625
Lower! Try again.
Enter your guess: 562
Lower! Try again.
Enter your guess: 531
Lower! Try again.
Enter your guess: 515 
Higher! Try again.
Enter your guess: 523
Lower! Try again.
Enter your guess: 519
Lower! Try again.
Enter your guess: 517
Congratulations! You guessed the correct number: 517
Here's your flag: picoCTF{g00d_gu355_2e90d29b}
Connection to atlas.picoctf.net closed.
```
Và ta đã có flag