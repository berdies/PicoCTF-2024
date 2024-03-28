![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/db78114c-fbbe-422e-b8c3-d898bed744c1)

To start this challenge off you'll want to launch your instance

You are provided a netcat, go to your shell enter the provided netcat into your command line, like this `nc titan.picoctf.net [port number]` and you should be met with this

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/e600d1b5-5dbd-4e03-b701-f863c731efbb)

My process for the conversion is a bit lengthy so bare with me...

For starters, I converted the ASCII text into Hex, you can do this per a ASCII to Hex calculator such as: https://www.rapidtables.com/convert/number/ascii-to-hex.html (use no spaces for conversion)

You'll then want to convert the Hex into its Little Endian representation. I did this by using the following python script

```python
hex_num = b'[YOUR HEX CODE]'
big = bytearray.fromhex(str(hex_num, 'utf-8'))
big.reverse()
little = ''.join(f"{n:02X}" for n in big)
print(little)
```

I compiled the code using a online python compiler such as https://www.programiz.com/python-programming/online-compiler/

Heres what the conversion should look like if you compile the script per the online python compiler

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/e55ca6e2-5017-44ac-a43d-657e2dfb5fa4)

Now copy the result you got, go back to your shell, and paste your result **Ctrl+Shift+V** like this

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/ae313488-d7ca-41af-869e-882ea71d3436)

Now for the last step, converting the Little Endian representation into Big Endian.

I converted the two by using the following website https://blockchain-academy.hs-mittweida.de/litte-big-endian-converter/ 

(Complete the conversion for Hexal instead of Binary)

You'll want to paste your Little Endian representation into the box for Little Endian, and immediately the Big Endian representation should pop up. Like this..

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/e01f0e3b-ead3-48dd-98ab-af6bfd092abe)

Finally.. copy the Big Endian Representation, go back to your shell, and paste the result **Ctrl+Shift+V** into the prompt.. like this...

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/044fce43-5846-47b3-875c-e4cbb2c5f64c)

There you should finally have your flag🥳
