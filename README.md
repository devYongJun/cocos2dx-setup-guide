
1. 깃에 ssh 공개키 등록. 키가없다면 생성
```
ssh-keygen
```
2. 깃 프로젝트 클론
```
cd <내컴퓨터 로컬 경로>
git clone git@github.com:cocos2d/cocos2d-x.git
git submodule update --init
git submodule update
./download-deps.py
```

3. 개발툴 경로 설정
ANDROID_SDK=
NDK_ROOT=
ANT_ROOT=

