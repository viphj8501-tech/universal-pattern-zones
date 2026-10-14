# 통합 패턴 영역 — Universal Pattern Zones v0.5

TradingView Pine Script v6 지표입니다. 여러 기술적 패턴 후보와 예상 가격 영역을 차트에 사각 박스로 표시합니다. 모든 영역은 분석 보조 수단이며 가격 도달 또는 수익을 보장하지 않습니다.

## 최신 버전
- [v0.5 Pine Script — 한글 패턴명 + 추세 지속 패턴 + 돌파선 재시험](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_5.pine)

## 구현 패턴

### 반전 구조
- 이중천장
- 이중바닥
- 헤드앤숄더
- 역헤드앤숄더

### 가격 불균형
- 상승 불균형(FVG)
- 하락 불균형(FVG)
- 부분 해소 / 완전 해소

### 캔들 패턴
- 상승 장악형 / 하락 장악형
- 상승 핀바 / 하락 핀바

### 삼각형 및 쐐기
- 상승 삼각형
- 하락 삼각형
- 대칭 삼각형
- 상승 쐐기형
- 하락 쐐기형

### v0.5 추세 지속·가격 구조
- 상승 깃발 / 하락 깃발
- 상승 페넌트 / 하락 페넌트
- 직사각형 박스권
- 상승 채널 / 하락 채널
- 삼각형·쐐기·깃발·페넌트·채널 등 감지 구조의 종가 기준 돌파
- 돌파 경계 주변의 재시험 대기 박스, 재시험 성공·실패·대기 만료 표시

## 표시 규칙
- 형성 중 패턴: 주황색 계열 구조 박스
- 목표 가격 영역: 패턴 높이 또는 ATR 기반으로 산출한 반투명 사각 박스
- 돌파선 재시험 대기: 노란색 박스
- 재시험 성공: 청록색 계열
- 무효화·만료: 회색 계열

## 설치
1. TradingView 차트를 열고 하단의 Pine Editor를 엽니다.
2. [v0.5 소스 파일](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_5.pine)을 열어 코드를 복사합니다.
3. Pine Editor에 붙여넣고 Save를 누른 뒤 Add to chart를 선택합니다.
4. 알림을 쓰려면 Create Alert에서 원하는 한글 알림 조건을 선택합니다.

## 주요 설정
- **패턴 설정**: 각 패턴군 탐지 켜기/끄기
- **탐지 설정**: 피벗 왼쪽·오른쪽 확인 봉 수, ATR 기간, 고점·저점 허용 오차
- **삼각형·쐐기**: 최소 스윙 폭, 수평 경계 허용 오차, 형성 박스 최대 개수
- **추세 지속 패턴**: 깃발·페넌트·박스권·채널 탐지, 선행 추세 최소 폭
- **돌파·재시험**: 재시험 박스 최대 개수, 돌파선 재시험 허용 폭
- **FVG·캔들 설정**: 최소 FVG 크기, 캔들 몸통 및 핀바 꼬리 조건, ATR 목표 거리
- **표시 설정**: 목표 영역 폭, 박스 오른쪽 투영 길이, 각 박스 최대 개수

## 중요한 한계
- v0.5는 TradingView Pine Editor에서 실제 컴파일을 자동으로 검증한 상태가 아닙니다. 사용자가 Pine Editor에서 컴파일과 차트 동작을 확인해야 합니다.
- 피벗 기반 패턴은 오른쪽 확인 봉이 지난 뒤 확정됩니다. 과거 봉 위치에 표시되어도 해당 시점에 실시간으로 미리 알 수 있었던 신호가 아닙니다.
- 가격 구조는 5개의 교대 피벗과 단순 기울기 외삽을 이용합니다. 깃발·페넌트·채널의 판별은 근사 규칙이며, 모든 시장 상황을 완벽하게 분류하지는 않습니다.
- 목표 가격은 패턴 높이 또는 ATR 배수를 이용한 기술적 추정치입니다. 목표 도달, 매매 성공 또는 수익을 보장하지 않습니다.
- 돌파선 재시험은 돌파 이후 정해진 대기 기간 안에 가격이 구간을 다시 터치하고 돌파 방향으로 종가가 회복되는 경우 성공으로 표시합니다. 이는 자동 매매 지시가 아닙니다.

## 버전 이력
- [v0.1 — 클래식 패턴 코어](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_1.pine)
- [v0.2 — FVG 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_2.pine)
- [v0.3 — 캔들 패턴 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_3.pine)
- [v0.4 — 삼각형·쐐기 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_4.pine)

개발 계획은 [패턴 모듈 확장 로드맵](docs/PATTERN_MODULE_ROADMAP.md)을 참조하세요.
