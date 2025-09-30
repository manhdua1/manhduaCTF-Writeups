# Super SSH
## Thông tin về bài

```text
Level: Easy
Tags: General Skills, shell, ssh, browser_webshell_solvable
Author: JEFFERY JOHN

Description:
Using a Secure Shell (SSH) is going to be pretty important. Can you ssh as ctf-player to titan.picoctf.net at port 61321 to get the flag? You'll also need the password 84b12bae. If asked, accept the fingerprint with yes. If your device doesn't have a shell, you can use: https://webshell.picoctf.org If you're not sure what a shell is, check out our Primer: https://primer.picoctf.com/#_the_shell

Hints:
1. https://linux.die.net/man/1/ssh
2. You can try logging in 'as' someone with <user>@titan.picoctf.net
3. How could you specify the port?
4. Remember, passwords are hidden when typed into the shell
```
Link bài: https://play.picoctf.org/practice/challenge/424?category=5&page=1
## Lời giải
Bài này chỉ đơn giản là chạy secure shell vào port trên đề bài với user là ctf-player tới titan.picoctf.net.
```text
ssh -p 61321 ctf-player@titan.picoctf.net                             ⌂ 14:34
The authenticity of host '[titan.picoctf.net]:61321 ([3.139.174.234]:61321)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:4: [titan.picoctf.net]:64884
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:61321' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: flag.
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_07a987ac}
Connection to titan.picoctf.net closed.
```
Vậy là chúng ta đã có flag.