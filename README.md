# 통합 패턴 영역 — Universal Pattern Zones v0.9

TradingView Pine Script v6 기반 차트 분석 지표입니다. 여러 기술적 패턴 후보와 예상 가격 영역을 차트에 사각 박스로 표시합니다. 모든 영역과 신호는 분석 보조 수단이며, 가격 도달·매매 성공·수익을 보장하지 않습니다.

## 최신 버전
- [v0.9 Pine Script — 캔들 패턴 확장: 모닝스타·이브닝스타·해머·슈팅스타·적삼병·흑삼병](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_9.pine)
- [v0.8 Pine Script — 하모닉 패턴: AB=CD·가틀리·배트·버터플라이·크랩](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_8.pine)
- [v0.7 Pine Script — EQH/EQL 유동성 풀·오더 블록 영역 선택](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_7.pine)
- [v0.6 Pine Script — ICT/SMC: BOS·CHOCH·유동성 스윕·오더 블록](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_6.pine)
- [v0.5 Pine Script — 한글 패턴명·추세 지속 패턴·돌파선 재시험](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_5.pine)

## 구현 패턴

### 반전 구조
- 이중천장 / 이중바닥
- 헤드앤숄더 / 역헤드앤숄더

### 가격 불균형
- 상승 불균형(FVG) / 하락 불균형(FVG)
- 부분 해소 / 완전 해소

### 캔들 패턴
- 상승 장악형 / 하락 장악형
- 상승 핀바 / 하락 핀바
- 모닝스타 / 이브닝스타
- 하락 흐름 뒤 해머 / 상승 흐름 뒤 슈팅스타
- 적삼병 / 흑삼병

### 삼각형·쐐기 및 추세 지속
- 상승 삼각형 / 하락 삼각형 / 대칭 삼각형
- 상승 쐐기형 / 하락 쐐기형
- 상승 깃발 / 하락 깃발
- 상승 페넌트 / 하락 페넌트
- 직사각형 박스권 / 상승 채널 / 하락 채널
- 구조 돌파 이후 돌파선 재시험의 대기·성공·실패·만료 상태

### v0.6 ICT/SMC 구조
- **BOS (Break of Structure)**: 최근 확정 스윙 고점·저점을 종가로 돌파할 때 표시
- **CHOCH (Change of Character)**: 추적 중인 구조 방향과 반대 방향의 종가 돌파를 감지
- **유동성 스윕**: 확정 스윙 고점·저점을 꼬리로 넘어섰다가 레벨 안쪽에서 종가가 형성되면 표시
- **오더 블록**: BOS/CHOCH 발생 전 설정한 탐색 범위 내에서 가장 가까운 반대 방향 캔들을 찾고 해당 캔들의 고가~저가를 박스로 표시
- 오더 블록 상태: 활성 → 재방문 → 종가 기준 무효화
- 각 모듈의 한글 박스 라벨 및 개별 알림 조건

### v0.7 ICT/SMC 정교화
- **EQH (Equal Highs)**: 허용 오차 내에 반복해서 형성된 확정 스윙 고점들을 상단 유동성 풀로 표시
- **EQL (Equal Lows)**: 허용 오차 내에 반복해서 형성된 확정 스윙 저점들을 하단 유동성 풀로 표시
- 비슷한 높이의 미체결 유동성 풀은 하나로 병합해 중복 표시를 줄임
- 유동성 풀은 레벨을 꼬리로 넘은 뒤 다시 안쪽에서 종가가 형성되면 스윕 완료 상태로 바뀜
- 오더 블록 영역을 **전체 캔들 고가~저가** 또는 **캔들 몸통(open~close)** 기준으로 선택
- EQH/EQL 생성 및 각 방향의 스윕 알림 추가

### v0.8 하모닉 패턴
- **AB=CD**
- **가틀리(Gartley)**
- **배트(Bat)**
- **버터플라이(Butterfly)**
- **크랩(Crab)**
- 다섯 개의 확정 피벗 X-A-B-C-D에서 피보나치 비율 조합을 검사
- D점 주변을 ATR 기반 잠재 반전 영역(PRZ) 박스로 표시하고 감지 알림 제공
- 비율 허용 오차, AB=CD 길이 오차, PRZ 폭 및 표시 박스 수 설정 제공 

### v0.9 확장 캔들 패턴
- 모닝스타 / 이브닝스타: 3개 캔들 조합과 첫 캔들 몸통 중간값 회복·이탈 조건
- 해머 / 슈팅스타: 긴 꼬리·몸통 위치와 간단한 직전 하락·상승 흐름 조건
- 적삼병 / 흑삼병: 3개 연속 방향성 캔들, 단계적인 종가 진행, 이전 몸통 내부 시가 조건
- 기존 ATR 목표 영역·신호 캔들 고가/저가 무효화 관리 및 박스 수 제한을 공유
- 패턴별 알림과 확장 캔들 패턴 on/off 설정 제공
- 탐지 조건은 차트에서 식별하기 위한 근사 규칙이며, 모든 교과서적 변형을 포괄하지 않음

