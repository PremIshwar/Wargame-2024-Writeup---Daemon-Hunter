# Wargames 2024 Writeup - DaemonHunter

## Introduction
Hi! This my writeup on my solves for Wargames 2024. I'm still quite new to CTF, so I did not get many solves. I still had fun participating and I can't wait to do the same next year!


## Forensic
### I Cant Manipulate People
This one is fairly simple, it's one pcap file. 
After inscpecting the pcap in Wireshark, when following the ICMP traffic, you can see that one character of the flag is located in ech packet.
Knowing this, we can write a tshark command to extract the data from the end of each ICMP packet

![image](https://github.com/user-attachments/assets/ae7c9faf-fab2-4be6-b3ad-da13631e5137)

Flag found!

### Unwanted Meow
We are presented with a SHREDDED file. 
View in HxD hex editor

![image](https://github.com/user-attachments/assets/d5888bfc-62c1-4695-a267-0050b42eb0bf)

According the maigc number, this is a jpg file
The hex is riddled with "meow"
We can do a simple search and replace for the word meow and replace it with nothing
NOTE: HxD didnt managed to get all the "meow", so I had to open the hex in VSCode and manually find some meows and remove them

![flag1](https://github.com/user-attachments/assets/6f21b78e-00f9-4442-867b-3fc16fbc1439)


## Misc
