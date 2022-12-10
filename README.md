![header](https://capsule-render.vercel.app/api?type=waving&&color=gradient&height=100&section=header&fontSize=10)
# FoodFighter

## 1. 프로젝트 목적 및 용도

+ 이 프로젝트는 무엇을 위한 것인가
  + 지역별로 있는 맛집들을  별점순, 리뷰순, 검색 등등 체계적으로 알려주는 홈페이지 입니다.
  
+ 어떤 사람들이 이 프로젝트를 사용하면 좋은가
  + 무엇을 먹을지 고민이되는 사용자들에게 이 사이트를 이용하여 해결할수 있게 도와줄수 있습니다.

+ 이 프로젝트는 어떻게 작동하는가
  + 사용자들이 쉽게 볼수있게 AWS 서버 Ubuntu 18.04 / Apache / Tomcat9 / JDK8 / MariaDB 10 / dokuwiki 등을 이용하여 주소창에 입력하면 바로 확인할수 있게 되었습니다.
<br>

## 2. 팀원 소개 및 역할분담
#### 팀장 : 이순영 <br>
#### 팀원 : 윤정민, 박정안, 정미정

  1. 이순영 : AWS 구축, DB 관리 상세 리뷰 페이지 설계 및 제작
  2. 윤정민 : 디자인 총괄, 로그인 및 회원가입, 관리자페이지 관련 설계 및 제작
  3. 박정안 : PPT제작, 메인페이지 및 지역별 소개 페이지 설계 및 제작
  4. 정미정 : 상세정보 검색, 공지사항 페이지 설계 및 제작
<br>

## 3. 기술 스택
<p align="center">
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=HTML5&logoColor=white"/></a> &nbsp
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=CSS3&logoColor=white"/></a> &nbsp
<img src="https://img.shields.io/badge/JAVA-007396?style=flat-square&logo=java&logoColor=white"/></a> &nbsp
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=white"/></a> &nbsp
<img src="https://img.shields.io/badge/jquery-0769AD?style=flat-square&logo=jquery&logoColor=white"/></a> &nbsp
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/></a> &nbsp
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=Node.js&logoColor=white"/></a> &nbsp
<img src="https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=MariaDB&logoColor=white"/></a> &nbsp
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/></a> &nbsp 
<img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=flat-square&logo=Amazon%20AWS&logoColor=white"/></a> &nbsp 
<img src="https://img.shields.io/badge/ApacheTomcat-F8DC75?style=flat-square&logo=ApacheTomcat&logoColor=white"/></a> &nbsp
</p>
<br>

## 4.프로젝트 폴더 구조
<br>
<details>
<summary>Project Folder</summary>
<br>
  <div markdown="1">
  
```
🗃 문서 폴더 구조 
📁WebContent  
├── top.jsp 
├── bottom.jsp
├── imsi.jsp
├── index.jsp
│   
├── 📁admin
│   ├── gongji_delete.jsp
│   ├── gongji_view.jsp
│   ├── member_chg.jsp
│   ├── member_view.jsp
│   ├── review_delete.jsp
│   └── review_view.jsp
│   
├── 📁content     
│   ├── detail.jsp
│   ├── review_detail.jsp
│   ├── review_ok.jsp
│   ├── review_update_ok.jsp
│   └── review_update.jsp
│    
├── 📁gongji
│   ├── content.jsp
│   ├── delete.jsp
│   ├── list.jsp
│   ├── readnum.jsp 
│   ├── write_ok.jsp 
│   └── write.jsp
│    
├── 📁localsearch
│   └── localsearch.jsp
│    
├── 📁login
│   ├── login_ok.jsp
│   ├── login.jsp
│   ├── logout.jsp
│   ├── resign.jsp
│   ├── userid_check_ok.jsp
│   ├── userid_check.jsp
│   ├── userpwd_check_ok.jsp
│   └── userpwd_check.jsp
│    
├── 📁main    
│    └── main.jsp
│    
├── 📁mypage   
│   ├── mypage_end.jsp
│   ├── mypage.jsp
│   ├── pwd_change_end.jsp
│   ├── pwd_change_ok.jsp 
│   ├── pwd_change.jsp 
│   ├── update_ok.jsp
│   ├── user_delete_ok.jsp
│   └── user_delete.jsp 
│
├── 📁search
│   ├── error.jsp
│   └── search.jsp
│
├── 📁signup
│   ├── captcha_audio.jsp
│   ├── captcha_img.jsp
│   ├── captcha_submit.jsp 
│   ├── signup_end.jsp
│   ├── signup_ok.jsp
│   ├── tos.jsp
│   └── userid_check.jsp
│  
├── 📁css
│   ├── content.css
│   ├── localsearch.css
│   ├── main.css 
│   └── search.css
│   
└── 📁js
    ├── content.js
    └── search.js
    
    
🗃 Dao, Dto 폴더 구조               
📁src    
├── 📁com.foodfighter.content
│   ├── ContentDao.java
│   ├── ContentDto.java
│   ├── ImageDto.java
│   └── MenuDto.java
│   
├── 📁com.foodfighter.gongji
│   ├── GongjiDao.java
│   └── GongjiDto.java
│   
├── 📁com.foodfighter.review
│   ├── ReviewDao.java
│   └── ReviewDto.java
│   
├── 📁com.foodfighter.util
│   ├── AudioCaptCha.java
│   ├── CaptCha.java
│   └── SetTextProducer.java
│   
├── 📁foodfighter.main
│   ├── MainDao.java
│   └── MainDto.java
│   
├── 📁foodfighter.searchlocal
│   ├── SearchlocalDao.java
│   ├── SearchlocalDto.java
│   └── SearchpageDto.java
│   
├── 📁food
│   ├── FoodDao.java
│   └── FoodDto.java
│   
└── 📁search
    ├── Search.java
    └── SearchRestaurant.java
```
</div>
</details>
<br>


## 5. 사진
![198678337-5ce4632c-9da5-42e4-927f-80fd4ab79870](https://user-images.githubusercontent.com/56786339/198813815-3e2fa0b1-4b75-433e-8490-13622d7ac716.png)
![198678502-6bda3db7-85a7-4583-8907-4bc5bfa0cf34](https://user-images.githubusercontent.com/56786339/198813816-73921944-3f5a-4c9c-8b8e-5ea6cbec9390.png)



## 6. FoodFighter PPT
[PPT ](https://drive.google.com/file/d/1q3n8m-GLqOhiPH6eOW8Iv0RlMmUywze0/view?usp=sharing)



## 7. 프로젝트 바로가기
#### 노션을 이용한 프로젝트 관리
+  [푸드파이터 노션 바로가기](https://galvanized-jackal-cd2.notion.site/ba59ae10199e40789254536868868c84)
+  [회의록 / 일정](https://galvanized-jackal-cd2.notion.site/e1f51b195ae24d2395388a9fb1785829?v=731bc292746d4945a9c254cf98027791) 
+  [아이디어 조사](https://galvanized-jackal-cd2.notion.site/50e4ffbf2e8845b58caa07b8483d651c?v=d91a49fcbeda49c3aa9f9a63f7086d29) 
+  [작업 현황](https://galvanized-jackal-cd2.notion.site/7f2ce6e1952d400ca1058b5454c1f225?v=eed1c16b7a9c42f6815c1cbf22156d2a) 
+  [게시판](https://galvanized-jackal-cd2.notion.site/bf9f86a8828f46aaa67d10f79d25baa9?v=b9b32dc6e86045b19e8a300f0404b2eb) 
+  [분석한 사이트](https://galvanized-jackal-cd2.notion.site/0546d030a7c949419cb000384f70a673?v=4e8d3334a9d94ff09ff1e7935cde70e6)





![footer](https://capsule-render.vercel.app/api?type=waving&&color=gradient&height=100&section=footer&fontSize=90)
