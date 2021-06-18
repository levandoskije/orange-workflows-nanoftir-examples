# Point Spectrum Examples
-------
The spectrum of points is a simpler file to generate for this equipment.

There are 3 possible file types:

 - Raw files, with extension \*.gsf
 - Spectra files, with extension \*.txt
 - Normalized files, with extension \*.txt

## How to open these files?

### 1. RAW files

It is the least processed file for equipment, so it is necessary to do the entire mathematical process.
There are benefits to this approach, as in this case you can have access to all measurements.
In some cases, it can be important to access SNR from all points, so with raw files you can do this.

How to open?

- To open these files you need to have **3 files in the same folder**, for example to open the second harmonic (O2)

  - "file name" O2A raw.gsf &rarr; *Interferogram of amplitude*
  - "file name" O2P raw.gsf &rarr; *Interferogram of phase*
  - "file name" .html &rarr; *File with measurement information*

- Open with ***Multifile***, when selecting the file "*[...] O2A raw.gsf*" or "*[...] O2P raw.gsf*" you need to select a specific reader, to raw files, needs to be **"*NeaSPEC raw files (\*. gsf)* "**, and the software will take care of finding the other 2 files, if they are in the same folder

- After opening the interferogram files, it is necessary to apply a Fast Fourier Transform (FFT), for that it is necessary to use the ***Interferogram to Spectrum*** widget, there are some settings available to users, such as Zero fill factor and what type of apodization you want to use. But you can just live by default if you don't want to change.

- The result of FFT is two files, "O2A" amplitude spectrum and "O2P" phase spectrum, this two files need to be splipted, for you can use them. For this you will use the ***Select Rows*** widget. Input the data from ***Interferogram to Spectrum*** in ***Select Rows***, open ***Select Rows*** and in Conditions add **channel** and type or select ***O2A***, now you have only *amplitude* spectrum in output. Put another ***Select Rows*** in data from ***Interferogram to Spectrum*** and in Conditions add **channel** and type or select ***O2P***, now you have only *phase* spectrum on another output.

- Now you have two diferent files, Phase Spectrum and Amplitude Spectrum.

### 2. Spectra files

### 3. Normalized files

## How to normalized these files using a reference spectrum?