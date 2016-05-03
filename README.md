# DSP-mid
This is my midterm exam in Signal and System

1.(a)

signal=SinSignal(100)

signal.plot()

<<請打開midsignal07.png

signal=TriangleSignal(100)

signal.plot()

<<請打開midsignal08.png

signal=SquareSignal(100)

signal.plot()

<<請打開midsignal09.png

signal=SawtoothSignal(100)

signal.plot()

<<請打開midsignal10.png

(b)

signal=SinSignal(100)

wave=signal.make_wave()

spectrum=wave.make_spectrum()

spectrum.plot()

<<請打開midsignal14.png

signal=TriangleSignal(100)

wave=signal.make_wave()

spectrum=wave.make_spectrum()

spectrum.plot()

<<請打開midsignal13.png

signal=SquareSignal(100)

wave=signal.make_wave()

spectrum=wave.make_spectrum()

spectrum.plot()

<<請打開midsignal12.png

signal=SawtoothSignal(100)

wave=signal.make_wave()

spectrum=wave.make_spectrum()

spectrum.plot()

<<請打開midsignal11.png

(c)

Sawtooth有最複雜的頻譜結構

2.(a)

from thinkdsp import*

signal=Chirp(start=100,end=1000)

wave=signal.make_wave(duration=10)

(b)

spectrum=wave.make_spectrum()

spectrum.plot_power()

<<請打開midsignal05.png

(c)

wave=signal.make_wave(duration=10,framerate=2048)

spectrogram=wave.make_spectrogram(seg_length=1024)

spectrogram.plot()

<<請打開midsignal06.png


3.(a)

import numpy as np

f=open('_taiwanStock.csv')

s=f.read()

sL=s.split('\n')

xL=[x.split(',')[-1]for x in sL]

yL=[float(x)for x in xL[1:-4]]

pData=np.array(yL)

len(pData)

<<13505

(b)

print(pData[13494:13504])

<<[ 8513.3   8490.25  8541.5   8562.59  8531.18  8652.08  8667.71  8700.39 8666.01  8633.72]

(c)

import numpy as np

import pylab as pl

def movingAverage(x,length): 
  
  y=np.convolve(x,np.ones(length)/length) 
  
  y=y[:len(x)] 
  
  return y

pl.plot(prData)

<<請打開midsignal01.png

ma100=movingAverage(pData,100)

pl.plot(ma100)

<<請打開midsignal02.png

ma1000=movingAverage(pData,1000)

pl.plot(ma1000)

<<請打開midsignal03.png

ma10000=movingAverage(pData,10000)

pl.plot(ma10000)

<<請打開midsignal04.png

(d)

from thinkdsp import*

pNoise=PinkNoise()

pNoise.make_wave(13505).plot()


