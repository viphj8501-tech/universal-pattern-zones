# 통합 패턴 영역 — Universal Pattern Zones v1.9

TradingView Pine Script v6 기반 차트 분석 지표입니다. 여러 기술적 패턴 후보와 예상 가격 영역을 차트에 사각 박스로 표시합니다. 모든 영역과 신호는 분석 보조 수단이며, 가격 도달·매매 성공·수익을 보장하지 않습니다.

## 최신 버전
- [v1.9 Pine Script — 진단·검증 패널](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_9.pine)
- [v1.8 Pine Script — 하모닉+SMC+반전 캔들 3중 합류](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_8.pine)
- [v1.7 Pine Script — 쐐기 돌파 필터 및 가격 갭+FVG 복합 합류](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_7.pine)
- [v1.6 Pine Script — 일반 가격 갭 및 미충전·부분 해소·완전 해소 상태 추적](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_6.pine)
- [v1.5 Pine Script — 거래량·ATR·HTF 추세·세션 품질 필터](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_5.pine)
- [v1.4 Pine Script — 내부·외부 유동성 및 상위 시간대 컨플루언스](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_4.pine)
- [v1.3 Pine Script — 라운딩 바텀·탑, 컵앤핸들, 확장형·다이아몬드 패턴](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_3.pine)
- [v1.2 Pine Script — 도지·하라미·관통형·먹구름형·집게형·인사이드/아웃사이드 바·장대캔들](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_2.pine)
- [v1.1 Pine Script — 사이퍼·샤크 하모닉 및 AB=CD 변형, 알림 코드 제거](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_1.pine)
- [v1.0 Pine Script — 오더 블록+FVG 겹침 컨플루언스 및 EQH/EQL 인접 태그](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_0.pine)
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
- 도지
- 상승·하락 하라미
- 관통형 / 먹구름형
- 집게형 저점 / 집게형 고점
- 상승·하락 인사이드 바 / 아웃사이드 바
- 장대양봉 / 장대음봉
- 라운딩 바텀 / 라운딩 탑
- 컵앤핸들
- 확장형 천장 / 확장형 바닥
- 다이아몬드 천장 / 다이아몬드 바닥

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

