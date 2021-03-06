
1. Python 2.7 설치
```
brew install python
```

2. cmake 설치
```
brew install cmake
```

3. 환경변수 설정   
```
vi ~/.bash_profile
ANDROID_SDK_ROOT=<경로>
NDK_ROOT=<경로> 
ANT_ROOT=<경로>  
```

4. GitHub에 ssh 공개키 등록. 키가없다면 생성
```
ssh-keygen
```

5. Cocos 프로젝트 클론
```
cd <내컴퓨터 프로젝트 받을 경로>
git clone git@github.com:cocos2d/cocos2d-x.git
git submodule update --init
git submodule update
./download-deps.py
```

6. 새 프로젝트 경로로 이동
```
cd <2에서 받은 깃허브 프로젝트 폴더>
```

7. 환경변수 업데이트
```
./setup.py
source <bash_profile 파일경로>
```

8. Cocos 버전 확인
```
cocos -v
```

9. 새 Cocos 프로젝트 생성
```
cocos new <프로젝트 이름> -p com.your_company.mygame -l cpp -d <새 프로젝트 경로>
```

9-1. MacOS 프로젝트 생성
```
cd <프로젝트 경로>
mkdir mac-build && cd mac-build
cmake .. -GXcode
open Cocos2d-x.xcodeproj
```

9-2. iOS 프로젝트 생성
```
cd <프로젝트 경로>
mkdir ios-build && cd ios-build
cmake .. -GXcode -DCMAKE_SYSTEM_NAME=iOS -DCMAKE_OSX_SYSROOT=iphoneos
open Cocos2d-x.xcodeproj
```

10. 실행
```
cd <프로젝트 경로>/<프로젝트이름>
mkdir build
cd build
cocos run <프로젝트 경로> -p <빌드플랫폼> -m <release or debug>
cocos run .. -p mac -m release
```

7-1. No CMAKE_C_COMPILER could be found 에러
```
sudo xcode-select --reset
cocos run ...
```
