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
<img width="900" height="1600" alt="WhatsApp Image 2026-08-08 at 08 15 04" src="https://github.com/user-attachments/assets/83aa5bd6-ce23-49d3-b5dc-3a0e1a96a28b" />

<img width="1080" height="1108" alt="WhatsApp Image 2026-08-08 at 08 15 18" src="https://github.com/user-attachments/assets/6178d899-ef6a-4ba3-a719-286eb0b62c4f" />


### SAMPLE OUTPUT:
<img width="757" height="597" alt="WhatsApp Image 2026-08-08 at 08 19 39" src="https://github.com/user-attachments/assets/2a27f6e5-da5e-4904-9689-d5f2512e1e02" />





RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
