#Python Program to read CSV file
import numpy as np
import matplotlib.pyplot as plt
import csv

with open('GForce.csv','r') as f:
    data =list(csv.reader(f, delimiter=',')) #reading CSV file
    
data1 = np.array(data[1:], dtype=np.float) #converting list into float array

#Extracting data
time= data1[:,0]
ax=data1[:,1]
ay=data1[:,2]
az=data1[:,3]
aT=data1[:,4]

#Plotting all data on same axis
plt.figure(figsize=(20,10))
plt.plot(time,ax,time,ay,time,az,time,aT)
plt.title('Accelerometer data', fontsize=20)
plt.xlabel('Time',fontsize=20)
plt.ylabel('Acc.Values', fontsize=20)

#Separate plots using subplots
plt.figure(figsize=(20,20))

plt.subplot(2,2,1)
plt.plot(ax, color = 'r')
plt.title('a[x]', fontsize = 30)

plt.subplot(2,2,2)
plt.plot(ay, color = 'g')
plt.title('a[y]', fontsize = 30)

plt.subplot(2,2,3)
plt.plot(az, color = 'b')
plt.title('a[z]', fontsize = 30)

plt.subplot(2,2,4)
plt.plot(az, color = 'k')
plt.title('a[Total]', fontsize = 30)


#Processing data: Finding dwt of aT
#import pywt
#cA, cD = pywt.dwt(aT,'db5', mode='symmetric');
#plt.plot(cA)
#plt.plot(cD)


