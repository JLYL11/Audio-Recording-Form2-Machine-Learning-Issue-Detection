# Audio-Recording-Form2-Machine-Learning-Issue-Detection

Repository refereing to a post I made on Formlabs forum in Aug 2020 : 

[Audio Recording Form2 + Machine Learning = Issue Detection?](https://forum.formlabs.com/t/audio-recording-form2-machine-learning-issue-detection/28657?u=jlyl33)

Two days ago I heard a loud banging noise just after starting a new print on my Form2. Luckily I immediately found out that I stupidly forgot to attach the wiper after changing the resin tray. I could abort and start over rapidly without any damage to the printer and its accessories. I think I was quite lucky as I did not leave the place right after starting the print.

What saved me here is the noise from the machine that gave me quite a hint that something was wrong.

I think some sort of sound monitoring could be useful either as a warning or diagnosis tool. I’m not a coder but as a proof of concept I used 
[Teachable Machine](https://teachablemachine.withgoogle.com/)
, a machine learning tool from Google and trained it using a microphone near my Form2.

I made several classes (Background Noise, Wiper, Build Platform going UP, Build Platform going Down) and the preview seems to be working okay with little samples 
[you can try it online if you have a microphone to put next to the printer](https://teachablemachine.withgoogle.com/models/3HDwEux7g/)
.

![6cc3b7ce05080d1c516e74c272473d988523f5fd_2_690x344](https://user-images.githubusercontent.com/63747240/228868668-3d467431-a6df-4c47-890a-99293c3e3efd.jpg)

I think with more training on specific problematic sounds, and a better method for recording sounds it could make a great inexpensive feature. I am thinking about some noise-related posts in the forum that were related to:

- z-axis stepper motor
- suction issue
- resin tray not mounted well
- collision wiper/failing parts

I am not keen on reproducing these issues on my printer to train the model but I would totally have a Raspberry Pi with a microphone recording during the print and send me notifications if something weird is recorded.

PS: Happy to share TM file with samples (30Mo)

PPS: I also tricked TM by sending sliced mp3 recording of the print via a virtual microphone
