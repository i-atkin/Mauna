# Mauna
# -*- coding: utf-8 -*-
"""
Spyder Editor

This is a temporary script file.
"""

import numpy as np
from pylab import *

CO2_ppm_MaunaLoa = np.load("Mauna_CO2.npy")
#print(CO2_ppm_MaunaLoa)

# Create an array of time points (x)
# Each year will have 26 data points 

print(len(CO2_ppm_MaunaLoa))

x = np.linspace(0,229, 230)
print(x)

#how should I create a time stamp arrary so I'm able to average the measurements for each year, and then find the increese from yr to yr 
plot(x, CO2_ppm_MaunaLoa)

m, b = np. polyfit(x, CO2_ppm_MaunaLoa, 1)
plot(x, m*x + b)
xlabel("Observation number (time) (taken every 14 days)")                    # label the horizontal axis
ylabel("CO2 concentration (ppm)")                       # label the vertical axis
title("CO2 concentration as measured in Manua Loa, Hawaii")  # title the graph

show()


