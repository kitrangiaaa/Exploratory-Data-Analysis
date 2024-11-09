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

To get the outliers for the artist count, I coded "spotify.artist_count > 3" to create a filtered data frame where the artist count is greater than 3. It points to data points with more than three artists for a specific release year.

Here is the output:

<img width="856" alt="Screenshot 2024-11-09 at 7 49 21 PM" src="https://github.com/user-attachments/assets/8f5eede9-fe8e-4670-845b-2350f5532a37">

## __TOP PERFORMERS__

### __Which track has the highest number of streams? Display the top 5 most streamed tracks.__

I used these codes:

<img width="495" alt="Screenshot 2024-11-09 at 7 55 00 PM" src="https://github.com/user-attachments/assets/30a5f8dd-41df-4a62-9350-901aec096d40">

This code sorts the Spotify data frame based on the "by='streams, " specifically the streams column, and I used .head() to get only the top five most streamed tracks.

<img width="626" alt="Screenshot 2024-11-09 at 8 10 31 PM" src="https://github.com/user-attachments/assets/4ae7cdce-bad4-4436-b4d2-e28e779acbcb">

This code is used to bar plot the outcome of the most streamed tracks. Here, you will know the track with the highest number of streams, "Blinding Lights"; you will see it in the output.

Here are the outputs:

<img width="1034" alt="Screenshot 2024-11-09 at 7 59 15 PM" src="https://github.com/user-attachments/assets/955a9b27-6c7e-4501-8959-62073f00b9b4">

<img width="1034" alt="Screenshot 2024-11-09 at 7 57 40 PM" src="https://github.com/user-attachments/assets/a642ccdf-2141-4197-8c87-52ad2cd1eca1">

<img width="686" alt="Screenshot 2024-11-09 at 8 17 18 PM" src="https://github.com/user-attachments/assets/d0c889dd-5a0f-409d-aa2d-11d1407cfb28">

### __Who are the top 5 most frequent artists based on the number of tracks in the dataset?__

I used these codes to answer the question:

<img width="963" alt="Screenshot 2024-11-09 at 8 17 58 PM" src="https://github.com/user-attachments/assets/b2d99e66-8763-4bf8-bc95-544d557f0d85">

"spotify_exploded" contains the data about the Spotify data frame. I used the "groupby('artist(s)_name')" to organize it based on the specific column. This means all rows with the same artist name will be grouped.

<img width="697" alt="Screenshot 2024-11-09 at 8 18 23 PM" src="https://github.com/user-attachments/assets/6404ce44-9741-492c-82d1-1a968243d15c">

This code is used to bar plot the outcome of the most frequent artists again based on the number of tracks. Here, based on the outcome below, you will know who is the top one and who is the top 5.

Here are the outputs:

<img width="1034" alt="Screenshot 2024-11-09 at 8 18 38 PM" src="https://github.com/user-attachments/assets/5a8e5715-f0a7-46a4-9af3-af449bbea503">

<img width="1037" alt="Screenshot 2024-11-09 at 8 18 59 PM" src="https://github.com/user-attachments/assets/06d6fd82-a34c-4c1a-a8a5-cad5e209903e">

<img width="584" alt="Screenshot 2024-11-09 at 8 19 30 PM" src="https://github.com/user-attachments/assets/86aa1321-f17d-4065-bf87-f30f13f38b62">

## __TEMPORAL TRENDS__

### __Analyze the trends in the number of tracks released over time. Plot the number of tracks released per year.__

I used this code to answer the question:

<img width="519" alt="Screenshot 2024-11-09 at 8 24 56 PM" src="https://github.com/user-attachments/assets/116cbb42-8fbf-4ae3-9713-5b74a158fb38">

I used "spotify.groupby('released_year')" to group the tracks released in the same year. I used "plt.plot" to plot the number of tracks released yearly. I renamed the x, y, and title by using "plt.xlabel", "plt.ylabel", and "plt.title". I printed the number of tracks per year to see the difference.

Here are the outputs:

<img width="83" alt="Screenshot 2024-11-09 at 8 25 52 PM" src="https://github.com/user-attachments/assets/8ba5fb57-74ce-4800-9418-a34068d88696">

<img width="600" alt="Screenshot 2024-11-09 at 8 26 22 PM" src="https://github.com/user-attachments/assets/31adc62e-70d6-4bb3-aec0-a6ce679c4046">

### __Does the number of tracks released per month follow any noticeable patterns? Which month sees the most releases?__

I used this code:

<img width="552" alt="Screenshot 2024-11-09 at 8 29 48 PM" src="https://github.com/user-attachments/assets/fb4a8924-fe5f-48d5-9845-424611f1d983">

I used "spotify.groupby('released_month')" to group the tracks released in the same month. I renamed the x, y, and title by using "plt.xlabel", "plt.ylabel", and "plt.title". I used the "month.idxmax()" to determine which month has the most releases. You will see in the output that January is that month.

