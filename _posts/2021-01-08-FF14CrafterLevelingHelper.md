---
layout: post
title:  "(개인) FF14 Crafter Leveling Helper"
date:   2021-12-19
excerpt: "퍼즐 액션 게임 개발"
project: true
tag:
- jekyll 
- moon
- blog
- about
- theme
comments: true
---
<center><b>FF14 Crafter Leveling Helper</b></center>
     
### 프로젝트 제목
FF14 Crafter Leveling Helper

### 프로젝트 기간
2021-12-12 ~ 2021-12-19

### 프로젝트 목표 및 내용
* 목표
	파이널판타지14 현재 내 레벨과 남은 경험치에 따라 레벨링 루트에 따른 필요한 제작 개수를 산출하자.

* 내용
	새로운 확장팩이 나왔는데 제작직 레벨링하는데 필요한 재료 개수 세기가 너무 귀찮았던 나머지 자동으로 계산해주는 프로그램을 만들어보기로 결심.
	현재 내 경험치, 소장품 납품 경험치, 길드의뢰 납품 경험치 등을 REST API로 가져와 데이터를 재가공해서 보여준다.

---

### 팀 규모 및 역할
* 1인 개발
나재흠 : 앱 기획 및 프로그램 개발

### 나의 역할 및 기술 스택
#### Android Studio / Java / Python3  
* FF14 REST API 문서에는 Java에 대한 정보가 없기 때문에 Java로 개발하기 위한 방법을 찾아보면서 Python으로 프로토타입을 만들어 요청 보낼 URL을 완성하고 테스트.
* 안드로이드 레이아웃 구성, 안드로이드 앱 개발
* 필요한 데이터를 선언하고 요청받은 raw 데이터를 필요한 부분만 재가공


### 이 프로젝트를 통해 배운점
*  REST API의 사용법을 알게 되었음.
*  Document에서는 정보가 너무 적어 개발자 discord에 들어가 정보를 얻으면서 문서의 중요성과 다른 개발자들과의 소통의 중요성을 깨닫게 됨.

---

### 소스 저장소
* [FF14_Crafter_Leveling_Helper](https://github.com/Meerkat-GMD/FF14_Crafter_Leveling_Helper)
* [FF14Helper 발표자료.pdf](https://github.com/Meerkat-GMD/FF14_Crafter_Leveling_Helper/files/9140412/FF14Helper.pdf)

### Preview
![image](https://user-images.githubusercontent.com/18138559/179735139-a3b62eb5-cfb0-4d7a-9e3c-5e07d2fa20c0.png)