# Universal Pattern Zones — 모듈 확장 및 검증 계획

## 현재 구현 상태

### v0.1 — 클래식 패턴 코어
- Double Top / Double Bottom
- Head & Shoulders / Inverse Head & Shoulders
- 후보 / 완성 확인 / 목표 도달 / 무효화 상태 박스와 알림

### v0.2 — FVG 모듈
- 3개 캔들 구조의 bullish / bearish FVG
- 최소 FVG 크기(ATR 배수) 필터
- 활성 / 부분 해소 / 완전 해소 상태와 알림

### v0.3 — 캔들 패턴 모듈
- Bullish / Bearish Engulfing
- Bullish / Bearish Pin Bar
- 종가가 확정된 신호 캔들로 패턴 탐지
- ATR 배수 기반 예상 목표 영역
- 신호 캔들 고가/저가 기준 무효화, 목표 도달 및 무효화 알림

## 다음 모듈 후보
1. 가격 구조: 삼각형, 쐐기, 깃발, 페넌트, 직사각형, 채널, 브레이크아웃/리테스트
2. ICT/SMC: Order Block, BOS/CHOCH, Liquidity Sweep, Equal Highs/Lows
3. 하모닉: AB=CD, Gartley, Bat, Butterfly, Crab, Cypher, Shark
4. 파동: 해석 규칙을 명시한 Elliott wave 후보
5. 품질 필터: 거래량, ATR, 상위 타임프레임 방향, 세션 조건
6. 검증: 신호 지연, 오탐 분석, 실시간 리페인팅 점검, 전략테스터용 별도 구현

## 코어 원칙
- 탐지, 목표 구간 산출, 박스 표시/상태 관리를 분리한다.
- 후보 상태와 종가 기준 확인 상태를 구분한다.
- 피벗 확인 지연 및 리페인팅 위험을 문서화한다.
- 패턴별 탐지 규칙, 무효화 조건, 목표가 공식을 명시한다.
- FVG와 캔들 패턴 목표는 자동 매매 권고가 아니라 시각적 분석 도구로 설명한다.

## 릴리스 검증 게이트
1. TradingView Pine Editor에서 컴파일 성공 확인
2. 패턴 예제 차트에서 탐지/무효화/목표 영역 검증
3. 후보·확정·부분 해소·완전 해소 상태 전이 확인
4. 과거 차트와 실시간 봉에서 신호 시점과 리페인팅 여부 확인
5. 박스 개수 한도 및 성능 점검
6. 목표가는 추정치이며 성과를 보장하지 않음을 명시
