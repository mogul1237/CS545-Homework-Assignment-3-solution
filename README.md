# CS545-Homework-Assignment-3-solution

Download Here: [CS545 Homework Assignment 3 solution](https://jarviscodinghub.com/assignment/cs545-homework-assignment-3-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

1. (100 Points) This problem is to familiarize you with data filtering, by comparing a 2nd Order
Butterworth Filter with a Kalman Filter. The data in the file noisy.data was generated from
the following difference equations:
xn+1 = 0.5xn + 3.5un + ε x
yn = xn + ε y
(1)
where ε x ∼ N 0,σ2 ( x ), ε y ∼ N 0,σ2
( y ) are Gaussian noise variables. The file noisy.data contains 1000 observations of yn
, xn
,un ( ) from 1000 time steps of the system sampled at Δt = 0.01
seconds.
a) A second order Butterworth filter has the following mathematical form:
xf
n = b1yn + b2 yn−1 + b3yn−2 − a2 xf
n−1 − a3xf
n−2
where the subscript “f” denotes the filtered variable. The “butter” function in Matlab allows
you to generate the filter coefficients for a discrete Butterworth filter (try “help butter” in
Matlab). The function takes two arguments, the filter order and the cutoff frequency, expressed as a fraction of half of the sampling frequency, also called the Nyquist frequency.
The filter order will be “2” for a second order filter as described above, and our sampling
frequency is 100Hz. Calculate the filter coefficients b1,b2 ,b3,a2 ,a3 for a low pass filter with
cutoff frequency 5Hz. Provide a print-out of the coefficients.
b) Use the Matlab “filter” function and apply your filter to the yn data from noisy.data. Plot the
filtered, i.e., xf
n and the true, i.e., xn data on top of each other, provide the print-out, and
comment on the quality of the filter. Estimate the delay of the filtered data from your plots.
c) Assume σ x
2 = 0.01 and σ y
2 = 1.0 . Implement a Kalman filter from the equations provided in
class for the system in Matlab, using your knowledge of yn
,un ( ) (but not xn — this is only
used for comparisons.) Provide a print-out of your Matlab program, and a plot of the filtered
data, i.e., xˆn , and the true data xn . Plot the gain K and the posterior covariance matrix P as a
function of time (iterations). How did you initialize P? Estimate the delay of the filtered data
from your plots. Comment on the quality of the filter in comparison to the Butterworth filter.
