# Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib
## AIM

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. Apparatus Required
Software: Python with NumPy and Matplotlib libraries

## HARDWARE
Personal Computer

## THEORY

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of the message signal. The general form of an AM signal is:<img width="290" height="152" alt="image" src="https://github.com/user-attachments/assets/dbe771a4-4857-47ca-a3e3-c9e0559add09" />


## ALGORITHM

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Generate Carrier Signal: Define the carrier signal as a cosine wave.
5.	Modulate Signal: Apply the AM formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## PROGRAM
```
Ac = 14;     
Am = 7;      
fc = 6530;   
fm = 653;     
fs = 653000;  
t = 0:1/fs:2/fm; 
m = Am * cos(2 * 3.14 * fm * t);
c = Ac * cos(2 * 3.14 * fc * t);
s = (Ac + m) .* cos(2 * 3.14 * fc * t);
env = abs(hilbert(s));
m_demod = env - mean(env); 
figure;
subplot(4,1,1);
plot(t, m);
xlabel('Time (s)');
ylabel('Amplitude');
title('Message Signal');
subplot(4,1,2);
plot(t, c);
xlabel('Time (s)');
ylabel('Amplitude');
title('Carrier Signal');
subplot(4,1,3);
plot(t, s);
xlabel('Time (s)');
ylabel('Amplitude');
title('AM Modulated Signal');
subplot(4,1,4);
plot(t, m_demod);
xlabel('Time (s)');
ylabel('Amplitude');
title('Demodulated Signal');
```
## OUTPUT
![WhatsApp Image 2025-12-03 at 8 42 18 PM](https://github.com/user-attachments/assets/51da067c-fb10-4a42-aaf6-0107fb617bed)

## RESULT
![WhatsApp Image 2025-12-03 at 8 42 48 PM](https://github.com/user-attachments/assets/675f95b5-8035-4f2f-8104-7b1d16307bb8)
