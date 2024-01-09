from fredapi import Fred # This line imports the Fred class from the fredapi module. The Fred class provides methods to interact with the FRED API.
import matplotlib.pyplot as plt # This line imports the pyplot module from matplotlib and names it plt for convenience.

# Set up Fred with your API key
fred = Fred(api_key='Your API') #This line creates an instance of the Fred class, passing your FRED API key as an argument. This fred object now has methods that can fetch data from the FRED API.

# Get the S&P 500 data
sp500 = fred.get_series('SP500', start='2020-01-01', end='2022-01-01') # This line calls the get_series method on the fred object to fetch the S&P 500 data from the FRED API. The data fetched is for the period from ‘2020-01-01’ to ‘2022-01-01’. The fetched data is stored in the sp500 variable.

# Plot the data
plt.figure(figsize=(10, 6)) #This line creates a new figure for plotting, with a size of 10 units wide by 6 units tall.
plt.plot(sp500) #This line creates a line plot of the sp500 data. The x-axis represents the index of the sp500 data (usually time or date), and the y-axis represents the values.
plt.ylabel('S&P 500 Index') #This line sets the label for the y-axis to ‘S&P 500 Index’.
plt.xlabel('Date') #This line sets the label for the x-axis to ‘Date’.
plt.show() #This line displays the plot. You should see the plot appear when this line runs.


