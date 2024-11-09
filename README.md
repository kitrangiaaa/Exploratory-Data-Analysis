## <center> WELCOME TO MY EXPLORATORY DATA ANALYSIS (EDA) ON SPOTIFY 2023!

##### Name: Trangia, Klein Isshi G.

##### Section: 2ECE-D

##### Date Submitted: November 9, 2024

I first imported the pandas as pd, matplotlib.pyplot as plt, and seaborn as sns to access their following libraries.
<img width="276" alt="Screenshot 2024-11-09 at 5 21 54 PM" src="https://github.com/user-attachments/assets/16993dc4-8a6e-4a2d-b181-e5abddebe10b">

## __OVERVIEW OF THE DATA SET__

### __How many rows and columns does the dataset contain?__

I first downloaded the data card using the link provided and converted it to Excel since CSV is not working on my end. I then used "Spotify" to store the code to read the Excel file uploaded in my Jupyter.

<img width="376" alt="Screenshot 2024-11-09 at 5 31 07 PM" src="https://github.com/user-attachments/assets/ebddcdd3-961f-4e9a-82dd-d108a158aeb6">

<img width="1014" alt="Screenshot 2024-11-09 at 5 37 08 PM" src="https://github.com/user-attachments/assets/bcfbdf83-b77f-42c2-9aec-501f364b4e22">
<img width="1037" alt="Screenshot 2024-11-09 at 5 37 34 PM" src="https://github.com/user-attachments/assets/a301583b-d4ce-477c-adf1-1521dce8aed5">

To answer the question, I used this code:

<img width="119" alt="Screenshot 2024-11-09 at 5 46 51 PM" src="https://github.com/user-attachments/assets/a9aeac6d-0b36-4964-b605-4eb88af7cd7a">

I used .shape in order to get the number of rows and columns in the dataset.

Here is the output of my code:

<img width="94" alt="Screenshot 2024-11-09 at 5 47 19 PM" src="https://github.com/user-attachments/assets/3c1b150d-64e1-487f-8fd6-f9ca29ad2341">

### __What are the data types of each column? Are there any missing values?__

I used these following codes for this question:

<img width="132" alt="Screenshot 2024-11-09 at 5 48 55 PM" src="https://github.com/user-attachments/assets/5dedd2be-8946-453a-a3be-4f19c4cd3230">
<img width="192" alt="Screenshot 2024-11-09 at 5 49 50 PM" src="https://github.com/user-attachments/assets/dcb70411-3cef-44d9-bbe3-ea5e592ac19a">

For the data types of each column, I used .dtypes. 

Here is the output for data types:

<img width="259" alt="Screenshot 2024-11-09 at 5 50 44 PM" src="https://github.com/user-attachments/assets/41442528-c176-4025-ae73-d32774855e8a">

While I used .isnull().sum() to get the missing values, and because of that, I knew that there were missing values in "in_shazam_charts" and "key," which are 50 and 95, respectively.

Here is the output for the missing values:

<img width="223" alt="Screenshot 2024-11-09 at 5 58 27 PM" src="https://github.com/user-attachments/assets/02fac4cb-b735-434a-bed6-bab9a9010e37">

Now that we are done with overview of the data set, let's proceed to the basic descriptive statistics.

## __BASIC DESCRIPTIVE STATISTICS__

### __What are the mean, median, and standard deviation of the streams column?__

I first coded the "pd.to_numeric" to convert the streams column into a numeric data type. While "error='coerce'" is for any values that cannot be converted.

<img width="570" alt="Screenshot 2024-11-09 at 7 33 46 PM" src="https://github.com/user-attachments/assets/13eb73c1-2828-42e0-860f-fb8c40f7a891">

After coding that, I proceeded to answer the question.

I used this code to get the mean:

<img width="271" alt="Screenshot 2024-11-09 at 7 37 07 PM" src="https://github.com/user-attachments/assets/7c12c8f6-4671-4914-a911-b07f7265685a">

