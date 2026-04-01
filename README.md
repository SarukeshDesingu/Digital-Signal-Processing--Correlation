# Digital-Signal-Processing--Correlation
## AIM:
To generate discrete auto correlation and cross correlation of signals using MATLAB.
## APPARATUS REQUIRED:
MATLAB R2012.
## ALGORITHM:
Step 1: Open matlab. Write the program.

Step 2: Read the input sequence 1 and input sequence 2 sequence.

Step 3: Perform auto correlation and cross correlation for both the sequences. 

Step 4: Plot the output sequence with x-label and y-label with suitable title.

Step 5: Terminate the program.


## PROGRAM: 
```
clc;
clear all;
close all;

% INPUT SIGNAL-1
a = input('enter the starting x(n)');
x = input('Enter the x(n) sequence');
n = a : 1 : length(x) + a - 1;
figure(1)
stem(n,x)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-1')

% INPUT SIGNAL-2
b = input('enter the starting y(n)');
y = input('Enter the y(n) sequence');
m = input('enter the ending y(n)');
n1 = b : 1 : length(y) + b - 1;
figure(2)
stem(n1,y)
xlabel('Time')
ylabel('Amplitude')
title('Input signal-2')

% DISCRETE AUTO CORRELATED SIGNAL
Out1 = xcorr(x,x);
n2 = a - m : 1 : length(Out1) + a - m - 1;
figure(3)
stem(n2,Out1)
xlabel('Time')
ylabel('Amplitude')
title('Discrete auto correlated waveform')

% DISCRETE CROSS CORRELATED SIGNAL
Out2 = xcorr(x,y);
n3 = a - m : 1 : length(Out2) + a - m - 1;
figure(4)
stem(n3,Out2)
xlabel('Time')
ylabel('Amplitude')
title('Discrete cross correlated waveform')
```
## OUTPUT:

### INPUT SIGNAL-1:
<img width="705" height="629" alt="image" src="https://github.com/user-attachments/assets/1140edb4-32da-4163-9864-e953529fa966" />

### INPUT SIGNAL-2:
<img width="706" height="627" alt="image" src="https://github.com/user-attachments/assets/d46902c1-d9e2-4814-a4c4-c3d4e2f8c73f" />

### DISCRETE AUTO CORRELATED :
<img width="702" height="630" alt="image" src="https://github.com/user-attachments/assets/46f77c9d-6631-4a69-b8b8-bcb5cb5e1618" />

### DISCRETE CROSS CORRELATED :
<img width="702" height="626" alt="image" src="https://github.com/user-attachments/assets/e7d3c853-c775-471e-8f9f-fe832ae31de5" />

## RESULT:
<img width="1600" height="802" alt="image" src="https://github.com/user-attachments/assets/6812539d-4bbf-4e9b-88fe-e673e5ac1be3" />