### v1.0 오더 블록·FVG 컨플루언스
- 같은 방향의 활성 오더 블록과 미완전 해소 FVG가 실제 가격 범위에서 겹칠 때 별도 컨플루언스 영역 생성
- 컨플루언스는 소스 오더 블록과 FVG의 생성 봉 키로 중복 박스 생성을 억제
- 기초 오더 블록이 무효화·제거되거나 FVG가 완전 해소되면 컨플루언스 영역을 종료 표시
- 겹치는 영역이 활성 EQL(상승형) 또는 EQH(하락형) 가격대에 가까우면 라벨에 인접 정보를 추가
- 컨플루언스 탐지 on/off, EQH/EQL 근접 허용 ATR 폭, 최대 박스 수 설정과 개별 알림 제공
- 단순한 가격 겹침 기반 보조 표시이며 독립적인 매수·매도 추천이나 성공 확률 계산은 아님
### v1.1 하모닉 패턴 확장 및 알림 코드 제거
- 사이퍼(Cypher): AB/XA, BC/XA, CD/XC 비율과 C점 바깥 확장 및 D점 형상을 함께 검사
- 샤크(Shark): B점 XA 바깥 확장, BC/AB 확장, D점의 X 기준 거리 조건을 검사
- AB=CD 변형: CD/AB가 1.272 또는 1.618에 가까운 확장형을 구분 표시
- 사이퍼·샤크·AB=CD 변형을 각각 켜고 끄는 설정 추가
- 하모닉 비율 조건은 허용 오차를 쓰는 근사 구현으로, 실제 차트에서 추가 검증 필요
- 요청에 따라 alertcondition() 및 alert() 호출을 모두 제거. 패턴 구성 확장 후 별도 단계에서 알림을 설계할 예정
### v1.2 캔들 패턴 확장
- 도지: 전체 캔들 범위 대비 작은 몸통으로 식별; 도지는 본질적으로 방향 불확정이며 목표 영역 방향은 최근 가격 움직임을 이용한 표시상 추정
- 상승·하락 하라미: 현재 몸통이 이전 반대색 몸통 내부에 있고 상대적으로 작은지 확인
- 관통형 / 먹구름형: 반대 방향 두 캔들의 몸통 중간값을 종가로 회복·이탈하는 조건
- 집게형 저점 / 집게형 고점: 연속 두 캔들의 저점·고점 차이가 ATR/최소 틱 허용 오차 이내인지 확인
- 인사이드 바 / 아웃사이드 바: 이전 캔들의 고가·저가 범위를 완전히 포함하거나 바깥으로 확장하는지 확인
- 장대양봉 / 장대음봉: ATR 기준 몸통 최소 크기와 전체 범위 대비 몸통 비중을 사용
- 확장 패턴 켜기/끄기, 도지 몸통 비율, 하라미 몸통 비율, 집게형 허용 오차, 장대 몸통 크기 설정 제공
- 기존 캔들 목표 영역·신호 캔들 극값 무효화·박스 개수 제한과 연계; 한 봉에서 여러 형태가 겹치면 우선순위가 높은 대표 라벨 하나를 표시
- v1.1부터 요청에 따라 alertcondition() 및 alert() 호출이 없으며 v1.2도 알림 코드를 포함하지 않음
### v1.9 진단·검증 패널
- 차트 우측 상단 패널에서 현재 봉의 확정 여부와 피벗 오른쪽 확인 봉 수를 표시
- 최근 SMC 구조 이벤트, 하모닉 PRZ, 방향성 반전 캔들의 발생 시점·이름을 표시
- 3중 합류 박스, FVG 박스, 오더 블록의 저장 개수를 요약
- 거래량·ATR·HTF 추세·세션 필터가 켜져 있는지와 현재 상승/하락 방향의 필터 통과 여부를 표시
- 선택 HTF가 활성화되었는지와 피벗 확인 지연/이전 확정 HTF 값 사용에 관한 안내 제공
- 진단 패널은 기본 표시되며 '진단 패널 표시' 옵션으로 끌 수 있음; 탐지 조건이나 박스 생성 로직은 변경하지 않음
- alertcondition() 및 alert() 호출은 포함하지 않음

### v1.8 하모닉·ICT/SMC·반전 캔들 3중 합류
- 하모닉 완성 PRZ, ICT/SMC의 BOS·CHOCH 또는 유동성 스윕, 방향성 반전 캔들 신호를 각각 독립 이벤트로 추적
- 세 신호가 같은 방향이며 설정한 봉 수 이내에 발생하고, 가격 구간이 ATR 허용폭을 적용한 뒤 공통으로 겹칠 때 3중 합류 박스를 생성
- 합류 박스에는 하모닉 패턴명, SMC 이벤트, 캔들 반전 패턴명을 표시
- 신호 간 최대 봉 간격, 가격 허용폭(ATR), 최대 합류 박스 수 설정 제공
- 같은 세 원천 이벤트 조합의 중복 박스를 방지하고, 가장 오래된 원천 이벤트가 시간 창을 벗어나면 종료 표시
- 합류는 근사 조건 기반 분석 보조 표시이며 성공 확률이나 매매 결과를 보장하지 않음; 알림 호출은 계속 없음

