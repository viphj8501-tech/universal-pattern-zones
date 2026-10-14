# Universal Pattern Zones — Pine Script v0.2

TradingView Pine Script v6용 기술적 패턴 및 목표 가격 영역 표시 지표의 개발 저장소입니다. 현재 구현은 초기 프로토타입이며, 투자 결과를 보장하지 않습니다.

## 최신 버전: v0.2

파일: [universal_pattern_zones_v0_2.pine](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_2.pine)

### 탐지 패턴
- 이중천장(Double Top)
- 이중바닥(Double Bottom)
- 헤드앤숄더(Head & Shoulders)
- 역헤드앤숄더(Inverse Head & Shoulders)
- FVG(Fair Value Gap): 3개 캔들 구조의 상승·하락 불균형 구간

### 표시 및 상태
- 피벗 기반 패턴 후보와 측정 목표가 영역을 반투명 사각형으로 표시
- 종가 기준 넥라인 돌파/이탈 확인 시 클래식 패턴 상태 변경
- FVG의 활성·부분 해소·완전 해소 상태 구분
- 오래된 영역 삭제를 통해 박스 수 제한
- 후보 감지, 완성 확인, 목표 영역 도달, 패턴 무효화, FVG 감지 및 완전 해소 알림 조건 제공

## 설치 방법
1. TradingView에서 차트를 열고 하단의 Pine Editor를 엽니다.
2. [v0.2 Pine Script 파일](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_2.pine)의 코드를 복사해 붙여넣습니다.
3. Save를 누른 뒤 Add to chart를 선택합니다.
4. 오류가 표시되면 오류 전문과 줄 번호를 기록해 수정합니다.
5. 차트 적용 후 Create Alert에서 필요한 알림 조건을 별도로 설정합니다.

## 설정 튜닝
- `Pivot left bars`, `Pivot right bars`: 패턴에 필요한 스윙 민감도와 확인 지연을 조절합니다.
- `Shoulder/top-bottom tolerance (ATR)`: 어깨 또는 고점·저점 유사성 허용 오차를 조절합니다.
- `Minimum FVG size (ATR)`: 작은 불균형 구간을 필터링합니다.
- `Target zone half-width (ATR)`: 목표 영역의 세로 폭을 조절합니다.
- `Maximum pattern zones`, `Maximum FVG zones`: 각각 표시할 영역의 개수를 제한합니다.

## 중요 한계
- Pine Editor에서 실제 컴파일 또는 실시간 차트 검증은 아직 수행하지 않았습니다. GitHub 등록만으로 컴파일 성공을 의미하지 않습니다.
- 피벗은 오른쪽 확인 봉이 지난 뒤 확정됩니다. 표시 위치가 과거 봉으로 되돌아가 보이더라도, 해당 지점에서 실시간으로 미리 알 수 있었던 신호는 아닙니다.
- 패턴 목표가는 구조에 기반한 추정치입니다. 도달 또는 수익을 보장하지 않습니다.
- FVG는 가격 불균형 구간이며 자동 매수·매도 신호로 해석해서는 안 됩니다.
- 기본 탐지 범위는 일부 대표 패턴에 한정됩니다. 모든 금융시장 패턴이 구현된 완성판은 아닙니다.

## 버전
- [v0.1](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_1.pine): 클래식 4개 패턴의 초기 코어
- [v0.2](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_2.pine): v0.1 기능 + FVG 구간 탐지/해소 상태

## 로드맵
다음 구현·검증 계획은 [패턴 모듈 확장 로드맵](docs/PATTERN_MODULE_ROADMAP.md)을 참조하세요.
