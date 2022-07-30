---
layout: post
title: (iOS) PocketSong
tags: [iOS]
---

# PocketSong

---

<p align="left">
    <img src="https://img.shields.io/badge/Xcode-11.0-blue">
    <img src="https://img.shields.io/badge/iOS-13.2-green">
</p>

![9787F746-E2FC-4C97-8868-9A0AF2956601.png](/assets/PocketSong/Imgs/9787F746-E2FC-4C97-8868-9A0AF2956601.png)

> PocketSong is recoding the music and show the record based on location information.


## Using Frameworks and Libraries

- [ShazamKit](https://developer.apple.com/shazamkit/) : record musics
- [CLTypingLabel](https://cocoapods.org/pods/CLTypingLabel) : show typing effect on labels
- [SQLite](https://www.sqlite.org/index.html) : save music data you recorded
- [Mapkit](https://developer.apple.com/documentation/mapkit/): show the position where you record songs

## Prerequisite

---

1. Install frameworks and library
    
    ```jsx
    cd PocketSong
    pod install
    ```
    

## Storyboard

---

Storyboard

![스크린샷 2022-07-31 오전 4.30.37.png](/assets/PocketSong/Imgs/_2022-07-31__4.30.37.png)

## ViewControllers

---

1. MyMemoriesViewController
    
    ![6178A997-4A29-44B1-95A9-C0FA17BAC451.png](/assets/PocketSong/Imgs/6178A997-4A29-44B1-95A9-C0FA17BAC451.png)
    
    : It shows positions where you record the song. 
    
2. CatchSongViewController
    
    ![E79C846F-8481-4682-A6A2-F309EC27D651.png](/assets/PocketSong/Imgs/E79C846F-8481-4682-A6A2-F309EC27D651.png)
    
    : It record the song what you hear. If the process is success, it will show the result consists of song information, your present location and time. Also, you can insert a comment you want anything.
    
3. SongListViewController
    
    ![A37C92BA-CFE7-4192-B6CA-55FE7DCACDD8.png](/assets/PocketSong/Imgs/A37C92BA-CFE7-4192-B6CA-55FE7DCACDD8.png)
    
    : It shows songs list classified with the date. This ViewController uses TableView and CollectionView. TableViewCell is shown by date and CollectionView consists of that songs.
    

## Notice

---

PocketSong uses Microphone and GPS. Therefore when you launch the app first, it requires permissions. Please Accept it if you want to use this app.
