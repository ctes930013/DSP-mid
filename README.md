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


