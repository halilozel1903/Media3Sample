# Media3 Android Sample 🎥 📸 📺

![Screenshot](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg4xS6qkXGiJs4EAhcrM38RaEvqOC2n7qTnv-tBylczHyOXOtUBMKdZoe3eI2HAD61mvUak1yP1QsU7aZaoXwoTjvZhZixQ7qvnEu2MCMYjoI84uMOO8VsUpNCb2v8YJ4FRIGaxTqGdAp4WrDTB6DbINkiRPi4LKLD0-tSSsAtkKkYCCd5ob_LDj6xf/s1600/header-Android%20-%20Media3%20is%20ready%20to%20play.png)

The code is for an Android app that plays videos using ExoPlayer, a media player library for Android. The app has a single activity, MainActivity, which is responsible for creating and managing the player, as well as handling playback events.

## Importing Necessary Packages:

The code begins by importing the necessary packages, including the core Android packages, the ExoPlayer library, and the data binding library.

## Creating the Data Source Factory:

A data source factory is created using the `DefaultHttpDataSource.Factory` class. This factory will be used to create data sources for the player, which are responsible for fetching video data from the internet.

## Initializing the Player:

The `initPlayer()` function initializes the ExoPlayer instance. It first creates a new ExoPlayer object using the ExoPlayer.Builder class. Then, it creates a MediaSource object based on the provided media URL. The media URL can be either a regular MP4 file or an HLS playlist. Finally, it sets the media source on the player, prepares the player, and adds a listener to handle playback events.

## Handling Media Source Creation:

The `getHlsMediaSource()` and `getProgressiveMediaSource()` functions create MediaSource objects for HLS playlists and regular MP4 files, respectively. Both functions use the dataSourceFactory to create data sources for fetching video data.

## Managing Player Playback:

The `releasePlayer()`, `pause()`, and `play()` functions are used to control the playback of the video. The `releasePlayer()` function releases the player resources, the `pause()` function stops playback, and the `play()` function resumes playback.

## Restarting the Player:

The `restartPlayer()` function seeks the player to the beginning of the video and then resumes playback. This function is called when the playback ends.

## Handling Playback Events:

The playerListener object implements the Player.Listener interface and is used to handle playback events. The `onPlaybackStateChanged()` method is called when the playback state changes. It handles the following playback states:

`STATE_ENDED`: Restarts the video playback
`STATE_READY`: Starts playback and sets the player view
`STATE_BUFFERING`: Does nothing
`STATE_IDLE`: Does nothing

## Defining Media URLs:

The `MEDIA_URL` and `MEDIA_URL_HLS` constants define the URLs of the videos to play. The MEDIA_URL is for a regular MP4 file, while the MEDIA_URL_HLS is for an HLS playlist.

## Summary:

The provided code demonstrates how to use ExoPlayer to play videos in an Android app. It covers the creation of the player, handling of media sources, playback controls, and event management

## Screenshots 🖼
<img src="https://github.com/halilozel1903/Media3Sample/blob/master/screen-one.png" width="250"/> || <img src="https://github.com/halilozel1903/Media3Sample/blob/master/screen-two.png" width="250"/> || <img src="https://github.com/halilozel1903/Media3Sample/blob/master/screen-three.png" width="250"/>

## Donation 

You can support by buying a coffee. ☕️

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/halilozel1903)

## License ℹ️
```
MIT License

Copyright (c) 2023 Halil OZEL

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```