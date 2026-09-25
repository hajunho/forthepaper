<p align="right"><a href="README.md">English</a> · <b>한국어</b></p>

# 판정문, 분야별

> **이 폴더의 모든 판정문은 AI가 초안을 쓴 것이며, 어느 것이든 틀릴 수 있다.** 판정문은 [000_tier.ko.md](../000_tier.ko.md)의 T-Grade 척도를 적용한 것이고, 이 척도는 아직 사람 판정자를 상대로 검증되지 않았다(척도의 부록 B). 판정문은 논문을 매기는 것이지 결코 저자를 매기는 것이 아니다. 같은 분야 폴더 안의 이웃들 사이에서만 유효하다. 세 문장의 판정 없이 유통되어서는 안 된다. 그리고 논문의 본문은 결코 여기 옮겨 싣지 않는다. 각 판정문은 서지 정보와 식별자를 담으며, 독자는 논문 자체를 읽어야 한다.

## 폴더 구성 방식

척도의 금지 3에 따라 등급은 한 분야 안에서만 의미가 있다. 폴더 구조가 이를 강제한다. **분야마다 폴더 하나, 비교는 폴더 경계에서 멈춘다.**

분류 체계는 OECD *연구개발 분야 분류*(Frascati Manual, 2015)를 따른다. 공개되어 있고, 안정적이며, 각국 통계 기관이 이미 쓰고 있기 때문이다. 최상위 폴더는 여섯 개 대분야이고, 하위 폴더는 2단계 분류명을 케밥 케이스로 쓴다.

| 폴더 | 대분야 | 하위 폴더 예 |
|---|---|---|
| `natural-sciences/` | 자연과학 | `mathematics`(수학), `computer-and-information-sciences`(컴퓨터·정보과학), `physical-sciences`(물리학), `chemical-sciences`(화학), `earth-and-environmental-sciences`(지구·환경과학), `biological-sciences`(생물학) |
| `engineering-and-technology/` | 공학·기술 | `civil-engineering`(토목), `electrical-electronic-and-information-engineering`(전기·전자·정보공학), `mechanical-engineering`(기계), `chemical-engineering`(화학공학), `materials-engineering`(재료), `medical-engineering`(의공학), `environmental-engineering`(환경공학), `nano-technology`(나노기술) |
| `medical-and-health-sciences/` | 의학·보건 | `basic-medicine`(기초의학), `clinical-medicine`(임상의학), `health-sciences`(보건학), `medical-biotechnology`(의료생명공학) |
| `agricultural-and-veterinary-sciences/` | 농업·수의학 | `agriculture-forestry-and-fisheries`(농림수산), `animal-and-dairy-science`(축산·낙농), `veterinary-science`(수의학), `agricultural-biotechnology`(농업생명공학) |
| `social-sciences/` | 사회과학 | `psychology-and-cognitive-sciences`(심리·인지과학), `economics-and-business`(경제·경영), `education`(교육학), `sociology`(사회학), `law`(법학), `political-science`(정치학), `social-and-economic-geography`(사회·경제지리), `media-and-communications`(미디어·커뮤니케이션) |
| `humanities-and-the-arts/` | 인문·예술 | `history-and-archaeology`(역사·고고학), `languages-and-literature`(언어·문학), `philosophy-ethics-and-religion`(철학·윤리·종교), `arts`(예술) |

논문은 게재 학술지의 분야가 아니라 **논문이 기여를 주장하는 분야**(척도의 5장 사례 6)에 둔다. 둘이 다르면 판정문의 0단계에서 그렇게 밝힌다. 두 분야에 기여를 주장하는 논문은 두 분야의 기준으로 모두 매기고, 주된 분야에 두며, 메모를 남긴다.

## 여기 있는 모든 판정문의 규칙

1. **고지가 먼저다.** 각 판정문 맨 위의 오류 가능성 고지는 선택 사항이 아니며 각주도 아니다.
2. **워크시트 전체를 공개한다.** 척도의 부록 A에 따라 분야와 번역, 주장 문장과 근거 문장, 이유가 딸린 여덟 가지 답, 세 문장의 판정, 경계 표시, 검증 기록.
3. **논문의 본문은 싣지 않는다.** 제목, 저자, 게재지, 식별자, 그리고 요약 서술만. PDF도, 긴 인용도, 저자에게 속한 보충 자료도 싣지 않는다.
4. **답변권.** 저자는 [이슈 템플릿](https://github.com/hajunho/forthepaper/issues/new/choose)으로 답변한다. 답변은 원문 그대로 덧붙여지며 사람의 재검토를 촉발한다.
5. **번호는 전체 통합**(`001`, `002`, …)이다. 판정문을 번호로 인용할 수 있게 하기 위해서이며, 분야는 폴더가 말해 준다.
6. **언어.** 판정문은 영어로 쓰고, 논문이 다른 언어로 쓰였으면 그 언어로도 `.ko.md`(또는 해당 언어 코드) 대응본을 둔다.

## 목록

| 번호 | 논문 | 폴더 | 등급 | 경계 | 사람 재검토 | 저자 답변 |
|---|---|---|---|---|---|---|
| [001](social-sciences/education/001_one_movie_two_perspectives.ko.md) · [English](social-sciences/education/001_one_movie_two_perspectives.md) | 김자미·정재림 (2023), 「하나의 영화, 서로 다른 두 시선」, *한국어문교육* 45, 167–190. [DOI](https://doi.org/10.24008/klle.2023..45.006) | `social-sciences/education` | **T6** | T6/T5 | 대기 중 | 아직 없음 |

## 판정 제안하기

논문(제목, 게재지, DOI)과 적절하다고 생각하는 분야 폴더를 적어 이슈를 열어 달라. 논문 파일은 첨부하지 않는다. 판정문은 AI 판정자가 게재된 전문을 읽고 초안을 쓰며, 병합 전에 관리자를 거친다.
