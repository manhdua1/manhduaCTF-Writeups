# Blame Game
## Thông tin về bài

```text
Level: Easy
Tags: General Skills, browser_webshell_solvable, git
Author: JEFFERY JOHN

Description:
Someone's commits seems to be preventing the program from working. Who is it? You can download the challenge files here:

    challenge.zip

Hints:
1. In collaborative projects, many users can make many changes. How can you see the changes within one file?
2. Read the chapter on Git from the picoPrimer here.
3. You can use python3 <file>.py to try running the code, though you won't need to for this challenge.
```
Link bài: https://play.picoctf.org/practice/challenge/405?category=5&page=1
## Lời giải
Để xem những commit đã thay đổi 1 file, ta chỉ cần chạy: git log [tên_file]
```text
git log message.py                           □ 
commit 2466febd40004b9ca644ce924181d07e23dcfaeb
Author: picoCTF{@sk_th3_1nt3rn_cfca95b2} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:06 2024 +0000

    optimize file size of prod code

commit 05f26d123cde97b714aaae28ba8f18db3f385af5
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:06 2024 +0000

    create top secret project
```
Vậy là chúng ta đã có flag.