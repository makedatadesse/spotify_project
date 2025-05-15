# Spotify API for Archiving Taste

## Description: 
This project sets the foundation for the long term data collection and archiving of my personal user data in the form of my most listened to songs of the past year (April 2024 – April 2025) through SpotiPy, a third party Spotify linked API specifically for Python. Spotify has recently deprecated access to many of their most interesting request features – specifically audio_features and genres – which in turn deprecated access to such requests through SpotiPy as well. To circumvent this, the MusicBrainz API was linked to pull genre information for each track.

## Rationale: 
This project is meant to be an ongoing replicable code for keeping a record of songs and artists listened to the most for each passing year. Emulating Spotify’s Wrapped – which is only accessible by users for the two months following – this project is meant to be an improvement of the feature by allowing the ability to save, archive, and thus retrieve, listening history. Consciously we can make assumptions about the type of music we prefer to listen to, but the data of who we are through what we listen to can provide us with a clearer story.

## Workflow/Required Libraries: 
### Many libraries were used in this project only as supplements, the most notable and important to run this code:
      spotipy (to access Spotify API through Python)
      musicbrainzgs (to access unique artist IDs and pull genre data)
      time (for breaks between calls to musicbrainzgs API)
      json, base64, pandas (for parsing and database building)

## Further uses: 
With proper API Key authentication through Spotify, the entirety of this code is replicable (customizations should be made in the manual assigning of genres). Interested code builders may consider utilizing the recently listened to feature to join with spatial data and analyze music listening habits by locations and movement (change scope in Authorization from user-top-read).  The goal would be to have the program recognize the type of music being listened to at home versus in transit versus at work, in different parts of the city, at different times of the day. Geospatial location tracking tools with time stamps are possible, but to uphold some data privacy, manual user-based tracking may be preferred.

## Files list: 
  MusicBrainz x SpotiPy + LONG TERM.ipynb: Python Notebook – Main parent script containing requests, API calls, table cleaning, API joins, and visualizations for main analysis on Long-Term 
  requests   
        Correlated Files:
            df_tracks_new.csv – stemmed from df_tracks DataFrame, exported and reuploaded as .csv to manually search and enter MBID codes for each artist
            condensed_new.csv – re-exported to manually enter binary on explicit/clean and 1-100 scores for ‘energy,’ ‘danceability,’ and ‘happiness.’ Re-uploaded to create mood_data DataFrame 
            for Mood Plot visualization.






TL;DR: Pulling from Spotify API to and visualizes personal user data