### v1.7 쐐기 돌파 필터 및 복합 패턴 합류
- 삼각형·쐐기·채널 등 기하학 패턴의 돌파에서 선택적인 ATR 최소 이탈폭 조건 제공
- 선택적인 돌파봉 몸통 방향 확인: 상승 돌파는 양봉, 하락 돌파는 음봉 조건 추가
- 기본값은 두 필터 모두 꺼짐으로 설정해 기존 돌파 판정과 표시를 유지
- 동일 방향의 일반 가격 갭과 3개 봉 FVG 가격 영역이 겹치면 복합 합류 박스를 생성
- 복합 영역에 오더 블록도 같은 방향으로 겹치면 OB 중첩 태그 추가
- 소스 가격 갭 또는 FVG가 완전 해소되면 복합 합류 박스를 종료하고, 중복 쌍과 최대 박스 수를 관리
- 알림 호출은 계속 포함하지 않음

### v1.6 일반 가격 갭
- 연속한 두 봉의 가격 범위가 겹치지 않는 상승 갭과 하락 갭을 탐지
- ATR 대비 최소 갭 크기를 설정하고 기존 거래량·ATR·상위 시간대 추세·세션 품질 필터를 적용
- 미충전 → 부분 해소 → 완전 해소 상태를 별도로 추적하고, 해소 상태에 따라 박스 색상과 라벨 변경
- 가격 갭 박스 수 상한을 설정해 오래된 박스를 정리
- 3개 봉 기준 FVG와는 별도 모듈이며, 갭 발생이 향후 가격 방향이나 매매 성공을 보장하지 않음
- 알림 호출은 계속 포함하지 않음

### v1.5 품질 필터
- 거래량 필터: 거래량이 설정 기간 평균의 지정 배수 이상일 때 신규 패턴 영역을 허용
- ATR 변동성 필터: ATR/종가 비율이 설정한 최소 퍼센트 이상일 때 신규 패턴 영역을 허용
- 상위 시간대 추세 필터: 이전에 확정된 HTF 종가가 HTF EMA 위/아래인지에 따라 상승/하락 방향을 필터링
- 거래 세션 필터: 사용자가 선택한 세션과 시간대를 벗어난 신규 패턴 영역 생성을 억제
- 네 필터는 각각 독립적으로 켜고 끌 수 있고, 기본값은 모두 꺼져 있어 기존 표시 동작을 유지
- 필터는 새 패턴 영역과 핵심 신호 생성 시점에 적용됩니다. 상위 시간대가 차트와 같거나 낮으면 HTF 추세 필터는 적용되지 않음
- 필터는 신호를 줄이는 옵션이며 매매 결과나 정확도를 보장하지 않음; 알림 호출은 계속 없음

### v1.4 내부·외부 유동성 및 HTF 컨플루언스
- EQH/EQL을 선택한 상위 시간대의 과거 확정 롤링 고가·저가 범위와 비교해 내부 유동성 / 외부 유동성 / 범위 외부로 라벨링
- 상위 시간대 범위 상단·하단과 가까운 EQH/EQL에는 HTF 경계 근접 정보를 추가
- 오더 블록+FVG 겹침 영역이 HTF 범위 상단·하단에 가까우면 컨플루언스 박스에 HTF 위치 태그 추가
- HTF 범위는 `request.security()`에서 이전 확정 HTF 봉의 범위를 사용해 실시간 미확정 HTF 봉에 의한 변동을 줄임
- 상위 시간대, 범위 계산 봉 수, 내부·외부 경계 폭 설정과 HTF 상·하단 단계선 표시 제공
- 차트 시간대가 선택한 HTF보다 같거나 높으면 HTF 분류를 적용하지 않음
- 내부·외부 분류는 과거 HTF 범위와 사용자 허용 폭을 이용한 근사 프록시이며, 모든 ICT 유동성 정의를 대신하지 않음
- 알림 호출은 계속 포함하지 않음

