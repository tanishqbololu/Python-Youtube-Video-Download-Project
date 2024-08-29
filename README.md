# Python-Youtube-Video-Download-Project

This Python script performs several tasks related to YouTube videos, such as extracting information about the video and providing an option to download it. The script uses two libraries: pytube and yt-dlp.

Step-by-Step Breakdown: 
1. Installing Required Packages:
    opip install pytube3 and pip install --upgrade pytube: Install and upgrade the pytube library. This library allows you to interact with YouTube videos.
    opip install yt-dlp: Install yt-dlp, a popular YouTube downloader with more advanced features.
    2. Importing the Libraries:
      ofrom pytube import YouTube: Import the YouTube class from the pytube library, which is used to interact with YouTube videos.
      ofrom yt_dlp import YoutubeDL: Import the YoutubeDL class from yt-dlp, used for downloading videos.
    3. Getting the YouTube Video Link:
      olink = input("Enter youtube video"): Prompt the user to enter the YouTube video URL.
    4. Extracting Video Information:
      oyt = YouTube(link): Create a YouTube object for the provided video link.
      oprint("Title :", yt.title): Print the title of the video.
      oprint("Views :", yt.views): Print the number of views the video has.
      oprint("Duration :", yt.length): Print the duration (in seconds) of the video.
      oprint("Description :", yt.description): Print the video's description.
      oprint("Ratings :", yt.rating): Print the video's average rating.
    5. Downloading the Video:
       odownload_option = input("Do you want to download this video? (yes/no): ").lower(): Ask the user if they want to download the video. The answer is converted to lowercase for easier comparison.
       oIf the user chooses "yes":
       url = 'https://youtube.com/shorts/skdXa3Q61HE?si=nHklaHieslhrsGxm': Define the URL of the video to be downloaded (in this case, a specific YouTube Shorts video).
       ydl_opts = {'format': 'best'}: Set the download options, specifying that the best quality available should be downloaded.
       with YoutubeDL(ydl_opts) as ydl: Use the YoutubeDL class to download the video using the specified options.
       ydl.download([url]): Start downloading the video.
       print("Download completed."): Inform the user that the download is complete.
       If the user chooses "no":
       print("Download aborted."): Inform the user that the download has been aborted.

Documentation:
1. Overview
This script allows you to extract information about a YouTube video and optionally download it. It utilizes the pytube library for fetching video details and yt-dlp for downloading the video.
2. Prerequisites
Make sure you have the required Python packages installed:
bash
Copy code
pip install pytube3
pip install --upgrade pytube
pip install yt-dlp
3. Usage
    1.Running the Script:
    To use the script, run it in your Python environment. The script will prompt you to enter a YouTube video URL.
    2.Extracting Video Information:
    The script will print the following details about the video:
     * Title
     * Number of views
     * Duration (in seconds)
     * Description
     * Average ratings
    3.Downloading the Video:
     After displaying the video information, the script will ask if you want to download the video.
     * If you choose "yes", it will download the video using the URL provided in the script.
     * If you choose "no", the download will be aborted.
4. Code Explanation
The code is broken down into the following main sections:
    * Input Handling: The user is prompted to enter the YouTube video URL.
    * Information Extraction: Video details like title, views, duration, description, and ratings are fetched using the pytube library.
    * Download Handling: The user is asked whether they want to download the video. If they agree, the video is downloaded using yt-dlp.
5. Customization
To download a different video, change the url variable inside the download block to the desired video's URL. You can also modify the ydl_opts to specify different download formats or settings.
This script can be extended or modified to support additional features, such as downloading playlists or handling different formats.
