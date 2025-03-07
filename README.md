# kotlin-racingcar

# 자동차 경주 게임

## 진행 방법
* 자동차 경주 게임 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 코드 리뷰 요청을 한다.
* 코드 리뷰 피드백에 대한 개선 작업을 하고 다시 PUSH한다.
* 모든 피드백을 완료하면 다음 단계를 도전하고 앞의 과정을 반복한다.

## 온라인 코드 리뷰 과정
* [텍스트와 이미지로 살펴보는 온라인 코드 리뷰 과정](https://github.com/next-step/nextstep-docs/tree/master/codereview)

## 목차

1. [자동차 경주 게임][# 자동차 경주]
---

# 자동차 경주

## 기능 요구 사항
초간단 자동차 경주 게임을 구현한다.
- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- 각 자동차에 이름을 부여할 수 있다. 자동차 이름은 5자를 초과할 수 없다.
- 자동차 이름은 쉼표(,)를 기준으로 구분한다.
- 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 사용자는 몇 대의 자동차로 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- 자동차의 상태를 화면에 출력한다. 어느 시점에 출력할 것인지에 대한 제약은 없다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.

## 기능 구현
- [x] 사용자에게 경주할 자동차 이름을 입력받는 기능 구현 - RacingCarInput#getCarName
  - [x] 입력 값이 쉼표를 기준으로 구분되는지 검증 - isCommaSeperated()
  - [x] 시도할 횟수가 입력받는 기능 구현 - getRaceCount()  
- [x] 자동차 이름, 위치정보를 저장하는 자동차 클래스 - RacingCar 
  - [x] 자동차 이름의 길이가 5이하인지 검증 - isCorrectNameSize()
  - [x] 전진 하는 메서드 - moveForward()
- [x] 자동차게임 실행하는 클래스 - GameLauncher
  - [x] 필드로 자동차 리스트 관리
  - [x] 여러 자동차 한번에 전진 - start()
  - [x] 시도마다 결과를 출력 - printRacing()
  - [x] 우승자를 선정해서 출력 - printWinner()
- [x] 랜덤값 생성 클래스 - RandomUtil
  - 랜덤값 생성기능 구현 - createRandomNumber()
