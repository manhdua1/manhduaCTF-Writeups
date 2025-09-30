# Collaborative Development
## Thông tin về bài

```text
Level: Easy
Tags: General Skills, browser_webshell_solvable, git
Author: JEFFERY JOHN

Description:
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together? You can download the challenge files here:

    challenge.zip

Hints:
1. git branch -a will let you see available branches
2. How can file 'diffs' be brought to the main branch? Don't forget to git config!
3. Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.
```
Link bài: https://play.picoctf.org/practice/challenge/410?category=5&page=1
## Lời giải
Ta kiểm tra file flag.py ở trong branch main nhưng chỉ có lệnh in chứ không có flag nên ta suy nghĩ ra flag nằm trong nhiều branch khác nhau do tên đề bài và mô tả. Ta chỉ cần ghép những phần của flag lại với nhau.
```text
◄ 0s ◎ git branch                                              
  feature/part-1
  feature/part-2
  feature/part-3
* main
                                                                                               
◄ 0s ◎ git checkout feature/part-1                               
Switched to branch 'feature/part-1'
                                                                                               
◄ 0s ◎ cat flag.py                                  
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')⏎                                                                                                                                                           
◄ 0s ◎ git checkout feature/part-2                  
Switched to branch 'feature/part-2'
                                                                                               
◄ 0s ◎ cat flag.py                                  
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')⏎                                                                                                                                                            
◄ 0s ◎ git checkout feature/part-3                  
Switched to branch 'feature/part-3'
                                                                                               
◄ 0s ◎ cat flag.py                                  
print("Printing the flag...")

print("w0rk_2c91ca76}")
```
Vậy là chúng ta đã có flag.