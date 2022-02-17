# histogram-equalization-from-scratch
implementation of histogram equalization ,as an image contrast enhancement method, from scratch using python only


histogram equalization is a wellknown method for image contrast enhancement.
in this notebook i implemented this method as a function, and then compared the results with CV2's equalizeHist. results were promising.

how to implement:
1.first we need to calculate the occurance probabilty of brightensses in an image (relative frequency). this helps us to know how often a brightness occurs in an image , so we know how much it affects the final result.
2. we are going to calculate CDF (cumulative distribution function) using these frequencies , to have a linear model of the brightnesses, to be able to map them on a liner graph like histogram
3. now all the pixels in image will be enhanced by this formula (floor((L-1)*sum(CDF)))
