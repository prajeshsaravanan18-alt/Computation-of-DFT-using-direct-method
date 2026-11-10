# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
clc;
clear;
clf;

xn = [1,2,3,4,4,3,2,1];

N = length(xn);
n = 0:N-1;
j = %i;

Xk = zeros(1, N);

// Direct DFT calculation
for k = 0:N-1
    for r = 0:N-1
        Xk(k+1) = Xk(k+1) + ...
            xn(r+1)*exp(-j*2*%pi*k*r/N);
    end
end

disp("DFT output:");
disp(Xk);

K = 0:N-1;
magnitude = abs(Xk);
phase = atan(imag(Xk), real(Xk));

subplot(3,1,1);
plot2d3(n, xn);
xtitle("Input Sequence", "n", "x(n)");

subplot(3,1,2);
plot2d3(K, magnitude);
xtitle("Magnitude Spectrum", "k", "|X(k)|");

subplot(3,1,3);
plot2d3(K, phase);
xtitle("Phase Spectrum", "k", "Phase (radians)")
### CALCULATIONS:
<img width="1575" height="1600" alt="image" src="https://github.com/user-attachments/assets/1ba7a228-291d-4b3d-8677-aba1bcf12101" />
<img width="1000" height="1600" alt="image" src="https://github.com/user-attachments/assets/e1b405f4-0b8a-4aa6-94fe-70b3b31e6b24" />
<img width="1013" height="1600" alt="image" src="https://github.com/user-attachments/assets/b4fdb72c-1f5f-4974-a08f-8d387a54bf1a" />
<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/dc8e7b2d-c0ce-4be7-8c60-205490e54162" />

### SAMPLE OUTPUT:
<br>
<img width="1080" height="1378" alt="image" src="https://github.com/user-attachments/assets/1782c149-8700-4b9d-baaf-b6b049183e50" />

<br>



## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

