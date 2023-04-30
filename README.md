# ⚾︎숫자 야구 게임
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
| <center>[github profile](https://github.com/mint3382)</center>  | <center>[github profile](https://github.com/YaRkyungmin)</center>     |

<\br>

## 3. 타임라인: 시간 순으로 프로젝트의 주요 진행 척도를 표시



| 4월 24일 | 순서도 작성, 흐름 정리  |
| ---- | --------------------------------------------------------------------------------------------------------------------------------- |
| **4월 25일** | <center>**네이밍 공부, 학습자료 공부, 임의의 수를 생성해서 볼과 스트라이크를 판별하는 기능 구현**</center> |
| **4월 26일** | <center>**학습자료 공부, 함수들 리펙토링, 네이밍 수정**</center> |
| **4월 27일** | <center>**readline()으로 숫자를 입력받고 입력된 값에 문제가 없으면 컴퓨터의 임의의 수 3개와 볼, 스크라이크를 판별해서 출력할 수 있도록 구현**</center> |
| **4월 28일** | <center>**로직 상 불필요한 부분들 리펙토링, 네이밍 수정**</center> |

<\br>


## 4. 시각화된 프로젝트 구조(다이어그램 등)
![](https://i.imgur.com/zwtZfQV.png)

<\br>

## 5. 실행 화면(기능 설명)

| 볼과 스트라이크를 판별하는 화면 | 정답이 3,2,1 일때 사용자 승리가 나타나는 화면 | 게임 종료 선택 시 나타나는 화면 |
| -------- | -------- | -------- |
| ![](https://i.imgur.com/lzen1LZ.gif)| ![](https://i.imgur.com/MPVZKuu.gif) | ![](https://i.imgur.com/kM6F6aS.gif) |


<\br>

## 6. 트러블 슈팅

### 함수 배치 순서
함수, 프로퍼티의 순서에 대한 논의가 있었습니다.프로퍼티와 함수 중 무엇을 먼저 작성하느냐에 대한 고민과 함수와 함수들 사이의 순서에 대한 고민이 있었습니다. 단순히 생각나는 대로 함수를 작성했기에 순서가 정리되지 않은 느낌이 강했는데 서로 다른 두 곳에서 쓰는 경우 어디에 놓는 것이 적절한지에 대한 문제였습니다. 

-> 프로퍼티와 함수의 경우 프로퍼티를 먼저 선언하고 함수 내에서 사용하는 것이기에 프로퍼티를 먼저 작성하는 것으로 하였습니다. 그리고 함수의 순서는 실현되는 과정에서 호출 하는 순으로 작성하는 것이 코드만 보았을 때 과정을 따라가기 좋을 것 같아 그렇게 작성하였습니다. 

### while flag
재귀함수와 while true는 되도록 사용하지 않는 것이 좋다, 라는 말에 꽂혀서 무조건적으로 flag를 남발하는 문제가 있었습니다. 사실상 while true와 다를 것이 없는 부분조차 flag로 처리했는데 이 부분에 대한 고민이 많았습니다. 이렇게 쓰면 flag의 형식을 지닌 while true인데 과연 더 나은 선택이 맞는지, 이보다 더 좋은 방법이 무엇일지에 대한 고민이었습니다. 

-> while true가 들어갈 부분을 위에 변수로 다른 조건을 하나 줘서 해결했습니다. 빈 배열을 선언 후 그 빈 배열 안 요소들의 개수가 3개가 되면 while문을 탈출합니다. 요소들의 개수가 3개가 되려면 기존의 예외 사항들을 전부 지나와야하기에 탈출의 조건이 될 수 있었습니다. 

### 네이밍
대부분의 것들에 대한 네이밍을 고민했지만 그 중에서도 Bool 타입의 네이밍과 관련하여 생각하는 시간이 길었습니다. be 동사로 시작해야 하기에 초반 isLeftChance를 사용하였는데 마땅한 표현인지에 대한 의문이 있었습니다. 또한 남은 기회에 대한 네이밍으로 Chance만 사용했는데 앞에 Left라던가 하는 단어가 붙는 것이 조금 더 네이밍 컨벤션에 맞는 네이밍인지에 대한 궁금증도 있었습니다. 

-> 리뷰어께서 Bool 타입의 네이밍과 관련한 자료를 남겨주셨습니다. 함수를 수정하면서 네이밍도 여러번 수정하였는데 최종적으로는 isRemainingChance라는 이름으로 변경하였습니다.

### generateRandomNumber()
```swift
func generateRandomNumber() -> [Int] {
    var randomNumbers = Set<Int>()

    while randomNumbers.count < 3 {
        randomNumbers.insert(Int.random(in: 1...9))
    }
    return Array(randomNumbers)
}
```
random메서드를 통해 임의의 수를 추출한후 set에 담아서 중복되지 않은 3개의 임의의 배열을 넘겨주는 방식으로 구현하였습니다. random메서드가 우연치 않게 중복 된 수를 계속 반환할 시 의도치않게 계속해서 while문을 반복해야 한다는 사실에 대해 알게 됐습니다.


#### -> 1차 수정 

```swift
func generateRandomNumber() -> [Int] {
    var randomNumbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
    var ouputNumbers = [Int]()

    for index in (6...8).reversed() {
        let outIndex = Int.random(in: 0...index)
        ouputNumbers.append(randomNumbers[outIndex])
        randomNumbers.remove(at: outIndex)
    }
    return ouputNumbers
}
```
Set 타입을 사용하지 않기 위해서 위와 같이 코드를 변경하였습니다. 다만 불필요한 변수, 상수를 선언해줘야했으며 중간에는 6...8이라는 하드코딩적인 부분도 존재했습니다. 그리고 remove(at:)메서드 시간복잡도가 O(n)이라는 것을 깨닫고 기존에 구현했던 함수와 비교했을때 시간복잡도 차이가 없다는 것을 알게 되었습니다. 
time complexcity : O(n^2)

#### -> 2차 수정
```swift
func generateRandomNumber() -> [Int] {
    var randomNumbers = Array<Int>(1...9)
    randomNumbers.shuffle()
    return Array(randomNumbers[1...3])
}
```
기존 코드로 돌리는 방법도 있었지만 shuffle이라는 힌트를 받아 변경해보았습니다. shuffle 메서드는 배열을 무작위적으로 섞어주는 역할을 하기에 이를 통해 배열을 섞고 필요한 숫자 3개만 ArraySlice를 한다음 Array로 변환해서 반환해줬습니다. 코드도 더 간결해지고 시간복잡도도 줄일 수 있었습니다.
time complexcity : O(n)

<\br>

## 7. 참고 링크
[Optional](https://github.com/apple/swift/blob/main/stdlib/public/core/Optional.swift)

[Control Flow](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/controlflow/#Switch)

[Bool 이름 짓기](https://soojin.ro/blog/naming-boolean-variables)

[Compact Map](https://developer.apple.com/documentation/swift/sequence/compactmap(_:))

[shuffle method Time Complexcity](https://hyerios.tistory.com/18)

[ArraySlice Time Complexcity](https://swiftdoc.org/v5.1/type/arrayslice/)