### v1.3 차트 패턴 확장
- 라운딩 바텀 / 라운딩 탑: 7개의 확정 교차 피벗에서 양쪽 테두리·중앙 극값·완만한 회복/하락 구조를 근사 검사
- 컵앤핸들: 왼쪽 테두리, 컵 저점, 비슷한 오른쪽 테두리, 얕은 손잡이 저점의 4개 확정 피벗을 검사
- 확장형 천장 / 확장형 바닥: 5개 피벗의 고점·저점이 서로 멀어지는 구조를 검사
- 다이아몬드 천장 / 다이아몬드 바닥: 9개 확정 교차 피벗에서 확장 후 수렴하는 스윙 구조를 근사 검사
- 각 차트 패턴군의 탐지 on/off, 최소 높이(ATR), 테두리 허용 오차, 최소 스윙 확장 설정 제공
- 기존 넥라인 확인, 목표 영역, 무효화 처리와 연결하며 박스 수 상한을 공유
- 차트 패턴 판별은 단순화한 기하학적 근사이며 모든 교과서적 변형을 포괄하지 않음; 알림 코드는 계속 없음

## 표시 규칙
- 형성 중 패턴: 주황색 계열 구조 박스
- 목표 가격 영역: 패턴 높이 또는 ATR 기반의 반투명 사각 박스
- BOS / CHOCH: 스윙 돌파 레벨 주변에 방향별 박스
- 유동성 스윕: 스윕 캔들의 꼬리 영역을 강조하는 박스
- 오더 블록: 활성은 방향별 색상, 재방문은 주황색, 무효화는 회색
- 무효화·만료된 영역은 회색 계열로 상태 표시

## 설치
1. TradingView 차트를 열고 하단의 Pine Editor를 엽니다.
2. [v1.9 소스 파일](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_9.pine)을 열어 코드를 복사합니다.
3. Pine Editor에 붙여넣고 Save를 누른 뒤 Add to chart를 선택합니다.
4. v1.9에는 알림 호출이 없습니다. 모든 패턴 모듈 확장이 끝난 뒤 별도 단계에서 알림을 추가할 예정입니다.

## 주요 설정
- **탐지 설정**: 피벗 왼쪽·오른쪽 확인 봉 수, ATR 기간, 고점·저점 허용 오차
- **패턴 설정**: 반전·FVG·캔들·기하학 패턴군의 탐지 켜기/끄기
- **추세 지속 패턴**: 깃발·페넌트·박스권·채널 탐지 및 선행 추세 최소 폭
- **돌파·재시험**: 재시험 허용 폭, 박스 최대 개수
- **삼각형·쐐기**: 선택적 돌파 ATR 이탈폭 및 돌파봉 몸통 방향 필터
- **복합 패턴 합류**: 가격 갭+FVG 합류 켜기/끄기, 최소 겹침 폭, 최대 합류 박스 수
- **다중 모듈 합류**: 하모닉+SMC+반전 캔들 합류, 신호 간 최대 봉 간격, ATR 가격 허용폭, 최대 합류 박스 수
- **ICT/SMC 구조**: BOS·CHOCH·스윕 활성화, EQH/EQL 허용 오차, 오더 블록 전체 캔들/몸통 선택
- **하모닉 패턴**: 패턴 감지 켜기/끄기, 피보나치 비율 허용 오차, AB=CD 길이 오차, D점 PRZ 폭 및 최대 박스 수
- **FVG·캔들 설정**: 최소 FVG 크기, 캔들 몸통·핀바 꼬리 조건, 별형 중간 캔들 몸통 비율, 확장 패턴 탐지 켜기/끄기, ATR 목표 거리
- **가격 갭**: 일반 갭 탐지, 최소 갭 크기(ATR), 최대 갭 박스 수, 미충전·부분 해소·완전 해소 상태
- **OB/FVG 컨플루언스**: 오더 블록과 FVG 겹침 탐지, EQH/EQL 인접 허용 폭, 컨플루언스 박스 최대 개수
- **차트 패턴**: 라운딩 바텀/탑, 컵앤핸들, 확장형·다이아몬드 탐지 및 최소 높이·테두리 허용 오차 설정
- **HTF 유동성**: 상위 시간대, 과거 범위 계산 봉 수, 내부·외부 유동성 경계 폭
- **품질 필터**: 거래량 평균 기간·배수, 최소 ATR/종가 %, 상위 시간대 EMA 방향·기간, 세션 및 시간대
- **표시 설정**: 목표 영역 폭, 오른쪽 투영 길이, 목표 박스 최대 개수
- **진단·검증**: 현재 봉 상태, 원천 이벤트 발생 시점, 저장 박스 수, 필터 판정, HTF 기준 정보

