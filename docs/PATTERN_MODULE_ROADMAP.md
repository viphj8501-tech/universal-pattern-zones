# Universal Pattern Zones — 모듈 확장 및 검증 계획

## 현재 구현 상태

### v0.1 — 초기 코어
- Double Top / Double Bottom
- Head & Shoulders / Inverse Head & Shoulders
- 후보 / 완성 확인 / 목표 도달 / 무효화 상태 박스
- 주요 상태에 대한 alertcondition

### v0.2 — FVG 모듈 추가
- 3개 캔들 구조로 bullish / bearish FVG 탐지
- 최소 FVG 크기(ATR 배수) 필터
- 활성 / 부분 해소 / 완전 해소 상태
- FVG 감지 및 완전 해소 알림
- FVG 박스 수 별도 제한

## 다음 모듈 후보
1. 가격 구조: 삼각형, 쐐기, 깃발, 페넌트, 직사각형, 채널, 브레이크아웃/리테스트
2. ICT/SMC: Order Block, BOS/CHOCH, Liquidity Sweep, Equal Highs/Lows
3. 캔들: Engulfing, Pin Bar, Hammer/Shooting Star, Morning/Evening Star 등
4. 하모닉: AB=CD, Gartley, Bat, Butterfly, Crab, Cypher, Shark
5. 파동: Elliott wave 후보(해석 규칙과 주관성을 별도로 명시)
6. 품질 필터: 거래량, ATR, 상위 타임프레임 방향, 세션/유동성 조건
7. 검증/분석: 신호 지연, 패턴별 오탐 기록, 전략테스터용 별도 구현

## 코어 원칙
- 패턴 탐지, 목표 구간 산출, 박스 표시·상태 관리를 분리한다.
- 후보와 종가 기준 확정 상태를 구분한다.
- 피벗 확인 지연 및 리페인팅 위험을 문서화한다.
- 패턴별 탐지 규칙, 무효화 조건, 목표가 공식을 명시한다.
- 표시 객체 수를 제한하고 오래된 구간을 정리한다.
- FVG를 포함한 패턴 영역은 자동 매매 권고가 아니라 시각적 분석 도구로 설명한다.

## 릴리스 검증 게이트
1. TradingView Pine Editor에서 컴파일 성공 확인
2. 대상 심볼·시간봉에 적용해 탐지 영역이 올바르게 놓이는지 확인
3. 후보·확정·부분 해소·완전 해소·무효화 상태 전이 확인
4. 실시간 봉과 과거 차트에서 신호 확정 시점 및 리페인팅 여부 점검
5. 박스 개수 한도와 실행 성능 확인
6. 측정 목표가가 성과를 보장하지 않는다는 점을 명확히 표시
