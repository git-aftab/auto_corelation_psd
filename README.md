<h1>AUTO-CORRELATION-AND-PSD</h1>
<h2>Aim</h2>
Write a program for Autocorrelation and Power Spectral Density (PSD) of signals in Scilab and verify the Wiener–Khinchin relation.

<h2>Equipments Needed</h2>
Computer with Intel i3 processor (or higher)
Scilab software
<h2>Theory</h2>
The Wiener–Khinchin theorem states that:
The Power Spectral Density (PSD) of a wide-sense stationary random process is the Fourier Transform of its autocorrelation function.

<img width="466" height="74" alt="507396276-f7c7673b-e086-4231-b8b4-4a677a3f7d0c" src="https://github.com/user-attachments/assets/1cc85a0a-ae00-435b-bd60-2c22bf8a884c" />

This relationship bridges the time-domain correlation and frequency-domain power representations of a signal.


<h2>Algorithm</h2>
Load or Define the Signal: Input your time-domain signal.
Compute Autocorrelation: Calculate the autocorrelation function of the signal.
Compute Power Spectral Density (PSD):
Estimate the PSD using either:
Fourier Transform of the autocorrelation function, or
Methods like Welch’s periodogram.
Plot Results: Visualize both the autocorrelation function and PSD.

<h2>Procedure</h2>
Refer to the algorithm and write the code for the experiment.
Open Scilab on your system.
Type your code in a new editor.
Save the file.
Execute the code.
If any errors occur, debug and re-run the program.
Verify the generated waveform using tabulation and model waveform comparison.

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
Result:
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
