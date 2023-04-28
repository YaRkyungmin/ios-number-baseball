## iOS 커리어 스타터 캠프

### 숫자야구 프로젝트 저장소

- 이 저장소를 자신의 저장소로 fork하여 프로젝트를 진행합니다

# 숫자 야구 게임
## 📚목차
1. [소개](#1-소개)
2. [팀원](#2-팀원)
3. [타임라인](#3-타임라인)
4. [프로젝트 구조](#4-프로젝트-구조)
5. [실행화면(기능 설명)](#5-실행-화면기능-설명)
6. [트러블슈팅](#6-트러블-슈팅)
7. [참고링크](#7-참고-링크)

## 1. 소개
1부터 9까지의 숫자 중에서 임의로 3개의 숫자를 입력해서
자리와 숫자가 맞으면 스트라이크, 숫자만 맞으면 볼로 판별합니다. 
총 9번의 기회 내에 3 스트라이크를 맞추면 사용자 승리로 게임이 종료됩니다. 

## 2. 팀원

| MINT | 강경민 |
| -------- | -------- | 
|   <Img src = "https://i.imgur.com/ySVlJwk.jpg" width="200" height="200"/>  |  <Img src = "https://i.imgur.com/OSeygFq.png" width="200" height="200"/> |
| <center>Driver, Navigator</center>  | <center>Driver, Navigator</center>     |



## 3. 타임라인
#### 24일
순서도 작성, 흐름 정리
#### 25일
네이밍 공부, 학습자료 공부, 임의의 수를 생성해서 볼과 스트라이크를 판별하는 기능 구현
#### 26일
학습자료 공부, 함수들 리펙토링, 네이밍 수정
#### 27일
readline()으로 숫자를 입력받고 입력된 값에 문제가 없으면 컴퓨터의 임의의 수 3개와 볼, 스크라이크를 판별해서 출력할 수 있도록 구현
#### 28일 
로직 상 불필요한 부분들 리펙토링, 네이밍 수정

## 4. 프로젝트 구조
![](https://i.imgur.com/zwtZfQV.png)

## 5. 실행 화면(기능 설명)
![](https://i.imgur.com/MFGE6IH.gif)

입력 받아 형식에 맞게 입력했는지 확인 후 볼과 스트라이크 판별하는 과정

![](https://i.imgur.com/BRdwDr9.gif)

사용자 승리

![](https://i.imgur.com/QQV0qA7.gif)

게임 종료

## 6. 트러블 슈팅
1. 초반에 맞는 시간대를 찾느라 고생했습니다. 무작정 일단 시간이 되면 할 수 있는 순간까지 하려다가 너무 늦게까지 하게 되어 리뷰어 분과 서포터즈 님께서 조언을 남겨주시기까지 하였습니다. 
2. 짝 프로그래밍에서 기능을 기준으로 나누지 않고 시간을 기준으로 나눠서 함수를 만들다 말고 주는 경우가 있어서 대화가 길어지고 소통에 오류가 있었습니다. 
3. 활동학습의 시간대가 딱 2시 - 5시라 중간에 끊기는 느낌이 아쉬웠습니다.
4. 순서도 작성 경험이 부족해서 로직들의 기능을 모두 분리하여 순서도에 모두 작성 했지만 리뷰어의 조언을 듣고 순서도는 기능들을 추상화해서 전체적인 맥락을 한눈의 파악하기 쉽게 하기 위한 목적이라는 것을 알게됐습니다.
5. 리뷰어의 코멘트를 무조건적인 정답으로 생각하기 보다 그 질문과 코멘트에 대해 생각하고 그에 따른 본인만의 주관을 정리 후 코드를 수정해야한다는 점을 느꼈습니다. 
6. 함수, 프로퍼티의 순서에 대한 고민이 많았습니다. 프로퍼티와 함수 사이의 경우에는 프로퍼티를 먼저 작성하고 함수와 함수들 사이의 순서에서는 구현하는 순서대로 작성하는 것으로 했습니다. 


## 7. 참고 링크
[Optional](https://github.com/apple/swift/blob/main/stdlib/public/core/Optional.swift)
[Control Flow](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/controlflow/#Switch)
[Bool 이름 짓기](https://soojin.ro/blog/naming-boolean-variables)
[Compact Map](https://developer.apple.com/documentation/swift/sequence/compactmap(_:))

