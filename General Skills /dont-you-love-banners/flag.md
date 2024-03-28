![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/4e3cd800-5278-4986-bdf5-da2104683541)

To start this challenge off.. go to your shell and enter `nc tethys.picoctf.net [port number]` in the command line and this is what should pop up

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/41501823-d227-4376-8e62-cbef0a4ca2e7)


Then exit the instance with **Ctrl + Z**

Now enter `nc tethys.picoctf.net [Second provided port number]` in the command line and you should be met with this

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/3c0c6dd0-4835-44c8-a120-a5b59c8515c3)

Enter the password provided from the last netcat, which is **My_Passw@rd_@1234**

From there on you should be met with two questions.

The answer to the first one is **DEFCON**, and the answer to the second one is **JOHN**

Like this

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/b44a3664-6aad-4c88-9588-fd3ad79dce6b)

You are now successfully in the instance, from there on you want to remove the banner file in your home directory by entering `rm banner` in the command line

After doing that enter `cd /root` in the command line and then enter `ls` and you'll see this 

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/a5d72cae-8f6a-49ed-9879-634cab3ef27e)

Now enter `cd /home/player` into the command line to return to the home directory 

Create a symbolic link to flag.txt that was in the root directory, by entering `ln -s /root/flag.txt banner` into the command line

Now exit the instance with **Ctrl + Z** 

After that restart instance, **UP ARROW** in the command line should take you back to it and then hit enter

Enter everything you did previously again, such as the password and answers 

![image](https://github.com/berdies/PicoCTF-2024/assets/132856091/79ff1b12-84f6-473e-9502-2959ba23c5a3)

Once you restart the instance, there should be your flag 🥳




