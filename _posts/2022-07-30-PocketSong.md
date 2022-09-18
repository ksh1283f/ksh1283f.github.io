# 2022-07-30-PocketSong (Korean)

# PocketSong

---

<p align="left">
    <img src="https://img.shields.io/badge/Xcode-11.0-blue">
    <img src="https://img.shields.io/badge/iOS-13.2-green">
</p>

![https://github.com/ksh1283f/ksh1283f.github.io/blob/main/assets/PocketSong/Imgs/PocketSongScreenShot.png?raw=true](https://github.com/ksh1283f/ksh1283f.github.io/blob/main/assets/PocketSong/Imgs/PocketSongScreenShot.png?raw=true)

> PocketSongd은 음악을 통해서 추억을 기록할 수 있는 앱입니다. 주위에서 나오는 음악을 판별해주고 관련 상세 정보들을 기록합니다. 해당 음악을 위치 정보를 이용해서 지도 위에 표시해줍니다.
> 

## Using Frameworks and Libraries

- [ShazamKit](https://developer.apple.com/shazamkit/) : 음악을 판별해주는 기능을 제공합니다.
- [Kingfisher](https://github.com/onevcat/Kingfisher): ImageView에 이미지를 다운로드 또는 캐싱을 통해서 비동기로 적용해줍니다.
- [FlyoverKit](https://github.com/SvenTiigi/FlyoverKit): 공중에서 360도로 회전하는 뷰를 `MKMapView` 위에서 제공합니다.
- [SnapKit](https://github.com/SnapKit/SnapKit): 가독성이 높은 코드로 오토레이아웃을 작성할 수 있게 합니다.
- [lottie-ios](https://github.com/airbnb/lottie-ios):  `Lottie` 파일을 앱에서 사용할 수 있게 해줍니다.
- [BottomHalfModal](https://github.com/mercari/BottomHalfModal): Half modal view를 상위 ViewController 위에 띄워줍니다.
- [SQLite](https://www.sqlite.org/index.html) : 기록한 음악 정보의 CRUD 기능을 제공합니다.
- [Mapkit](https://developer.apple.com/documentation/mapkit/): 기록한 음악들의 위치를 보여줍니다.

## Prerequisite

---

1. 실행 전 필요 라이브러리 셋팅
    
    ```jsx
    cd PocketSong
    pod install
    ```
    

## Storyboard

---

![https://github.com/ksh1283f/ksh1283f.github.io/blob/072284ab3199a1f0beb75205278f34ed9a90d925/assets/PocketSong/Imgs/Storyboard.png?raw=true](https://github.com/ksh1283f/ksh1283f.github.io/blob/072284ab3199a1f0beb75205278f34ed9a90d925/assets/PocketSong/Imgs/Storyboard.png?raw=true)

## Onboarding

---

![https://github.com/ksh1283f/ksh1283f.github.io/blob/06af9a14ad11e44a66657075f4ee78d949d91577/assets/PocketSong/Imgs/PocketSongOnboarding.png?raw=true](https://github.com/ksh1283f/ksh1283f.github.io/blob/06af9a14ad11e44a66657075f4ee78d949d91577/assets/PocketSong/Imgs/PocketSongOnboarding.png?raw=true)

## ViewControllers

---

1. MyMemoriesViewController
    
    ![https://github.com/ksh1283f/ksh1283f.github.io/blob/cc39401addb524d8740bbb5cac2c873532d5171c/assets/PocketSong/Imgs/MyMemoriesVC.gif?raw=true](https://github.com/ksh1283f/ksh1283f.github.io/blob/cc39401addb524d8740bbb5cac2c873532d5171c/assets/PocketSong/Imgs/MyMemoriesVC.gif?raw=true)
    
    기록했던 음악의 정보를 아트워크 아이콘으로 보여줍니다. 또한 아트워크를 터치 시 해당 음악의 상세정보를 새로운 뷰로 보여줍니다. 또한 아이콘들이 서로 겹칠 경우 클러스터링 기능을 통해서 통합하여 겹친 아이콘의 개수로 표현합니다. 이 새로운 아이콘을 터치할 경우 통합된 아이콘들을 Half modal view를 새로 만들어서 보여줍니다.
    
2. CatchSongViewController
    
    ![https://github.com/ksh1283f/ksh1283f.github.io/blob/cc39401addb524d8740bbb5cac2c873532d5171c/assets/PocketSong/Imgs/CatchSongVC.gif?raw=true](https://github.com/ksh1283f/ksh1283f.github.io/blob/cc39401addb524d8740bbb5cac2c873532d5171c/assets/PocketSong/Imgs/CatchSongVC.gif?raw=true)
    
    마이크를 이용해서 주위에서 나오는 음악을 판별합니다. 이때 마이크 권한이 활성화되어 있지 않다면 설정창으로 이동시켜 마이크의 권한을 활성화할 수 있도록 해줍니다. 권한이 활성화되면, ShazamKit을 이용해서 음악의 정보를 식별하고 프로세스가 완료되면 판별된 음악의 정보와 이때의 위치 및 시간 정보를 같이 보여줍니다. 또한 이용자가 원하는 코멘트를 달 수 있도록 합니다.(단, 코멘트가 필수사항은 아닙니다.) 모든 과정을 완료하고 밑의 파란색의 Record 버튼을 터치하면 기록이 완료됩니다.
    
3. SongListViewController
    
    ![https://github.com/ksh1283f/ksh1283f.github.io/blob/cc39401addb524d8740bbb5cac2c873532d5171c/assets/PocketSong/Imgs/SongListVC.gif?raw=true](https://github.com/ksh1283f/ksh1283f.github.io/blob/cc39401addb524d8740bbb5cac2c873532d5171c/assets/PocketSong/Imgs/SongListVC.gif?raw=true)
    
    날짜별로 기록했던 음악들을 분류해서 보여줍니다. 해당 ViewController는 테이블 뷰와 각 테이블 뷰의 셀에 컬렉션뷰를 포함합니다. 테이블 뷰의 셀은 날짜로 구성되고 컬렉션 뷰의 셀은 해당 날짜의 노래로 구성됩니다.
    

## Notice

---

PocketSong 앱은 마이크와 GPS기능 을 사용합니다. 그러므로 앱을 처음 실행했을 때는 관련된 권한을 요구합니다. 앱을 사용하기 위해서는 이 권한들을 허용해주시기 바랍니다.
