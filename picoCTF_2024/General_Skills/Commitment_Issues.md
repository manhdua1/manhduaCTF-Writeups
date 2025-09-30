# Commitment Issues
## Thông tin về bài

```text
Level: Easy
Tags: General Skills, browser_webshell_solvable, git
Author: JEFFERY JOHN

Description:
I accidentally wrote the flag down. Good thing I deleted it! You download the challenge files here:
    challenge.zip

Hints:
1. Version control can help you recover files if you change or lose them!
2. Read the chapter on Git from the picoPrimer here
3. You can 'checkout' commits to see the files inside them
```
Link bài: https://play.picoctf.org/practice/challenge/411?category=5&page=1
## Lời giải
Dựa vào đề bài ta thấy tác giả để thêm flag vào đâu đó nhưng đã xóa mất và cập nhật lại git. Vì vậy nên ta sẽ quay lại commit đó.
```text
◄ 0s ◎ git log                                                             
commit 144fdc44b09058d7ea7f224121dfa5babadddbb9 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:25 2024 +0000

    remove sensitive info

commit 7d3aa557ff7ba7d116badaf5307761efb3622249
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:25 2024 +0000

    create flag

◄ 0s ◎ git checkout 7d3aa557ff7ba7d116badaf5307761efb3622249

Note: switching to '7d3aa557ff7ba7d116badaf5307761efb3622249'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 7d3aa55 create flag
                                                                                                                         
◄ 0s ◎ls                                                 
 message.txt
                                                                                                                         
◄ 0s ◎ cat message.txt                                                 
picoCTF{s@n1t1z3_be3dd3da}

```
Vậy là chúng ta đã có flag.