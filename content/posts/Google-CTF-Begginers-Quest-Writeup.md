---
title: "Google CTF Begginers Quest Writeup"
date: 2021-09-02T19:13:48+02:00
draft: false
---

## How I spent definitely too much time on an begginer capture the flag.
Last weekend,while scrolling twitter I saw the post about Google CTF. Of course I am not qualified to solve it, I clearly do not have much needed experience with such competitions and programming as a whole. After checking it out I stumbled upon an ["Google CTF begginers quest"](https://capturetheflag.withgoogle.com/beginners-quest "CTF") and tasks here looked like they were not that hard.

## Just secret agent things
So after my introduction to my new role as a spy I quickly grabbed a friend and we started to get going with the first task.

## Novosibirsk - CTTV hacking
First we were tasked with, breaking into a monitoring system of some super secret facility, secured by famous cybersecurity company "YesWeAreSecure™". First thing I done was viewing the source code and look what I found, a javacript that checks the password. ![](/source-cctv.png)

Then I concluded that the numbers in the starting with 52xx were ASCII characters and all left to do was to substract 0xCafe from that. The password I got was 
```
GoodPassword
```
which took me to the page with the flag:
```
CTF{IJustHopeThisIsNotOnShodan}
```