I used this code to get the median:

<img width="300" alt="Screenshot 2024-11-09 at 7 38 35 PM" src="https://github.com/user-attachments/assets/39221378-bf4f-4f2a-839a-1170dbfc9e55">

I used this code to get the standard deviation:

<img width="394" alt="Screenshot 2024-11-09 at 7 38 50 PM" src="https://github.com/user-attachments/assets/499652ee-1bf4-40d7-915b-0e1505795577">

I used the .mean(), .median(), and .std() since it can already be computed for the answer. It is a part of the Pandas Library, so it is easier than manually typing the code.

And here are the following outputs:

<img width="207" alt="Screenshot 2024-11-09 at 7 39 41 PM" src="https://github.com/user-attachments/assets/1f5cdb0f-33c9-414b-acf9-fa18bb7af00f">
<img width="174" alt="Screenshot 2024-11-09 at 7 39 59 PM" src="https://github.com/user-attachments/assets/aa7cce16-4f6b-4d16-a264-534895f18ebc">
<img width="312" alt="Screenshot 2024-11-09 at 7 40 12 PM" src="https://github.com/user-attachments/assets/1271567d-7050-48a4-8f4c-f01cc08207a0">

### __What is the distribution of released_year and artist_count? Are there any noticeable trends or outliers?__

I used this code:

<img width="686" alt="Screenshot 2024-11-09 at 7 48 02 PM" src="https://github.com/user-attachments/assets/00def768-248e-4564-a672-b7dd6061b806">

For "plt.figure", I chose a width of 10 inches and a height of 5 inches. "plt.bar" is to graph the x as released year and y as artist count. I also renamed the x, y, and title by using "plt.xlabel", "plt.ylabel", and "plt.title". 

To get the outliers for the artist count, I coded "spotify.artist_count > 3" in order to create a filtered data frame where artist count is greater than 3. It is pointing data points where more than 3 artists for a specific release year.

Here is the output:

<img width="856" alt="Screenshot 2024-11-09 at 7 49 21 PM" src="https://github.com/user-attachments/assets/8f5eede9-fe8e-4670-845b-2350f5532a37">

## __TOP PERFORMERS__

### __Which track has the highest number of streams? Display the top 5 most streamed tracks.__

I used this code:

<img width="495" alt="Screenshot 2024-11-09 at 7 55 00 PM" src="https://github.com/user-attachments/assets/30a5f8dd-41df-4a62-9350-901aec096d40">

Here is the output:

<img width="1034" alt="Screenshot 2024-11-09 at 7 59 15 PM" src="https://github.com/user-attachments/assets/955a9b27-6c7e-4501-8959-62073f00b9b4">

<img width="1034" alt="Screenshot 2024-11-09 at 7 57 40 PM" src="https://github.com/user-attachments/assets/a642ccdf-2141-4197-8c87-52ad2cd1eca1">

### __Who are the top 5 most frequent artists based on the number of tracks in the dataset?__

## __TEMPORAL TRENDS__

### __Analyze the trends in the number of tracks released over time. Plot the number of tracks released per year.__

### __Does the number of tracks released per month follow any noticeable patterns? Which month sees the most releases?__

## __GENRE AND MUSIC CHARACTERISTICS__

### __Examine the correlation between streams and musical attributes like bpm, danceability_%, and energy_%. Which attributes seem to influence streams the most?__

### __Is there a correlation between danceability_% and energy_%? How about valence_% and acousticness_%?__

## __PLATFORM POPULARITY__

### __How do the numbers of tracks in spotify_playlists, spotify_charts, and apple_playlists compare? Which platform seems to favor the most popular tracks?__

## __ADVANCED ANALYSIS__

### __Based on the streams data, can you identify any patterns among tracks with the same key or mode (Major vs. Minor)?__

### __Do certain genres or artists consistently appear in more playlists or charts? Perform an analysis to compare the most frequently appearing artists in playlists or charts.__
