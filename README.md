# Voice-Conversion
Converting male voice to female voice or vice versa

R&D
the input signal is an audio signal. audio signals have different kind of feature both in time and frequency domain,such as pitch, frequency, tone, to name a few. these features may differ based on the speaker gender.

besides, audio signals has some high level features such as language, emotion, etc.

There are already some voice changer app such as :
voicemoe, voxal voice changer , speechify, etc.
it seems that we can modify a voice by adjusting some features like pitch, frequency, tone , etc. Hence, one aim could be detection aforementioned features for a given voice, and adjust them to generate a new voice.

one way: do ASR(automatic speech recognition) to convert speech to text, and again do TTS(text to speech) with another voice

With the word "generate", i remember about GAN architecture, and a similar topic for vision! hmm.i knew an architecture in vision from the paper: "Image-to-Image Translation Using Identical-Pair Adversarial Networks" which is based on cycleGAN. Is there anythingg like that for voices? some challenges which we may encounter while working with audio signals are their variable length. i read that cyclegan which is trained based on souce A(male voice) and source B(female voice), may generates in noisy robot-like voice, and sometimes become worse by longer training[generate noise-like signal]. I googled about it and found similar ideas applied to audio signals. for instance there is a paper for voice conversion using speech2speech neurostyle transfer which is based on composition of VAE and GAN,followed by wavenet based vocoder vocoder is applied to transform the spectrogram to an audio waveform

there is also a python library for Pitch manipulation :parselmouth
torch.audio
it is also said wavenet can be applied for the Voice conversion
spectrogram :time-frequency representation of voice [to consider it as an image]

Reference:
https://www.andrewszot.com/posts/voice_conversion/ https://stackoverflow.com/questions/56509588/how-to-convert-a-female-to-a-male-voice-using-librosa
