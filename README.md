# java-racingcar-precourse

## 📋 기능 구현 목록 

### ✅ 진행 과정

#### 1. 경주할 자동차 이름을 `,` (쉼표) 기준으로 구분하여 입력한다

- 자동차 이름은 5자 이하만 가능하다
- 자동차 이름은 중복되면 안된다
```text
pobi,woni,jun
```

#### 2. 시도할 횟수를 입력한다

- 횟수는 양의 정수만 가능하다
- 횟수는 2,147,483,647(Integer.MAX_VALUE)로 제한한다

```text
5
```

#### 3. 자동차 별로 횟수 만큼 전진을 수행한다

- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4이상일 경우이다

#### 4. 차수별 실행 결과를 출력한다

- 전진 결과는 자동차 이름과 함께 `-` (하이픈)으로 표현된다

```text
pobi : --
woni : ----
jun : ---
```

#### 5. 최종 우승자를 출력한다

- 단독 우승자 안내 문구

```text
최종 우승자 : pobi
```

- 공동 우승자 안내 문구

```text
최종 우승자 : pobi, jun
```

### ✅ 실행 결과 예시
```text
경주할 자동차 이름을 입력하세요.(이름은 쉼표(,) 기준으로 구분)
pobi,woni,jun
시도할 횟수는 몇 회인가요?
5

실행 결과
pobi : -
woni : 
jun : -

pobi : --
woni : -
jun : --

pobi : ---
woni : --
jun : ---

pobi : ----
woni : ---
jun : ----

pobi : -----
woni : ----
jun : -----

최종 우승자 : pobi, jun
```

### ✅ 클래스 및 기능

#### 1. domain

##### Car

- [X] 자동차의 이름과 위치 정보를 갖고 있는다
- [X] 무작위 숫자에 따라 자동차의 전진을 결정한다
- [X] 해당 자동차가 우승인지 판단한다

###### 예외처리
- [X] 자동차의 이름이 5글자 초과인 경우
- [X] 자동차의 이름이 빈문자열인 경우

##### Count

- [X] 자동의 횟수 정보를 갖고 있는다

###### 예외처리
- [X] 횟수가 양의 정수가 아닌 경우
- [X] 횟수가 2,147,483,647(Integer.MAX_VALUE)를 초과할 경우

##### Racing

- [X] 자동차들을 생성한다
- [X] 자동차 경주를 시행한다
- [X] 최종 우승자를 결정한다

###### 예외처리

- [X] 중복된 자동차 이름이 존재할 경우

#### 2. util

##### RacingCarValidator

- [X] 자동차 이름 길이 검증
- [X] 자동차 이름 중복 여부 검증
- [X] 시도 횟수 범위 검증

##### InputValidator

- [X] 입력된 자동차 이름 형식 검증
- [X] 입력된 시도 횟수 형식 검증


##### RandomNumberGenerator

- [X] 0 ~ 9 사이 무작위 값을 생성한다
- [X] NumberGenerator의 구현체

#### 3. controller

- [X] 사용자에게 자동차 이름을 요청한다
- [X] 사용자에게 시도 횟수를 요청한다
- [X] 사용자에게 실행 결과를 반환한다
- [X] 사용자에게 최종 우승자를 반환한다

#### 4. view

##### InputView

- [X] 입력값을 읽는다

##### OutputView

- [X] 요청 메세지를 출력한다
- [X] 실행 결과를 출력한다
- [X] 최종 우승자를 출력한다

#### 5. constant

##### Rule

- [X] 자동차 경주의 룰을 상수로 정의한다

#### ErrorType

- [X] 에러 타입을 정의 한다