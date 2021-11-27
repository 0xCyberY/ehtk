## List of Cheat Sheets

1. [Penetration Testing Tools Cheat Sheet](https://highon.coffee/blog/penetration-testing-tools-cheat-sheet/#snmpv3-enumeration-tools)
2. [Pentest Book](https://pentestbook.six2dez.com/)
3. [pentestmonkey](http://pentestmonkey.net/category/cheat-sheet)
4. [HAUSEC](https://hausec.com/pentesting-cheatsheet/)
5. [penetration-testing-cheat-sheet](https://github.com/ivan-sincek/penetration-testing-cheat-sheet#readme)
6. [Penetration Testing Cheat Sheet](https://awesomeopensource.com/project/ivan-sincek/penetration-testing-cheat-sheet)
7. [Windows Privilege Escalation Fundamentals](https://www.fuzzysecurity.com/tutorials/16.html)
8. [Basic Linux Privilege Escalation](https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/)
9. [Active Directory Kill Chain Attack & Defense](https://github.com/infosecn1nja/AD-Attack-Defense#privilege-escalation)
10. [Windows & Active Directory Exploitation Cheat Sheet and Command Reference](https://casvancooten.com/posts/2020/11/windows-active-directory-exploitation-cheat-sheet-and-command-reference/)


## DNS Enumeration

### nslookup and dig Command

|              nslookup                             |               dig                |
| ------------------------------------------------- | -------------------------------- |
| nslookup target.com                               | dig target.com +short            |
| nslookup type= PTR target.com                     | dig target.com PTR               |
| nslookup type= MX target.com                      | dig target.com MX                |
| nslookup type= NS target.com                      | dig target.com NS                |
| nslookup > server target.com > ls d target.com    | dig axfr @target.com target .com |