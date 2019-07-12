
# The basic goal of speech processing is to provide an interaction between a human and a machine.

		Speech processing system has mainly three tasks −

		First, speech recognition that allows the machine to catch the words, phrases and sentences we speak

		Second, natural language processing to allow the machine to understand what we speak

		Third, speech synthesis to allow the machine to speak.

[//]: # (Image References)

[image1]:  ./Speech-Recognition/1.PNG  "Frequency versus Time Domain"


# The goals of this project are the following:

	* Understanding of main components of speech recognition.
	* Visualizing Audio Signals - Reading from a File and Working on.
	* Applying sampling at a certain frequency and converting the signal into the discrete numerical form.
	* Extracting Feature from Speech.
	* Speech Recognition Packages.




# Converting the signal into the discrete numerical form (Discrete Fourier Transform, or DFT)

When recording with microphone, the signals are stored in a digitized form. But to work upon it, the machine needs them in the discrete numeric form. Hence, we should perform sampling at a certain frequency and convert the signal into the discrete numerical form
The Fourier transform takes a signal in the time domain (i.e., a set of measurements over time) and turns it into a spectrum—a set of frequencies with corresponding values. The spectrum does not contain any information about time! 

[image1]

The DFT functionality in SciPy lives in the scipy.fftpack module. Among other things, it provides the following DFT-related functionality:

    fft, fft2, fftn

        Compute the DFT using the FFT algorithm in 1, 2, or n dimensions.
		
    ifft, ifft2, ifftn

        Compute the inverse of the DFT.
		
    dct, idct, dst, idst

        Compute the cosine and sine transforms, and their inverses.
		
    fftshift, ifftshift

        Shift the zero-frequency component to the center of the spectrum and back, respectively (more about that soon).
		
    fftfreq

        Return the DFT sample frequencies.
		
    rfft

        Compute the DFT of a real sequence, exploiting the symmetry of the resulting spectrum for increased performance. Also used by fft internally when applicable.
		

This list is complemented by the following functions in NumPy:

		np.hanning, np.hamming, np.bartlett, np.blackman, np.kaiser

Tapered windowing functions.

The DFT is also used to perform fast convolutions of large inputs by scipy.signal.fftconvolve.

# Feature Extraction from Speech.

This is the most important step in building a speech recognizer because after converting the speech signal into the frequency domain, we must convert it into the usable form of feature vector. 
We can use different feature extraction techniques like MFCC, PLP, PLP-RASTA etc.

# Speech Recognition Packages

A handful of packages for speech recognition exist on PyPI. A few of them include: apiai assemblyai google-cloud-speech pocketsphinx SpeechRecognition watson-developer-cloud wit Some of these packages—such as wit and apiai—offer built-in features, like natural language processing for identifying a speaker’s intent, which go beyond basic speech recognition. Others, like google-cloud-speech, focus solely on speechto- text conversion.
	 The Effect of Noise on Speech Recognition
	 Working With Microphones