Here is the output:

<img width="604" alt="Screenshot 2024-11-09 at 8 30 15 PM" src="https://github.com/user-attachments/assets/d4d83c52-b08e-467f-bf43-29f48691897c">

## __GENRE AND MUSIC CHARACTERISTICS__

### __Examine the correlation between streams and musical attributes like bpm, danceability_%, and energy_%. Which attributes seem to influence streams the most?__

I used this code:

<img width="1131" alt="Screenshot 2024-11-09 at 8 33 53 PM" src="https://github.com/user-attachments/assets/afc1802c-db04-4af2-8636-a98257c14453">

The algorithm computes and displays the correlation between different musical qualities and streams. It determines which property has the strongest correlation with streams. It then creates charts showing how each attribute affects streams.

Here is the output:

<img width="899" alt="Screenshot 2024-11-09 at 8 34 17 PM" src="https://github.com/user-attachments/assets/d63ccc68-24b6-4bae-b581-66c4746ddf3f">

### __Is there a correlation between danceability_% and energy_%? How about valence_% and acousticness_%?__

I used this code:

<img width="511" alt="Screenshot 2024-11-09 at 8 34 36 PM" src="https://github.com/user-attachments/assets/87508b59-9dd1-4fcb-895d-49e5c5d94809">

The algorithm determines the association between the musical attribute pairs "valence_%" and "acousticness_%" and "danceability_%" and "energy_%." The first pair plot illustrates the relationship between danceability_% and energy_%. The link between valence_% and acousticness_% is displayed in the second pair plot. Transparency is adjusted to 50% (alpha=0.5).

Here is the output:

<img width="268" alt="Screenshot 2024-11-09 at 8 35 02 PM" src="https://github.com/user-attachments/assets/1015f9d7-b4b0-4926-a4b2-e4bf986e5787">

## __PLATFORM POPULARITY__

### __How do the numbers of tracks in spotify_playlists, spotify_charts, and apple_playlists compare? Which platform seems to favor the most popular tracks?__

I used this code:

<img width="856" alt="Screenshot 2024-11-09 at 8 35 22 PM" src="https://github.com/user-attachments/assets/b3a0b372-c8ea-45b3-9961-3bba099e12ec">

This code is used to bar plot the comparison of different platforms. I used "sns.barplot" to plot already the x and y. I renamed the x, y, and title by using "plt.xlabel", "plt.ylabel", and "plt.title". You will see in the outcome that spotify playlists favored the most popular tracks.

Here is the output:

<img width="565" alt="Screenshot 2024-11-09 at 8 35 36 PM" src="https://github.com/user-attachments/assets/c7814283-8404-4146-8cee-ca64d48621f1">

## __ADVANCED ANALYSIS__

### __Based on the streams data, can you identify any patterns among tracks with the same key or mode (Major vs. Minor)?__

I used these codes:

<img width="837" alt="Screenshot 2024-11-09 at 8 35 52 PM" src="https://github.com/user-attachments/assets/0b95d251-8afc-49bb-930a-8865b5d318b9">

<img width="852" alt="Screenshot 2024-11-09 at 8 36 41 PM" src="https://github.com/user-attachments/assets/3f3e4bc2-1775-462d-be6b-50d038e98f64">

I used a bar plot in both of these codes. I separated them because one has the keys while the other has the mode, so you can see it. The key with the highest total streams is C# with 72513629843.0 streams, and the lowest is D# with 18250205825.0 streams. Major has the most streams based on the graph.

Here are the outputs:

<img width="586" alt="Screenshot 2024-11-09 at 8 36 08 PM" src="https://github.com/user-attachments/assets/16d4c807-fbc0-4b7d-935d-f71426294714">

<img width="582" alt="Screenshot 2024-11-09 at 8 37 05 PM" src="https://github.com/user-attachments/assets/14733d2a-1f61-4ea5-9ef4-bce5ee632750">

### __Do certain genres or artists consistently appear in more playlists or charts? Perform an analysis to compare the most frequently appearing artists in playlists or charts.__

I used this code:

<img width="1035" alt="Screenshot 2024-11-09 at 8 37 28 PM" src="https://github.com/user-attachments/assets/9d203d8f-27cd-4e85-8653-262609dc06f6">

The code produces a 2x2 grid of bar plots. The top five artists are displayed in each plot according to how often they appear in one of the four platforms: Apple charts, Spotify playlists, Spotify charts, or Spotify playlists. The bars show how often each artist has appeared on the platform. Matplotlib handles subplots, and Seaborn is used to visualize the plots.

Here is the output:

<img width="752" alt="Screenshot 2024-11-09 at 8 37 54 PM" src="https://github.com/user-attachments/assets/f81f1e2b-e624-4b28-93eb-a0ad281fb32d">

## __MESSAGE__

Thank you for accompanying me on this long journey. God bless!

