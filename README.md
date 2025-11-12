#Auto Corelation and PSD
#AIM

#Apparatus Required
Computer with i3 processor
Scilab

#Theory


#program
```
clc
clear all;
t = 0:0.01:2*3.14
x = tan(100*t);
subplot(3,2,1);
plot(x);

au = xcorr(x,x);
subplot(3,2,2);
plot(au);

v = fft(au);
subplot(3,2,3);
plot(abs(v));

fw = fft(x);
subplot(3,2,4);
plot(fw);

fw2 = (abs(fw)).^2;
subplot(3,2,5);
plot(fw2);

```

#Output Graph
<img width="1919" height="1198" alt="image" src="https://github.com/user-attachments/assets/49cfb41d-c5e7-44a8-80b5-3f6a3b8b4b48" />




``

