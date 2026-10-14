# Universal Pattern Zones — Pine Script v0.3

TradingView Pine Script v6용 기술적 패턴 및 예상 가격 영역 표시 지표의 개발 저장소입니다. 현재 구현은 초기 프로토타입이며 투자 결과를 보장하지 않습니다.

## 최신 버전: v0.3

- [v0.3 Pine Script](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_3.pine)

### 탐지 패턴
- 이중천장(Double Top)
- 이중바닥(Double Bottom)
- 헤드앤숄더(Head & Shoulders)
- 역헤드앤숄더(Inverse Head & Shoulders)
- FVG(Fair Value Gap): 3개 캔들 구조의 상승·하락 불균형 구간
- 캔들 패턴: Bullish/Bearish Engulfing, Bullish/Bearish Pin Bar

### 표시 및 상태
- 피벗 기반 클래식 패턴 후보와 측정 목표 영역
- 종가 기준 넥라인 돌파/이탈 시 클래식 패턴 확인
- FVG의 활성·부분 해소·완전 해소 상태
- 캔들 패턴 신호 후 ATR 배수로 산출한 목표 영역
- 캔들 패턴 목표 도달 및 신호 캔들 고가·저가 기준 무효화 표시
- 박스 수를 제한하고 오래된 객체 정리
- 패턴 후보, 확인, 목표 도달, 무효화, FVG, 캔들 신호에 대한 알림 조건

## 설치 방법
1. TradingView에서 차트를 열고 하단의 Pine Editor를 엽니다.
2. [v0.3 Pine Script](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_3.pine)의 코드를 복사해 붙여넣습니다.
3. Save를 누른 뒤 Add to chart를 선택합니다.
4. 오류가 표시되면 오류 전문과 줄 번호를 기록해 수정합니다.
5. 차트 적용 후 Create Alert에서 필요한 알림 조건을 별도로 설정합니다.

## 핵심 설정
- `Pivot left bars`, `Pivot right bars`: 피벗 민감도와 확인 지연
- `Shoulder/top-bottom tolerance (ATR)`: 어깨/고점·저점 유사성 허용 오차
- `Minimum FVG size (ATR)`: 작은 불균형 구간 필터
- `Minimum candle body (ATR)`: 작은 캔들 몸통 필터
- `Pin-bar wick/body ratio`: 핀바 꼬리 비율 조건
- `Candle target distance (ATR)`: 캔들 신호 목표 영역 거리
- `Target zone half-width (ATR)`: 목표 영역의 세로 폭

## 중요 한계
- TradingView Pine Editor에서 실제 컴파일 또는 실시간 차트 검증은 아직 수행하지 않았습니다. GitHub 등록 및 정적 검토만으로 컴파일 성공을 의미하지 않습니다.
- 피벗은 오른쪽 확인 봉이 지난 뒤 확정됩니다. 과거 봉에 표시된 피벗은 실시간 사전 신호가 아닙니다.
- 캔들 패턴의 목표는 사용자가 정한 ATR 배수 기반 투영입니다. 검증된 예측력이 입증된 목표가가 아닙니다.
- FVG는 불균형 구간이며 자동 매수·매도 신호가 아닙니다.
- 현재는 대표 패턴만 구현된 초기 버전으로, 금융시장의 모든 패턴을 포함하지 않습니다.

## 이전 버전
- [v0.1 — 클래식 패턴 코어](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_1.pine)
- [v0.2 — 클래식 패턴 + FVG](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_2.pine)

개발 계획과 검증 기준은 [패턴 모듈 확장 로드맵](docs/PATTERN_MODULE_ROADMAP.md)을 참조하세요.
