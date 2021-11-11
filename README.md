# ONLINE SIGNATURE VERIFICATION

There are two ways for signature verification, namely offline and online. Offline method comes under the area of image processing and computer
vision, where we are relying on information obtained from the image of the signature whereas the latter makes use of the dynamic characteristics
of the handwritten trace (such as position coordinates, pressure, azimuth, pen status) for verification which generally comes under the area of
time series analysis.

With regards to online signatures, the strategies used to extract feature information from the data utilize either global or local based
characteristics. Dynamic Time Warping (DTW) is a prominent distance strategy that can be used for authentication. This technique essentially
matches the data points of two signatures with different number of timestamps to get some sense of alignment for matching purposes. This
technique is inspired by Longest Common Sub-sequence, a very famous algorithm used for string matching in computer science applications.

The problem is formulated as the one of time series analysis where dynamic characteristics of the signature such as pressure, azimuth, angle,
inclination, coordinates of the stylus are recorded at each sample point of the signature which would eventually give us a feature vector at each
sample point for all the sample points spread out in time, more formally a multivariate time series.

The input signature is passed through a feature extractor module, which is subjected to Dynamic time warping along with the reference signature
to calculate the normalized DTW score and the warping path. Moreover an additional warping path based score is calculated which is then fused
with the original DTW score and this fused score is then used for classifying the signature as genuine or forgery.
Equal error ratio (EER) will be chosen as an evaluation metric and experiments have been performed with an objective in mind to achieve EER
less than that of the traditional DTW systems.
