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

