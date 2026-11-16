# YouTube to Spotify workflow

1. Capture the public YouTube video titles and IDs in source order. Keep the uploader and video duration when they help identify a recording. Note private or unavailable videos separately if YouTube shows them.
2. Match each song by artist and title in Spotify. When there are several recordings, check details such as the mix, live performance, soundtrack, and duration. For an identifiable full album, place its tracks in album order at that video's position.
3. Review unmatched entries with targeted searches for spelling variants, censored titles, and collaborations. Leave uncertain matches out and record them separately.
4. Preserve YouTube order. For a channel import by year, use the video's YouTube publication year, keep the newest upload first within each year, and remove repeats within that year. The David Dean Burkhart import used YouTube's ordered video index and checked the year boundaries against public video publication dates.
5. Add the verified matches in batches. Respect Spotify's rate-limit response and check the playlist's current contents before resuming an interrupted write to avoid duplicate inserts.
6. Read back the complete playlist and compare the recorded Spotify track IDs and order. Check the reported visibility and log any discrepancy.
7. Record the playlist link, source and scope, playlist track count, and exclusions in the [playlist index](playlists.md). For a title export, use UTF-8 plain text with one original YouTube title per line. The yearly exports include the unmatched titles so they reproduce the complete source list.

Commit only the intended log files. Inspect the staged diff before pushing.
