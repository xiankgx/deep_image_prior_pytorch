# Deep Image Prior Pytorch

This is a quick attempt to reproduce the work Deep Image Prior for image denoising.

## Summary

In brief, it says that you don't really need example pairs for certain tasks such as image denoising. What you can do is to use the one image that you want to be processed (denoising, resized, etc.), fit a network to it, but don't fit it for too long.

The idea is that it is harder to learn the image contents plus noise rather than just the image contents itself. In other words, there is high impedance towards learning noise. However, if we fit the network to the image long enough, eventually, the network will be able to overfit to the image and learn the noise provided there is enough capacity in the network to do so. The idea here is to stop training before that point is reached.
