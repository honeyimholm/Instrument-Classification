# Instrument Classification
Being able to detect instruments in audio files could be a very applicable
tool for applications from music education to consumer music search engines
like Spotify. This problem has been attempted, but not solved with complete
accuracy. The approach of this study is to use a Constant-Q transform on a
dataset of instrument samples, and train a Convolutional Neural Network to
be able to detect a specific instrument in an audio file. Using this method
within our data set, the accuracy of identification was 96.9%. The detection
remained robust even when noise was added to the samples.

# Demo
For this demo we'll show you our complete pipeline - from .wav sample to classification. 
You must have Tensorflow to run the demo.  

First, we take the noisy_flute.wav file and perform a CQT on it using the cqt.m file, and the plotnsgtf.m file . 

Next, we needed to crop the output image before it can be fed into our CNN.  We batch fed our images into photoshop to ensure that they were exactly the right size and cropped exactly in the right place.

The result of this is:
![alt text](https://github.com/honeyimholm/Instrument-Classification/blob/master/noisy_flute_sample.png)

Now this CQT was ready to be fed into our CNN! Do this by running "python predict.py noisy_flute_sample.png" 
 
The result should be an output list with the first element being confidence of the flute classification and second element being confidence of the no flute classification.

#Toolboxes

We tried all of the following algorithms for a Constant Q Transform, and got the most distinctly different visual results from the algorithm in the first link.  The parameters we used to tune the transform are detailed in our paper.

https://www.cs.tut.fi/sgn/arg/CQT/ 

http://www.ee.columbia.edu/ln/rosa/matlab/sgram/

http://doc.ml.tu-berlin.de/bbci/material/publications/Bla_constQ.pdf
