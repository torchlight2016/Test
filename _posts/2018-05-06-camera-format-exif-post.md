---
layout: post
title: "카메라 포맷 Exif "
author: "Chester"
---

카메라로 가로, 세로 방향으로 촬영하더라도 이미지는 동일한 해상도 정보를 가지는 문제가 있습니다.

아래 이미지는 세로 방향으로 촬영한 이미지의 정보입니다.

<img src="/assets/device-2018-03-31-003638.png">

해상도는 4160x2340로 나오지만 이미지 정보에서 방향 정보를 확인할 수 있습니다.

카메라 촬영시 Exif 포맷으로 이미지가 저장되며, 위키백과에서 아래와 같이 나와 있습니다. 
<h4>
교환 이미지 파일 형식 (Exif; EXchangable Image File format)은 디지털 카메라에서 이용되는 이미지 파일 포맷이다. 이 데이터는 JPEG, TIFF 6.0과 RIFF, WAV 파일 포맷에서 이용되며 사진에 대한 정보를 포함하는 메타데이터를 추가한다. Exif는 JPEG 2000, PNG나 GIF 파일에서는 지원하지 않는다.
Exif 메타데이터는 카메라 제조사, 카메라 모델, 회전 방향, 날짜와 시간, 색 공간, 초점 거리, 플래시, ISO 속도, 조리개, 셔터 속도, gps 등의 정보를 제공한다.
</h4>

Exif 포맷은 디지털 카메라 포맷이며, 메타데이터에 회전 방향이 포함되어 있는걸 확인할 수 있습니다.<br>
웹 페이지에서는 img 태그로 이미지를 출력하기 전에 메타데이터를 읽어서 회전시켜야 합니다.  
안드로이드는 glide, picasso 등 유명 이미지 라이브러리를 사용하면 정상적으로 노출됩니다.

직접 메타데이터를 읽어서 회전 처리할 경우 아래 링크를 참고하세요.
<br>[https://android-developers.googleblog.com/2016/12/introducing-the-exifinterface-support-library.html](https://android-developers.googleblog.com/2016/12/introducing-the-exifinterface-support-library.html)

