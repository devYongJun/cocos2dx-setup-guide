
1. Python 2.7 설치
```
brew install python
```

2. cmake 설치
```
brew install cmake
```

1. 환경변수 설정   
```
vi ~/.bash_profile
ANDROID_SDK_ROOT=<경로>
NDK_ROOT=<경로> 
ANT_ROOT=<경로>  
```

2. 깃허브에 ssh 공개키 등록. 키가없다면 생성
```
ssh-keygen
```

3. 깃허브 코코스 프로젝트 클론
```
cd <내컴퓨터 프로젝트 받을 경로>
git clone git@github.com:cocos2d/cocos2d-x.git
git submodule update --init
git submodule update
./download-deps.py
./setup.py
```

4. 코코스버전 확인
```
cocos -v
```

4. 새 프로젝트 생성
```
cd <2에서 받은 깃허브프로젝트폴더>
source <bash_profile 파일경로>
cocos new <프로젝트이름> -p com.your_company.mygame -l cpp -d <새 프로젝트 경로>
cd <새 프로젝트 경로>/<프로젝트이름>
mkdir build
cd build
cocos run <프로젝트경로> -p <빌드플랫폼> -m <release or debug>
cocos run .. -p mac -m release
```

4-1. No CMAKE_C_COMPILER could be found 에러
```
sudo xcode-select --reset
cocos run ...
```
