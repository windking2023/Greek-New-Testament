# Greek NT Reader — Galatians 2–6 검증 보고서

기준본: `galatians_1_pauline_golden_master_v1_0.html`. 1장은 바이트 단위로 보존했습니다. 2→3→4→5→6 순서로 독립 HTML을 생성하고 검사했습니다.

| 장 | 절 | 토큰 | lemma | 5층 연구 | 이형 패널 | 논증 구간 | 동사 RED | 명사 GREEN |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 2 | 21 | 385 | 156 | 28 | 4 | 8 | 78 | 86 |
| 3 | 29 | 455 | 151 | 31 | 3 | 7 | 82 | 120 |
| 4 | 31 | 444 | 167 | 31 | 9 | 7 | 85 | 92 |
| 5 | 26 | 313 | 157 | 29 | 5 | 7 | 62 | 86 |
| 6 | 18 | 267 | 124 | 23 | 3 | 6 | 49 | 54 |

합계: 125절 / 1,864토큰 / 주요 단어 연구 142개 / 본문이형 패널 24개. lemma 수는 각 장의 고유 lemma 수이며 장 간 중복을 포함합니다.

## 통과한 자동검증

- 원자료와 원문·lemma·POS·morphology의 토큰별 대조 및 절 누락 검사. 문장부호는 보존하고 SBL 장치기호는 별도 청색 ※ 계층으로 옮겼습니다.
- 모든 토큰 ID 및 실제 DOM ID의 유일성.
- lemma coverage 100%, 모든 토큰의 영·한 lexical gloss, 영문 발음과 한국어 근사 발음의 표시.
- 1,864개 단어 팝업을 실제 DOM 클릭으로 열고 lemma·형태분석·영한 어휘 뜻을 확인.
- 주요 연구 142개 각각의 5층이 정확한 절·lemma에 연결됨. 반복 출현을 포함한 연구 팝업 발생 위치는 160개.
- 모든 본문이형의 실제 표시 위치, 팝업의 SBLGNT/UBS5/TR 및 4개 해설층.
- 동사 356개 RED, 명사 438개 GREEN의 실제 계산된 CSS 색상 검사.
- 단어 음성 1,864회, 절 음성 125회의 Web Speech API 호출 및 전달 문자열 확인. Greek voice 선택과 voice 목록이 비어 있을 때의 el-GR fallback 확인.
- `speakGreek()` 함수는 기준본과 바이트 단위 동일: speechSynthesis / el-GR / rate 0.72 / pitch 1.
- 실행 코드 fetch 호출=0 / MP3 자산·호출=0 / 외부 TTS=0 / 외부 JS·CSS 로드=0. 브라우저 테스트 중 외부 요청=0.
- 갈라디아서 1–6장 파일 매핑. 2–6장 주소 검색과 절 이동, 상단 메뉴 접기/펼치기 통과.
- index의 요한복음 1–21장 파일명 매핑은 수정 전과 완전히 동일. 요한복음 파일은 수정하지 않았습니다.
- 브라우저 page error=0.

## 검증의 범위

브라우저에서 음성 API를 시험용 구현으로 바꾸어 클릭 이벤트, 음성 텍스트, 언어, 속도, 높이, Greek voice 선택을 검사했습니다. 실제 휴대폰의 스피커 출력이나 발음을 여기서 청취한 것은 아닙니다. 기기의 Greek TTS 음성이 설치되어 있어야 오프라인 실음성 출력이 가능합니다.

1장 원본 자체를 다시 작성하거나 고치지 않았습니다. 2–6장의 팝업 데이터 키는 원본의 조회 방식(v:lemma)에 맞추었으며, 상태 표시는 이미 선언되어 있는 statusEl을 사용하여 실제 검증 결과가 화면에 나오게 했습니다. 음성 함수와 화면 구조·색상 규칙은 그대로 계승했습니다.

본문이형 2:12는 세 판본 자체의 차이가 아니라 의미 있는 다른 사본 독법을 비교하는 패널입니다. 사본 간 차이와 판본 간 차이를 명시했습니다. TR 비교는 Stephanus 1550을 사용했습니다. UBS5는 바울서신에서 유지되는 NA/UBS 본문과 선택한 이형 위치의 UBS 번역 자료로 교차 확인했으며 UBS5 인쇄본 전체를 재현하거나 장치 전체를 직접 대조했다고 주장하지 않습니다. 단어 해설의 해석 논쟁은 본문이형과 분리했습니다.

## 원자료와 출처

- MorphGNT 6.12 Galatians: https://github.com/morphgnt/sblgnt/blob/master/69-Ga-morphgnt.txt
- SBLGNT 공식 본문·장치 PDF: https://www.sblgnt.com/download/SBLGNTpdf.zip
- SBLGNT 공식 소스 및 CC BY 4.0: https://github.com/Faithlife/SBLGNT
- MorphGNT 형태분석·lemma: James K. Tauber, CC BY-SA 3.0; https://github.com/morphgnt/sblgnt
- TR Stephanus 1550 Greek text: https://biblehub.com/tr/galatians/2.htm (3–6장 같은 주소 체계)
- UBS/SBL 판본 관계: https://www.sbl-site.org/resources/digital-texts/
- UBS 번역 연구 자료의 선택 위치: https://tips.translation.bible/tip_verse/gal-24/ ; https://tips.translation.bible/tip_verse/gal-524/
- 사본 독법 교차 확인: https://bterry.com/tc2/lay18gal.htm (해설을 전재하지 않았습니다.)

## 제작·편집 기록

사용자: 순수 Greek NT Reader의 범위, 절대 기준본, 5층 연구, 금지사항, 음성 보존 및 검증 기준 지정. AI: 원자료 정리, 영한 어휘 의미 및 연구 설명 작성, 프로그램 검증. 사용자가 새 연구 설명을 직접 수정·승인한 기록은 아직 없습니다. 연구 내용은 검토 가능한 편집 초안이며 사람의 저작 여부나 저작권 등록에 관한 법적 결론을 이 기록으로 단정하지 않습니다.

## 파일별 SHA-256

- `galatians_1_pauline_golden_master_v1_0.html`: `d4daa768b6ba4023832c604d9ee15e11c7dc1b40f58ab9b0c146b5de11c1ee45`
- `galatians_2_pauline_golden_master.html`: `bb5b4fb8fb8affd6c2cf8ef6606d3cc0bf4c3f11b6389ae023f83aa02b0634dd`
- `galatians_3_pauline_golden_master.html`: `344a208e12150c8303be53f6dd953dd81d35ad0badf48ba3ddcca61df45db866`
- `galatians_4_pauline_golden_master.html`: `34fd339e352a8522ca623b699d7352d14a7c7a9e3a4a7f0c33a5d470728f187c`
- `galatians_5_pauline_golden_master.html`: `6e3e70e693cd0b9f2a112538322dd0a59ec763cf22cfcfd1ad3641b83d2233dc`
- `galatians_6_pauline_golden_master.html`: `c84098c5ea1bdaaa81da1e6b00043828ec3738fe4f07cc704c1d504997d8d37c`
- `index.html`: `528f32ac0c888951a2bd52284814150d242c482c47329ad8e675651c33538f7f`
