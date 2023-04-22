---
layout: post
title: Open your window
date: 2023-02-05 00:00:00 +0300
image: project02/project02_cover.jpg
tags: TeamProject
description: 내 방 침대에 누워 세계 곳곳의 풍경을 구경하고 NASA에 선별한 일자별 우주 사진까지 확인할 수 있습니다. 나의 창밖 풍경을 공유하거나 마음에 드는 사진은 아카이빙하고 미니 게임도 즐길 수 있는 종합 힐링 서비스입니다.
---

## About

내 방 침대에 누워 세계 곳곳의 풍경을 구경하고 NASA에 선별한 일자별 우주 사진까지 확인할 수 있는 힐링 서비스. 나의 창밖 풍경을 공유하거나 마음에 드는 사진은 아카이빙하고 미니 게임도 즐길 수 있습니다.

#### Duration

2023/01/26 ~ 2023/02/04

#### Team

Full Stack 2

---

## 🛠️ Skills & Libraries

#### Backend, DB, Server

_Node.js, Express.js, Sequelize, MySql, AWS(EC2)_

#### Frontend

_React, Redux, JavaScript, Axios, Ajax_

#### Communication

<a href="https://github.com/nietzche15/windowToUNIVERSE" target="_blank">GitHub</a>,
<a href="https://www.figma.com/file/B1zA8TGk9QMuP7NWl42Efv/windowToUNIVERSE?node-id=0-1&t=EvOZ0GwbLocrViJs-0" target="\_blank">Figma</a>,
<a href="https://www.notion.so/scientific-hibiscus/window-to-UNIVERSE-18bb09e530414b31988cac9d4009fbb7" target="_blank">Notion</a>
, Whale

---

## 🌐 Flow Chart & ERD

![]({{ site.baseurl }}/images/project02/project02-FC.png)
_Flow Chart_

---

## 🙋🏻‍♀️ 담당 기능

#### 💻 NASA APOD API

- ##### API data의 비동기 처리

&emsp;&ensp; **-요청한 data loading 상태 관리 (Redux의 Thunk & Slice)**

#### 💻 회원가입 & 로그인

- ##### 회원 정보 data 무결성 확보

&emsp;&ensp; - Email 중복 확인  
&emsp;&ensp; - Password 암호화 (bcrypt)  
&emsp;&ensp; - Email, Password, Phone 정규식 확인

- ##### 소셜 로그인

&emsp; - 카카오톡 로그인 (passport)

#### 💻 미니 게임 - Hangman 제작

&emsp; - 게임 로직

---

<details>
<summary>📖 Content Details</summary>
<div markdown='1'>

### [ NASA APOD API ]

##### NASA에서 매일 업로드하는 우주의 image/video 정보를 알 수 있는

##### Astronomy Picture of the Day (APOD) API 를 사용해 페이지 구성

## ![]({{ site.baseurl }}/images/project02/project02-API-APOD.png)

##### 1. data가 pending 상태 일때 loading icon을 띄운다.

- 요청한 data의 상태를 pending/fulfilled/rejected로 나눠서 관리한다.
- fulfilled 전까지 laoding = true 로 상태를 설정하여 loading icon 을 띄운다.

##### 2. 처음 접속 시, date 를 공백처리해 deafult 값인 오늘의 data를 받는다.

- title, explanation, url, media_type
- media_type에 따라  
  &emsp;&emsp; video 인 경우 videoContainer(iframe) 삽입  
  &emsp;&emsp; image인 경우 background-image 설정

##### 3. datepicker

- datepicker 날짜 선택 시, value 형식 (YYYY/MM/DD) 을 API 형식(YYYY-MM-DD)으로 변환하여 새 Data 요청
- datepicker의 range 를 data가 존재하는 1995-06-16 이후 ~ 오늘 이전으로 설정

### [ 회원 DB 설계 ]

##### 회원 정보

## ![]({{ site.baseurl }}/images/project02/project02-API-sign.png)

- 입력받는 회원 정보는 정규식을 통해 검증  
  &emsp;&emsp; Email, 닉네임, 비밀번호, 전화번호
- Email 은 중복 확인하여 저장
- 비밀번호는 bcypt로 암호화하여 관리

##### 소셜 로그인 - 카카오톡

- passport-kakao 모듈 이용

### [ 미니게임 로직 ]

</div>
</details>

## 📙 Pages

#### 🔎 메인 Page

![]({{ site.baseurl }}/images/project02/project02-main.png)
_Main_

#### 🔎 UNIVERSE Page

![]({{ site.baseurl }}/images/project02/project02-universe-main.png)
_Universe Main (media_type=image)_

![]({{ site.baseurl }}/images/project02/project02-universe-video.png)
_Universe Main (media_type=video)_

#### 🔎 Hangman Game Page

![]({{ site.baseurl }}/images/project02/project02-universe-game.png)
_Universe Game Main_

![]({{ site.baseurl }}/images/project02/project02-universe-game-2.png)
_Universe Game Page_

#### 🔎 WINDOW Page
