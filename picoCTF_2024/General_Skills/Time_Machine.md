# Time Machine
## Thông tin về bài

```text
Level: Easy
Tags: General Skills, browser_webshell_solvable, git
Author: JEFFERY JOHN

Description:
What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:
challenge.zip

Hints:
1. The cat command will let you read a file, but that won't help you here!
2. Read the chapter on Git from the picoPrimer here.
3. When committing a file with git, a message can (and should) be included.
```
Link bài: https://play.picoctf.org/practice/challenge/425?category=5&page=1
## Lời giải
Dựa vào thông tin ở hint 3, là khi commit 1 file với git, có thể đính kèm một message. Nên ta sẽ thử xem lịch sử commit vì có thể flag sẽ ở đó.
```text
git log
commit e65fedb3a72a16c577f4b17023b63997134b307d (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:29 2024 +0000

    picoCTF{t1m3m@ch1n3_88c35e3b}
```
Vậy là chúng ta đã có flag.