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
x = [1 1 1 0];
h = [1 0 1 0];
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

<img width="1441" height="1600" alt="image" src="https://github.com/user-attachments/assets/945643b9-693a-4432-bea3-ac8f2018eb64" />



### SAMPLE OUTPUT:
<img width="597" height="568" alt="image" src="https://github.com/user-attachments/assets/ef69623b-a878-413c-9b38-d462231a0eca" />





RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