## 중요한 한계 및 검증 상태
- 사용자가 v1.8 정상 작동을 확인했습니다. v1.9 진단 패널은 TradingView Pine Editor에서 실제 컴파일 및 차트 검증이 필요합니다. 여기서 수행한 것은 정적 검사이며 TradingView 컴파일러 실행은 아닙니다.
- 최신 v1.9 소스에는 alertcondition() 및 alert() 호출이 없습니다. 알림 기능은 모든 패턴 모듈을 확장한 이후 별도 단계에서 다시 설계할 예정입니다.
- HTF 정보는 상위 시간대의 이전 확정 롤링 범위에서 계산합니다. 사용자가 선택한 HTF가 차트 시간대보다 높지 않으면 HTF 분류를 비활성화합니다.
- 하모닉 패턴의 피보나치 조건은 허용 오차를 가진 근사 판별이며, D점 PRZ는 실제 D 피벗 주변의 ATR 기반 표시 영역입니다. 이는 미래 반전을 보장하지 않습니다.
- BOS/CHOCH의 추세 방향은 스크립트 내부에서 추적하는 단순 편향 상태를 이용합니다. 다양한 ICT/SMC 정의를 완전히 대표하는 것은 아닙니다.
- 오더 블록은 BOS/CHOCH 직전 탐색 범위 내 최근 반대 방향 캔들의 전체 고가~저가로 근사합니다. v1.5의 거래량·ATR·상위 시간대 EMA·세션 필터는 신규 영역 생성에 적용되며, 별도의 전략 최적화나 패턴별 통계 검증을 대신하지 않습니다.
- 다중 모듈 합류는 같은 방향, 설정된 봉 간격, ATR 기반 가격 구간 근접성을 모두 요구하므로 드물게 생성될 수 있습니다. 근접 허용폭이 지나치게 크면 영역이 넓어질 수 있습니다.
- 일반 가격 갭은 연속 두 봉의 고가·저가 범위가 겹치지 않을 때만 탐지합니다. 24시간 거래로 봉 간 갭이 드문 시장이나 시간대에서는 가격 갭 박스가 적게 또는 전혀 나타나지 않을 수 있습니다.
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
- [v1.0 — 오더 블록·FVG 컨플루언스](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_0.pine)
- [v1.1 — 사이퍼·샤크·AB=CD 변형 및 알림 코드 제거](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_1.pine)
- [v1.2 — 추가 캔들 패턴 11종 및 알림 코드 없음](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_2.pine)
- [v1.3 — 라운딩 바텀/탑, 컵앤핸들, 확장형·다이아몬드 패턴](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_3.pine)
- [v1.4 — 내부·외부 유동성 및 HTF 컨플루언스](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_4.pine)
- [v1.5 — 거래량·ATR·HTF 추세·세션 품질 필터](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_5.pine)
- [v1.6 — 일반 가격 갭 및 해소 상태 추적](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_6.pine)
- [v1.7 — 쐐기 돌파 필터 및 가격 갭+FVG 복합 합류](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_7.pine)
- [v1.9 — 진단·검증 패널](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_9.pine)
- [v1.8 — 하모닉+SMC+반전 캔들 3중 합류](https://github.com/viphj8501-tech/universal-pattern-zones/blob/main/universal_pattern_zones_v1_8.pine)

개발 계획은 [패턴 모듈 확장 로드맵](docs/PATTERN_MODULE_ROADMAP.md)을 참조하세요.
