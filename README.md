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

First, we take the noisy_flute.wav file and perform a CQT on it using the (EDIT).m file. When run with 
command line options (EDIT) it will output a CQT that looks like this:
[EDIT]

Next, we'll need to crop the output image before it can be fed into our CNN. Run the (EDIT).m script.
Change the (EDIT) variable if you're using a different CQT image name. It will look like this:
[EDIT]

Now this CQT is ready to be fed into our CNN! Do this by running "python predict.py noisy_flute_sample.png"
The result should be an output list with the 
