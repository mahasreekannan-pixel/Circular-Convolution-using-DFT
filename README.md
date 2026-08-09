# EXPT 2B:CIRCULAR-CONVOLUTION-USING-DFT
## AIM
To perform and verify circular convolution operation of two given sequences using SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM:
## CIRCULAR CONVOLUTION
<br>
<br>clc; 
<br>clear;
<br>x=[1 1 1 1];
<br>n1=0:1:length(x)-1;
<br>subplot(3,1,1);
<br>plot2d3(n1,x);
<br>xlabel('time');
<br>ylabel('amplitude');
<br>title('input sequence');
<br>h=[1 2 3];
<br>n2=0:1:length(h)-1;
<br>subplot(3,1,2);
<br>plot2d3(n2,h);
<br>xlabel('time');
<br>ylabel('amplitude');
<br>title('impulse sequence');
<br>N1=length(x);
<br>N2=length(h);
<br>N=max(N1,N2);
<br>N3=N1-N2;
<br>if(N3>0)
<br>h=[h,zeros(1,N3)];
<br>else
<br>x=[x,zeros(1,abs(N3))];
<br>end
<br>disp(x)
<br>disp(h)
<br>for n=1:N
<br>y(n)=0;
<br>for i=1:N
<br>j=n-i+1;
<br>if(j<=0)
<br>j=N+j;
<br>end
<br>y(n)=y(n)+x(i)*h(j);
<br>end
<br>end
<br>disp(y)
<br>n=0:N-1;
<br>subplot(3,1,3);
<br>plot2d3(n,y);
<br>xlabel('time');
<br>ylabel('amplitude');
<br>title('circular convolution');


<br>
**CALCULATIONS:
**<br>
<br><img width="957" height="1600" alt="image" src="https://github.com/user-attachments/assets/2e5a753f-323e-4da4-8d5d-73d05f0228cd" />

<br>
<br>
<br>
** SAMPLE OUTPUT:
**<br>
<br><img width="856" height="733" alt="image" src="https://github.com/user-attachments/assets/5603c2ae-0135-44a2-b372-eeabecf4ddd8" />

<br>
<br>



## RESULT:
Thus, the circular convolution of the two given sequences were performed and its result was verified.


