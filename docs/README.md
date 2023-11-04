# 🎰 로또 게임

## 📌 프로젝트 소개
- 프로젝트 동기: (작성중) 
- 로또 게임 설명: (작성중)
- 프로젝트 특징: (작성중)

---
## 🛠️ 기능 목록

### 입력 기능
- [x] 로또 구입 금액 입력 기능
  - [x] 구입 금액을 1,000원 단위로 입력
  - [x] 예외 처리: 구입 금액이 숫자로 입력되지 않은 경우
  - [x] 예외 처리: 구입 금액이 1,000원으로 나누어 떨어지지 않는 경우
  - [x] 예외 처리: 구입 금액이 '-3,000'과 같은 음수이거나 0인 경우
- [ ] 당첨 번호 입력 기능
  - [ ] 각 번호는 쉼표(,)를 기준으로 구분해서 총 6개의 번호를 입력
  - [ ] 예외 처리: 각 번호가 1 이상 45 이하의 정수가 아닌 경우
  - [ ] 예외 처리: 당첨 번호의 개수가 6개가 아닌 경우
- [ ] 보너스 번호 입력 기능
  - [ ] 한 개의 보너스 번호를 입력
  - [ ] 예외 처리: 각 번호가 1 이상 45 이하의 정수가 아닌 경우
  - [ ] 예외 처리: 당첨 번호의 개수가 1개가 아닌 경우

### 발행 및 계산 기능 (도메인 로직)
- [x] 로또 발행 기능
  - [x] 사용자가 구매한 로또 수량만큼 로또 발행
  - [x] 각 로또를 발행할 때는 중복되지 않는 6개의 숫자를 랜덤으로 뽑기
- [ ] 당첨 계산 기능
  - [ ] 각 발행한 로또마다 당첨 번호와 일치하는 개수 계산
  - [ ] 5개가 일치한 로또의 경우, 보너스 번호가 일치하는지 확인
  - [ ] 등수를 기준으로 당첨된 내역 합산
- [ ] 수익률 계산 기능(도메인 로직으로 볼 수 있나?)
  - [ ] 총 당첨된 금액 계산
  - [ ] 로또 구입 금액 대비 총 당첨 금액에 대한 수익률 계산

### 출력 기능
- [ ] 발행 내역 출력 기능
  - [ ] "x개를 구매했습니다."와 같이 발행한 로또 수량 출력
  - [ ] 발행한 로또 번호를 오름차순으로 정렬하여 출력
- [ ] 당첨 내역 출력 기능
  - [ ] 1등부터 5등까지 각 등수마다 당첨된 로또 개수를 출력
- [ ] 수익률 출력 기능
  - [ ] 수익률은 소수점 둘째 자리에서 반올림하여 출력
- [ ] 에러 문구 출력 기능
  - [ ] 예외 상황의 경우, "[ERROR]"로 시작하는 에러 문구를 출력

---

## 🖥️ 실행 결과 예시
```
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[8, 21, 23, 41, 42, 43] 
[3, 5, 11, 16, 32, 38] 
[7, 11, 16, 35, 36, 44] 
[1, 8, 11, 31, 41, 42] 
[13, 14, 16, 38, 42, 45] 
[7, 11, 30, 40, 42, 43] 
[2, 13, 22, 32, 38, 45] 
[1, 3, 5, 14, 22, 45]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```