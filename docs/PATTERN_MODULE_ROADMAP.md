# Universal Pattern Zones — 모듈 확장 계획

## 코어 원칙
- 패턴 탐지 로직, 목표 구간 산출, 박스/상태 표현을 분리한다.
- 후보 상태와 종가 기준 확정 상태를 구분한다.
- 피벗 확인 지연과 리페인팅을 문서화한다.
- 패턴마다 탐지 조건, 무효화 조건, 목표가 산식을 명시한다.
- 차트 객체 수를 제한하고 중복 패턴을 정리한다.

## v0.1 포함
- Double Top / Double Bottom
- Head & Shoulders / Inverse Head & Shoulders
- 후보 / 확정 / 목표 도달 / 무효화 상태의 사각 박스
- Alert conditions

## 후속 모듈 후보
1. 가격 구조: 삼각형, 쐐기, 깃발, 페넌트, 직사각형, 채널, 브레이크아웃/리테스트
2. ICT/SMC: FVG, Order Block, BOS/CHOCH, Liquidity Sweep, Equal Highs/Lows
3. 캔들: Engulfing, Pin Bar, Hammer/Shooting Star, Morning/Evening Star 등
4. 하모닉: AB=CD, Gartley, Bat, Butterfly, Crab, Cypher, Shark
5. 파동: Elliott wave 후보(해석 규칙과 주관성을 별도로 명시)
6. 품질 필터: 거래량, ATR, 상위 타임프레임 방향, 세션/유동성 조건
7. 검증: 심볼/타임프레임별 오탐 분석, 신호 확정 지연, 리페인팅 점검, 전략테스터용 버전

## 릴리스 게이트
- TradingView Pine Editor에서 컴파일 성공 확인
- 과거 구간과 실시간 봉에서 신호가 어떻게 바뀌는지 확인
- 대상 패턴 예제 차트에서 탐지/무효화/목표 영역 검증
- 성능 및 박스 개수 제한 검증
- 투자 성과를 보장하는 표현 금지; 목표가는 패턴 규칙에 따른 추정값으로 표시
