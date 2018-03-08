# 안드로이드 관련 설정 파일들

---

## ./AndroidManifest.xml

https://developer.android.com/guide/topics/manifest/manifest-intro.html?hl=ko

앱의 각종 정보들과 동작환경에 대한 옵션들들 지정

---

## ./assets
앱에서 사용되는 각종 애셋 파일들이 들어있는 폴더
폰트, 이미지 파일, 텍스트 파일, 바이너리 파일 등...
파일접근으로 가져다 사용하게 된다.
``ex: InputStream ims = getAssets().open("avatar.jpg");``

---

## ./jniLibs
NDK를 통해 빌드된 native library들이 들어있는 폴더
빌드시 cpu별로 빌드되어 각각 다른 폴더에 저장된다.
arm5, armeabi, x86, x64_64 등 32bit와 64bit cpu를 고려 해 주어야 한다.

---

## ./res
앱에서 사용되는 리소스들이 디바이스 환경별로 구분되어 사용 하기위해 해상도별, 지역별로 구분된 디렉터리들이 있다.

#### ./res/anim
애니메이션되는 이미지 객체

#### ./res/drawable-
이미지 객체(bmp,png,jpg등...)
벡터 드로잉 변환 객체(xml)

#### ./res/layout
액티비티의 View layout을 구성하는 설정파일들
xml파일들을 선택하여 화면구성을 편집할수 있다.
(버튼, 스크롤뷰, 각종 ui component)

#### ./res/menu
액티비티의 메뉴 구성파일들이 있다. 선택하여 편집가능.

#### ./res/mipmap-
런처 화면에서 디바이스 화면 해상도에 따라 다르게 보여질 아이콘들

#### ./res/raw
음악파일, 동영상파일, 텍스트파일 등 원본 리소스로서 접근해 사용하기 위한 파일들이 들어있는 폴더.
파일접근이 아닌 리소스 접근 형식으로 사용된다.
``ex: InputStream in = getResources().openRawResource(R.raw.name)``

#### ./res/values-
디바이스 지역별로 구별되어 사용되는 텍스트들이 저장되는 폴더.
주로 메뉴,텍스트 메시지 등의 값이 이에 속한다.

#### ./res/xml

---
