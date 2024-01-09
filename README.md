from fredapi import Fred 
import matplotlib.pyplot as plt 

# Set up Fred with your API key
fred = Fred(api_key='Your API') 

# Get the S&P 500 data
sp500 = fred.get_series('SP500', start='2020-01-01', end='2022-01-01') 

# Plot the data
plt.figure(figsize=(10, 6)) 
plt.plot(sp500) 
plt.ylabel('S&P 500 Index') 
plt.xlabel('Date') 
plt.show() 


