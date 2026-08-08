EXPT 2a: LINEAR CONVOLUTION-USING-DFT
AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED
PC installed with SCILAB

PROGRAM:
LINEAR CONVOLUTION
```
clc;
clear;
x = [1 1 1 1];
h = [1 2 3 4];
m = length(x);
n = length(h);
a=0:1:m-1;
b=0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1: n+m-1
conv_sum = 0;
for j = 1:i
if (((i-j+1) <= n)&(j <=m))
conv_sum = conv_sum + x(j)*h(i-j+1);
end;
y(i) = conv_sum;
end;
end;
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');

```




### CALCULATIONS:
<img width="858" height="1600" alt="WhatsApp Image 2026-08-08 at 06 52 46" src="https://github.com/user-attachments/assets/3f4a55d4-7c5c-470d-98ff-73cfe624dafb" />
<img width="791" height="1282" alt="WhatsApp Image 2026-08-08 at 06 51 21" src="https://github.com/user-attachments/assets/1da495ec-2639-4eac-9027-7b389419c22a" />




### SAMPLE OUTPUT:

<img width="757" height="597" alt="Screenshot 2026-07-28 090026" src="https://github.com/user-attachments/assets/a18b521f-a6b7-4a49-ba5b-4d1ecdf2cdc3" />




RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
