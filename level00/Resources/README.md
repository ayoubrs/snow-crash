level00
pwd: level00

check files belonging to the group level00
in level00, use find while checking the files content using xargs +  discard errors

find / -group level00 -type f 2>/dev/null | xargs file | grep -vi 'error\|link'

a trick learned in the video: [Linux Essentials for Ethical Hackers min 1:23:33](https://youtu.be/1hvVcEhcbLM)

files were empty ( ex-cammand | grep -v 'empty')

in the intra video there is a cat of a file content (README) instructs us to ==FIND== a file belonging to flag00 

```
cat README
    FIND this first file who can run only as flag00...
```

same command applied to groupe flag00
result: 
`/usr/sbin/john:      ASCII text`

`cat /usr/sbin/john` ==> cdiiddwpgswtgt

[Cipher Identifier](https://www.dcode.fr/cipher-identifier) ==>  [ROT Cipher](https://www.dcode.fr/rot-cipher) (ROT11) ==> `nottoohardhere`

su flag00

getflag

Here is your token : **x24ti5gi3x0ol2eh4esiuxias**

`su level01`
