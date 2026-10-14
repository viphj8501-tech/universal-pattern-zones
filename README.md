# Universal Pattern Zones — Pine Script v0.4

TradingView Pine Script v6용 기술적 패턴 및 예상 가격 영역 표시 지표의 개발 저장소입니다. 현재 구현은 사용자가 차트에서 확인하며 테스트하는 프로토타입이며, 투자 결과를 보장하지 않습니다.

## 최신 버전: v0.4

- [v0.4 Pine Script — Triangle & Wedge 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_4.pine)

### 구현 패턴
- 클래식 구조: Double Top, Double Bottom, Head & Shoulders, Inverse Head & Shoulders
- FVG: Bullish/Bearish Fair Value Gap, 부분·완전 해소
- 캔들: Bullish/Bearish Engulfing, Bullish/Bearish Pin Bar
- 가격 구조 v0.4: Ascending Triangle, Descending Triangle, Symmetrical Triangle, Rising Wedge, Falling Wedge

### v0.4 가격 구조 모듈
- 5개의 교대 확정 피벗을 사용해 스윙 구조 후보를 판별합니다.
- 형성 중 패턴은 오렌지색 사각형으로 표시합니다.
- 상단·하단 경계선을 피벗 간 기울기로 연장해 종가 기준 돌파를 확인합니다.
- 돌파 방향은 실제 종가가 상단 경계 위인지 하단 경계 아래인지로 결정합니다. 패턴 이름만으로 매수·매도 방향을 확정하지 않습니다.
- 목표 영역은 돌파 경계에서 패턴의 초기 높이만큼 투영한 측정 이동 영역입니다.
- 삼각형/쐐기 형성, 돌파, 수렴 종료에 알림 조건을 제공합니다.

### 기존 모듈
- 이중천장·이중바닥, 헤드앤숄더·역헤드앤숄더: 측정 목표 영역 및 넥라인 확인
- FVG: 활성·부분 해소·완전 해소 상태
- 캔들: ATR 배수 기반 목표 영역, 신호 캔들 고가/저가 무효화

## 설치 방법
1. TradingView에서 차트를 열고 하단의 Pine Editor를 엽니다.
2. [v0.4 Pine Script](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_4.pine)의 코드를 복사해 붙여넣습니다.
3. Save 후 Add to chart를 선택합니다.
4. 컴파일 오류가 나면 메시지 전체와 줄 번호를 기록해 수정합니다.
5. 차트 적용 후 Create Alert에서 원하는 알림 조건을 별도로 설정합니다.

## 삼각형·쐐기 설정
- `Minimum swing move for shape (ATR)`: 경계가 충분히 움직여야 패턴 후보로 분류하도록 합니다.
- `Horizontal boundary tolerance (ATR)`: 삼각형의 수평 경계 판단 허용 오차입니다.
- `Maximum formation boxes`: 표시할 형성 중 구조 박스 개수입니다.
- `Target zone projection (bars)`: 목표 박스의 미래 표시 길이입니다.
- `Target zone half-width (ATR)`: 목표 가격대 박스의 세로 폭입니다.

## 중요 한계
- 실제 TradingView Pine Editor에서 v0.4의 컴파일 성공 및 차트별 탐지 정밀도는 아직 별도로 확인해야 합니다. 코드 등록과 정적 검토가 실행 검증을 의미하지는 않습니다.
- 피벗 기반 탐지는 오른쪽 확인 봉이 지난 후 확정됩니다. 차트에서 피벗이 과거 위치에 보이는 것은 그 시점에 알 수 있었던 실시간 신호라는 뜻이 아닙니다.
- 추세선 경계는 최근 확정 피벗에서 직선으로 외삽하는 단순 모델입니다. 장기간 외삽하면 경계가 부정확해질 수 있습니다.
- 측정 이동 목표가는 패턴 높이에 기반한 기술적 추정치이며 실제 목표 도달이나 수익을 보장하지 않습니다.
- FVG는 가격 불균형, 캔들 패턴은 시각적 구조로 표시되며 자동 매수·매도 지시가 아닙니다.
- 모든 금융시장 패턴을 구현한 것은 아닙니다.

## 버전
- [v0.1 — 클래식 패턴 코어](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_1.pine)
- [v0.2 — FVG 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_2.pine)
- [v0.3 — 캔들 패턴 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_3.pine)

개발 계획은 [패턴 모듈 확장 로드맵](docs/PATTERN_MODULE_ROADMAP.md)을 참조하세요.
