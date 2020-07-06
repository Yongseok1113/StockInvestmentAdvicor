
# StockInvestmentAdvicor
 - 고객이 소유한 주식에 대해 해당 회사와 관련된 뉴스기사를 분석하여 긍정적인지 부정적인지에 따라 주가 등락 예측 후 매수/매도를 추천하는 프로그램 개발

# 서비스 시나리오
1. 앱 접속 중 주식 매수 추천 서비스
    - 일정 기간 내 긍정 수치가 높은 기사가 노출되어 주가상승이 예상되는 주식 매수 추천
  
2. 앱 접속 중 소유주식 매도 추천 서비스
    - 현재 고객이 주식을 소유한 회사들 중 최근 부정 수치 높은 기사가 노출되어 주가 하락이 예상되는 주식 매도 추천 

3. 앱 비접속 중 주가 하락 경고 알림 서비스
    - 고객이 소유한 주식들 중 최근 노출된 기사가 부정 수치가 높아 일정 수준 주가하락이 예상되는 경우 푸시알림

# 서비스 타당성 검증
  - 긍정/부정적인 기사 노출이 정말로 주가에 영향을 미칠까? (유의미한 영향을 줄 수 있을까?)
  - 기사와 주가가 상관관계가 있다면, 기사 긍정/부정 정도에 따른 주식 등락폭이 예측 가능할까?
  - 기사에서 핵심 사실만 추출하는 것이 가능할까? -> 가능하다 (글 주제 추출 / 글 세줄 요약 프로젝트를 본적있다)
  - 기사에서 추출한 핵심 사실이 정말로 사실일까? (허위사실 포함한 경우 / 일부 사실 누락된 경우)
  
# 핵심 구현 기능
  - 단순히 주식 등락 예측이 아닌 어느 정도 수준까지 오르거나 내리는지 예측할 수 있어야 한다
  - 분류한 긍정/부정 수치가 신뢰도가 높아야 한다 (허위사실/일부사실누락)

# 사전 조사
  - 뉴스 기사와 주식을 연관시킨 다른 프로젝트 검색
  - 주식 앱 (오늘의 추천종목) -> 어떤 알고리즘으로 추천하는지?


# 생각
  - 주식이 오르고 내리는 원리는 무엇일까?
  - 허위사실을 어떻게 회피할까?
  - 사실 누락 여부를 어떻게 판단할까? 
  - 과거 동일 날짜(+-3일?) 기사 노출에 따른 주가그래프 변동을 데이터화 하여 훈련데이터로 쓰려하는데 이건 타당할까?
    (기사 뿐만아니라 다른 여러가지 요인이 복합적으로 작용해서 주가를 형성할 것이다)

# 구현 
  - 작업
  1. 데이터 크롤링
  2. 데이터 전처리
  3. 자연어 처리(핵심 사실 도출)
  4. 긍정 부정 예측(긍/부정 정도 수치화)
  5. 추천/비추천 분류

 
