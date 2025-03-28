# tdd-project

### Features
  - 5 USD x 2 = 10 USD
  - 10 EUR x 2 = 20 EUR
  - 4002 KRW / 4 = 1000.5 KRW
  - 모듈화; 프로덕션 코드에서 테스트 코드 분리
  - 중복 테스트 제거
  - 5 USD + 10 EUR = 17 USD
  - 1 USD + 1100 KRW = 2200 KRW
  - 연관된 통화에 기반한 환율 결정 (환전 전 -> 환전 후)
  - 환율이 명시되지 않은 경우 오류 처리 개선
    1. 하나 이상 필요한 환율이 누락되었을 때 evaluate() 메서드는 명시적 오류를 표시해야 함
    2. 오류 메시지는 greedy 해야함. 즉, 첫 번째 누락 환율만이 아닌 Portfolio의 평가를 방해하는 모든 누락 환율을 표시해야 함
    3. 호출자가 오류를 무시하지 않도록 누락 환율로 인해 오류가 발생할 때 유효한 Money가 반환되어서는 안됨
  - 환율 수정 허용