# Forecasting Number of Spotify Streams using Time Series

## Code
* [EDA and Forecasting Notebook](https://github.com/maxgrossenbacher/kaggle_spotify/blob/master/src/Spotify_Time_Series.ipynb) - In this notebook, I forecast the avg. number of streams and the number of streams for the #1 song on Spotify using ARIMA models.
* [Plotting Script](https://github.com/maxgrossenbacher/Forecasting_daily_spotify_streams/blob/master/src/spotify_plot_top_song.py) - script for plotting streams of number one song over time. Run [spotify_data_crawler.py](https://github.com/maxgrossenbacher/Forecasting_daily_spotify_streams/blob/master/src/spotify_data_crawler.py) for up to data Spotify streaming data.
* [Getting Audio Features](https://github.com/maxgrossenbacher/kaggle_spotify/blob/master/src/spotify_data_collection.py) - script for using Spotify API to get audio features of song on Spotify  

## EDA Plots
The United States has the most average daily streams on Spotify.
![alt_text](images/Avg_Daily_Streams_per_Region.png)
We can see that number of daily streams are lowest on Sundays and grow gradually throughout the week, peaking on Fridays.
![alt_text](images/Avg_Streaming_Jan_2017.png)
![alt_text](images/Avg_Streaming_Day_of_Week.png)

Here we can see the total number of streams of the top song on Spotify for the day and the average number of daily streams on Spotify for the day. Notice the spike in streams in the month of March.  

![alt_text](images/avg_streams_v.s_streams_%231_song.png)

Additionally, if we look at monthly trends we can see that Spotify streams peak in the month of March. Upon further analysis, one possible explanation for this spike in streams in March could be the result of a rise in demand for music streaming services during Spring Break which typically falls in the month of March. In March, we see approximately 100,000 stream increase compared to the average daily streams.  

![alt_text](images/avg_streams_per_month.png)

Lastly, we can track the total number of plays for the number one song on Spotify each day. Each line is colored based on track name. Below we can see the global top song and number of daily streams that song received.  
![alt_text](images/Global_%231_Song_Streams_January_to_September_2017.png)

## Conclusions & Future Directions
We can see that ARIMA models are able to capture the weekly trends in number of daily Spotify streams. Number of daily streams are lowest on Sundays and grow gradually throughout the week, peaking on Fridays.

However, the ARIMA models not very good at forecasting monthly trends of daily number of Spotify streams. Since, this data is only for an 8 month period, the ARIMA models are having a tough time forecasting the monthly underlying signal. A longer period of data would allow the ARIMA models to better capture this signal.  
![alt_text](images/ARIMA_model_to_Predict_Average_Number_of_Streams.png)

Some future directions for this project would be to try LSTM neural net to improve the forecasting number of daily streams on Spotify.

## Tech Stack
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Statsmodels
* TimeSeries - ARIMA
