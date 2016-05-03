# DSP-mid
This is my midterm exam in Signal and System


1.

import numpy as np

f=open('_taiwanStock.csv')

s=f.read()

sL=s.split('\n')

xL=[x.split(',')[-1]for x in sL]

yL=[float(x)for x in xL[1:-4]]

pData=np.array(yL)

len(pData)

<<13505

2.

print(pData[13494:13504])

<<[ 8513.3   8490.25  8541.5   8562.59  8531.18  8652.08  8667.71  8700.39 8666.01  8633.72]

3.

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


