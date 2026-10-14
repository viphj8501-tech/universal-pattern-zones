# Universal Pattern Zones — 모듈 확장 및 검증 계획

## 현재 구현 상태

### v0.1 — 클래식 패턴 코어
- Double Top / Double Bottom
- Head & Shoulders / Inverse Head & Shoulders
- 후보 / 완성 확인 / 목표 도달 / 무효화 상태 박스와 알림

### v0.2 — FVG 모듈
- 3개 캔들 구조의 bullish / bearish Fair Value Gap
- 최소 FVG 크기(ATR) 필터
- 활성 / 부분 해소 / 완전 해소 상태와 알림

### v0.3 — 캔들 패턴
- Bullish / Bearish Engulfing
- Bullish / Bearish Pin Bar
- 신호 캔들 종가 확인 후 ATR 기반 목표 영역
- 신호 캔들 극값 기준 무효화 및 목표 도달 알림

### v0.4 — 삼각형·쐐기 가격 구조
- Ascending Triangle / Descending Triangle
- Symmetrical Triangle
- Rising Wedge / Falling Wedge
- 5개의 교대 확정 피벗으로 형성 구조 후보 탐지
- 최근 고점/저점의 기울기를 외삽해 상단·하단 돌파 수준 추정
- 종가 돌파가 확인되면 실제 돌파 방향으로 패턴 높이 측정 이동 목표 박스 생성
- 수렴 종료 감지와 형성·돌파·수렴 종료 알림 조건

## 다음 모듈 후보
1. 가격 구조: Flag, Pennant, Rectangle, Channel, Breakout/Retest
2. ICT/SMC: Order Block, BOS/CHOCH, Liquidity Sweep, Equal Highs/Lows
3. 캔들: Morning/Evening Star, Hammer/Shooting Star, Three Soldiers/Crows
4. 하모닉: AB=CD, Gartley, Bat, Butterfly, Crab, Cypher, Shark
5. 파동: 규칙을 명시한 Elliott wave 후보
6. 필터: 거래량, ATR, 상위 타임프레임 추세, 세션 조건
7. 검증: 패턴별 오탐 분석, 신호 지연, 실시간 리페인팅 점검, 전략테스터용 별도 스크립트

## 코어 원칙
- 패턴 탐지, 목표 구간 산출, 박스 상태 관리를 분리한다.
- 후보와 확정 상태를 구분한다.
- 피벗 확인 지연과 실시간/과거 차트 차이를 문서화한다.
- 각 패턴의 탐지·무효화 조건 및 목표가 공식을 명시한다.
- 박스 개수와 기울기 외삽의 한계를 관리한다.
- 목표가 표시는 예측 보증이나 수익 보장이 아님을 명시한다.

## 릴리스 검증 게이트
1. TradingView Pine Editor에서 실제 컴파일
2. 최소 2~3개 심볼과 여러 시간대에서 차트 모양 검증
3. 후보 → 돌파 → 목표 도달 또는 수렴 종료의 상태 전이 점검
4. 실제 봉 마감과 과거 시그널 표시 차이 확인
5. 박스 한도와 실행 성능 확인
6. 컴파일 오류·경고를 수정하고 다음 버전으로 커밋