## 표시 규칙
- 형성 중 패턴: 주황색 계열 구조 박스
- 목표 가격 영역: 패턴 높이 또는 ATR 기반의 반투명 사각 박스
- BOS / CHOCH: 스윙 돌파 레벨 주변에 방향별 박스
- 유동성 스윕: 스윕 캔들의 꼬리 영역을 강조하는 박스
- 오더 블록: 활성은 방향별 색상, 재방문은 주황색, 무효화는 회색
- 무효화·만료된 영역은 회색 계열로 상태 표시

## 설치
1. TradingView 차트를 열고 하단의 Pine Editor를 엽니다.
2. [v0.9 소스 파일](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_9.pine)을 열어 코드를 복사합니다.
3. Pine Editor에 붙여넣고 Save를 누른 뒤 Add to chart를 선택합니다.
4. 알림을 쓰려면 Create Alert에서 필요한 한글 조건을 선택합니다.

## 주요 설정
- **탐지 설정**: 피벗 왼쪽·오른쪽 확인 봉 수, ATR 기간, 고점·저점 허용 오차
- **패턴 설정**: 반전·FVG·캔들·기하학 패턴군의 탐지 켜기/끄기
- **추세 지속 패턴**: 깃발·페넌트·박스권·채널 탐지 및 선행 추세 최소 폭
- **돌파·재시험**: 재시험 허용 폭, 박스 최대 개수
- **ICT/SMC 구조**: BOS·CHOCH·스윕 활성화, EQH/EQL 허용 오차, 오더 블록 전체 캔들/몸통 선택
- **하모닉 패턴**: 패턴 감지 켜기/끄기, 피보나치 비율 허용 오차, AB=CD 길이 오차, D점 PRZ 폭 및 최대 박스 수
- **FVG·캔들 설정**: 최소 FVG 크기, 캔들 몸통·핀바 꼬리 조건, 별형 중간 캔들 몸통 비율, 확장 패턴 탐지 켜기/끄기, ATR 목표 거리
- **표시 설정**: 목표 영역 폭, 오른쪽 투영 길이, 목표 박스 최대 개수

## 중요한 한계 및 검증 상태
- 사용자는 v0.8의 정상 작동을 확인했습니다. v0.9는 새 캔들 패턴을 포함하므로 TradingView Pine Editor에서 실제 컴파일 및 차트 확인이 필요합니다. 이 환경에서는 TradingView의 실제 컴파일러를 실행할 수 없습니다.
- 하모닉 패턴의 피보나치 조건은 허용 오차를 가진 근사 판별이며, D점 PRZ는 실제 D 피벗 주변의 ATR 기반 표시 영역입니다. 이는 미래 반전을 보장하지 않습니다.
- BOS/CHOCH의 추세 방향은 스크립트 내부에서 추적하는 단순 편향 상태를 이용합니다. 다양한 ICT/SMC 정의를 완전히 대표하는 것은 아닙니다.
- 오더 블록은 BOS/CHOCH 직전 탐색 범위 내 최근 반대 방향 캔들의 전체 고가~저가로 근사합니다. 바디만 쓰는 방식, 거래량·상위 시간대 필터, 다중 오더 블록 선택 등 고급 규칙은 아직 포함되지 않았습니다.
- 피벗은 오른쪽 확인 봉이 지난 뒤 확정됩니다. 과거 피벗 위치에 표시돼도 당시 실시간으로 미리 알 수 있었던 신호는 아닙니다.
- 깃발·페넌트·채널은 단순 피벗 기하 규칙으로 추정합니다. 목표 가격은 패턴 높이나 ATR 배수 기반 추정치이며 보장을 뜻하지 않습니다.

## 버전 이력
- [v0.1 — 클래식 반전 패턴 코어](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_1.pine)
- [v0.2 — FVG 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_2.pine)
- [v0.3 — 캔들 패턴 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_3.pine)
- [v0.4 — 삼각형·쐐기 모듈](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_4.pine)
- [v0.5 — 한글화·추세 지속·돌파선 재시험](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_5.pine)
- [v0.6 — ICT/SMC: BOS·CHOCH·유동성 스윕·오더 블록](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_6.pine)
- [v0.7 — EQH/EQL 유동성 풀 및 오더 블록 영역 선택](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_7.pine)
- [v0.8 — 하모닉 패턴 AB=CD·가틀리·배트·버터플라이·크랩](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_8.pine)
- [v0.9 — 캔들 패턴 확장: 모닝스타·이브닝스타·해머·슈팅스타·적삼병·흑삼병](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v0_9.pine)

개발 계획은 [패턴 모듈 확장 로드맵](docs/PATTERN_MODULE_ROADMAP.md)을 참조하세요.
