# Lab Report 3
---
## Streamline ssh Configuration
![lab3 1](https://user-images.githubusercontent.com/103228609/167335265-50759374-4527-4bee-9be2-09cfb391f5bd.png)
![lab3 2](https://user-images.githubusercontent.com/103228609/167336041-1cf4d47a-942b-449f-84a8-efaf1fe556f9.png)
![lab3 3](https://user-images.githubusercontent.com/103228609/167336050-4d8cca5e-d063-42e3-a0b2-0f3310f0f8b2.png)

I initially created and edited my config file in notepad since I simply created a text file. After removing the `.txt` from my text file, the config was able to work properly and I could login into my remote account with just the commmand `ssh ieng6`. I can also use commands such as scp which require the host name with a similar formatting, and also because it uses the ssh key-gen, I don't need a password.

## Setup Github Access from ieng6
![lab3 4](https://user-images.githubusercontent.com/103228609/167336568-bbd98dce-dc0a-4c29-884b-b15faee04753.png)
![lab3 5](https://user-images.githubusercontent.com/103228609/167336651-b6ff58f6-f2dc-4475-9f16-5dda4a3a526d.png)
![Lab3 6](https://user-images.githubusercontent.com/103228609/167341732-d6d710a9-b53b-4b13-a397-d32eada0bbbe.png)
[The Resulting Commit](https://github.com/A1yip/SkillDemonstration1/commit/178d2d64cc03195cf73b6f4917364e9f8b6c63b7)

To begin with, I went into my ssh course account, and then navigated to the `.ssh` directory and then created a new keygen there. After this I printed the contents of the public key using `cat id_rsa.pub` and then added they ssh key to my github account. After this I could push changes I made to a cloned repository from a remote account.

## Copying Whole Directories using `scp -r
![lab3 7](https://user-images.githubusercontent.com/103228609/167346067-bc5f8332-bb2f-4d27-8d4f-33cdc6d146c0.png)
![lab3 8](https://user-images.githubusercontent.com/103228609/167346076-975013f6-78f4-4e86-b750-98089d43dca7.png)
![lab3 9](https://user-images.githubusercontent.com/103228609/167346082-fe6ce92b-ce06-4011-b33e-270257f16483.png)

I was able to copy the entire directory from my local system to the remote system using the command `scp -r *.java *.md lib/ ieng6:markdown-parse`. After doing so, I could run the tests fine since all of the necessary libraries were also copied over. However, in order to run both the command to copy the entire directory as well as run the tests, I had to chance the `javac` and `java` commands in order to specify the version of java to run.
