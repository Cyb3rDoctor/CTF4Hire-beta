# OSINT - Caroline Shirley

## Challenge description:

![Caroline Shirley](https://user-images.githubusercontent.com/70543460/102475341-6925f500-4062-11eb-853f-b1007b689b20.png)

<br/><br/>

## Solution:

According to the description, we need to find someone called "Caroline Shirley" somewhere on the internet...

I noticed something interesting in the challenge description, which might be an embedded hint:

![image](https://user-images.githubusercontent.com/70543460/102476055-4f38e200-4063-11eb-99b6-ee61a31e1898.png)

So, I searched for **"Caroline Shirley"** in LinkedIn, then I checked a lot of profiles with that name, and this one was very suspicous:

https://www.linkedin.com/in/caroline-shirley-a4a1931ba/

![image](https://user-images.githubusercontent.com/70543460/102476826-35e46580-4064-11eb-844a-82a85435359d.png)

<br/><br/>

The profile summary was interesting...

![s](https://user-images.githubusercontent.com/70543460/102477346-e9e5f080-4064-11eb-937d-d827e5a9c6cc.png)

Hmmm... Something I like? A flag? 😂

<br/><br/>

I downloaded her resume from her profile:

![image](https://user-images.githubusercontent.com/70543460/102477545-2b769b80-4065-11eb-9f79-177ef58a3238.png)

Then I checked that pdf file, but there was nothing interesting, so I started analyzing it to find something hidden...

First of all, I checked the metadata:

![image](https://user-images.githubusercontent.com/70543460/102479147-303c4f00-4067-11eb-9432-8e7cb3183f1b.png)

The most interesting thing was: **"cairo 1.16.0 (https://cairographics.org)"**

So, I opened that link and started reading to figure out what was that:

![image](https://user-images.githubusercontent.com/70543460/102479971-51ea0600-4068-11eb-8c15-b4134b4820aa.png)

Then I checked the documentaion to find how the PDF files are rendered with cairo:

![image](https://user-images.githubusercontent.com/70543460/102480318-c624a980-4068-11eb-9366-85b59dc357a8.png)

Then I read about PS files:

![image](https://user-images.githubusercontent.com/70543460/102492762-d180d080-407a-11eb-8873-b06b099daba2.png)

I saved **pdftops.c** and compiled it, then I used it to convert that PDF tile to a PS file:

![image](https://user-images.githubusercontent.com/70543460/102490736-e871f380-4077-11eb-8c1e-107f7782828d.png)

Then I opened the output file (**output.ps**) with Adobe Illustrator:

![image](https://user-images.githubusercontent.com/70543460/102492080-caa58e00-4079-11eb-9721-e40fc17bc171.png)

I noticed something intersting in the layers:

![image](https://user-images.githubusercontent.com/70543460/102492246-15270a80-407a-11eb-9970-d54d2cd02547.png)

And that was the flag!

![image](https://user-images.githubusercontent.com/70543460/102492506-73ec8400-407a-11eb-81e5-01ca36e2dbb4.png)

<br/><br/>

## flag{f12945ed35f153ecb4de9006a7f2132c}
