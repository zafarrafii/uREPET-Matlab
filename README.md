# uREPET-Matlab

Matlab GUI for uREPET, a simple user interface system for recovering patterns repeating in time and frequency in mixtures of sounds. 

Files:
- [`urepet.m`](#urepet): Matlab class with the REPET methods.
- [`audio_file.wav`](#audio_filewav): audio file used for the examples.
- [`audio_file.wav`](#audio_filewav): audio file used for the examples.
- [`audio_file.wav`](#audio_filewav): audio file used for the examples.

See also:
- [REPET-Python](https://github.com/zafarrafii/REPET-Matlab): REPET in **Python** for audio source separation.

## urepet.m

Simple user interface system for recovering patterns repeating in time and frequency in mixtures of sounds.

Functionalities:

- [Open](#open)
- [Save](#save)
- [Play](#play)
- [Select](#select)
- [Zoom](#zoom-2)
- [Pan](#pan-2)
- [uREPET](#urepet)
- [Background](#background)
- [Undo](#undo)

### Open

- Select a WAVE or MP3 to open; the audio can be mono or stereo.
- Display the audio signal and the audio spectrogram; the x-axis limits of the signal axes and the spectrogram axes will be synchronized (and will stay synchronized if a zoom or pan is applied on one of them).

### Save

- Save the processed audio as a WAVE file; the default name is "urepet_file.wav."

### Play

- Play the audio if the playback is not in progress; stop the audio if the playback is in progress; a playback line will be displayed as the playback is in progress.
- If there is no selection line or region, the audio will be played from the start to the end; if there is a selection line, the audio will be played from the selection line to the end of the audio; if there is a selection region, the audio will be played from the start to the end of the selection region.
- Pressing the space key will also play and stop the audio.

### Select

- If a left mouse click is done on the signal axes, a selection line is created; the audio will be played from the selection line to the end of the audio.
- If a left mouse click and drag is done on the signal axes or on a selection line, a selection region is created; the audio will be played from the start to the end of the selection region.
- If a left mouse click and drag is done on the left or right boundary of a selection region, the selection region is resized.
- If a right mouse click is done on the signal axes, any selection line or region is removed.
- If a left mouse click and drag is done on the spectrogram axes, a customizable rectangle is created; the region-of-interest (ROI) can then be processed by clicking on the uREPET button; the rectangle can be resized and moved, and also deleted by doing a right mouse click on it.

<img src="images/open_play_select.gif" width="1000">

### Zoom

- Turn zooming on or off or magnify by factor (see https://mathworks.com/help/matlab/ref/zoom.html)
- If used on the signal axes, zoom horizontally only; the x-axis limits of the signal axes and the spectrogram axes will stay synchronized.

### Pan

- Pan view of graph interactively (see https://www.mathworks.com/help/matlab/ref/pan.html)
- If used on the signal axes, pan horizontally only; the x-axis limits of the signal axes and the spectrogram axes will stay synchronized.

<img src="images/zoom_pan.gif" width="1000">

### uREPET

- Apply uREPET to the audio, after selecting an ROI on the spectrogram axes, by searching for similar regions repeating in time and frequency and recovering the common background if the background button is selected, or the common foreground if the background button is deselected.

### Background

- If selected, uREPET will recover the repeating background in the ROI (default); if deselected, uREPET will recover the non-repeating foreground in the ROI.

### Undo

- Undo the last changes done by uREPET.

<img src="images/select_urepet_background_undo_save.gif" width="1000">


## audio_file.wav

23 second audio excerpt from the song *Que Pena Tanto Faz* performed by *Tamy*.


# References

- Zafar Rafii, Antoine Liutkus, and Bryan Pardo. "A Simple User Interface System for Recovering Patterns Repeating in Time and Frequency in Mixtures of Sounds," *40th IEEE International Conference on Acoustics, Speech and Signal Processing*, Brisbane, Australia, April 19-24, 2015. [[article](http://zafarrafii.com/Publications/Rafii-Liutkus-Pardo%20-%20A%20Simple%20User%20Interface%20System%20for%20Recovering%20Patterns%20Repeating%20in%20Time%20and%20Frequency%20in%20Mixtures%20of%20Sounds%20-%202015.pdf)][[poster](http://zafarrafii.com/Publications/Rafii-Liutkus-Pardo%20-%20A%20Simple%20User%20Interface%20System%20for%20Recovering%20Patterns%20Repeating%20in%20Time%20and%20Frequency%20in%20Mixtures%20of%20Sounds%20-%202015%20(poster).pdf)]

- Christian Schorkhuber and Anssi Klapuri. "Constant-Q Transform Toolbox for Music Processing," *AES 53rd International Conference on Semantic Audio*, London, UK, January 26-29, 2014. [[article](https://iem.kug.ac.at/fileadmin/media/iem/projects/2010/smc10_schoerkhuber.pdf)][[website](https://www.cs.tut.fi/sgn/arg/CQT/)]


# Author

- Zafar Rafii
- zafarrafii@gmail.com
- http://zafarrafii.com/
- [CV](http://zafarrafii.com/Zafar%20Rafii%20-%20C.V..pdf)
- [GitHub](https://github.com/zafarrafii)
- [LinkedIn](https://www.linkedin.com/in/zafarrafii/)
- [Google Scholar](https://scholar.google.com/citations?user=8wbS2EsAAAAJ&hl=en)
