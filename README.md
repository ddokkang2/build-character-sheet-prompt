# Character Sheet Prompt Builder

첨부한 전신 인물·캐릭터 이미지를 분석하여 **일관된 4패널 캐릭터 시트용 영문 이미지 생성 프롬프트**를 작성하는 Codex 스킬입니다.

Nano Banana Pro, FLUX, Midjourney 등에서 사용할 수 있도록 외형, 얼굴, 머리카락, 의상, 재질, 색상, 신발, 소품과 비대칭 디테일까지 구조적으로 정리합니다.

## 4패널 구성

| 패널 | 구성 | 필수 프레이밍 |
| --- | --- | --- |
| 1 | 정면 의상·신체 뷰 | 얼굴과 머리를 완전히 제외하고 목 밑부터 신발 밑창까지 표시 |
| 2 | 정확한 90도 측면 전신 | 머리 꼭대기부터 신발까지 표시하며 3/4 각도와 몸통 회전 금지 |
| 3 | 후면 전신 | 머리 꼭대기부터 신발까지 크롭 없이 표시 |
| 4 | 얼굴 클로즈업 | 동일 인물의 머리, 얼굴, 목, 어깨 상단과 식별 특징 표시 |

모든 패널은 동일한 인물, 신체 비율, 의상 구조, 색상, 소재, 액세서리, 조명과 렌더링 스타일을 유지하도록 강하게 제한합니다.

## 주요 기능

- 레퍼런스 이미지에서 보이는 캐릭터 정체성과 신체 비율 분석
- 헤어스타일, 헤어라인, 모발 색상과 세부 질감 분석
- 얼굴형, 눈, 코, 입, 피부톤, 메이크업, 흉터와 표식 분석
- 상의, 하의, 아우터, 장갑, 벨트, 신발과 레이어 구조 분석
- 무기, 홀스터, 가방, 안경, 장신구와 부착 위치 분석
- 정확한 90도 측면 실루엣과 좌우 비대칭 요소 보존
- 중립적인 연회색 스튜디오 배경과 일관된 제품 촬영 조명 지정
- 크롭, 3/4 측면, 다른 의상, 다른 얼굴과 잘못된 좌우 반전을 방지하는 네거티브 제약 생성

## 설치

### 방법 1: Codex에서 설치 요청

Codex에 아래와 같이 요청합니다.

```text
$skill-installer 다음 GitHub 저장소의 스킬을 설치해줘:
https://github.com/ddokkang2/build-character-sheet-prompt
```

### 방법 2: Git으로 직접 설치

OpenAI 공식 스킬 위치인 사용자 폴더의 `$HOME/.agents/skills` 아래에 저장소를 복제합니다.

#### Windows PowerShell

```powershell
New-Item -ItemType Directory -Force "$HOME\.agents\skills" | Out-Null
git clone https://github.com/ddokkang2/build-character-sheet-prompt.git "$HOME\.agents\skills\build-character-sheet-prompt"
```

#### macOS / Linux

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/ddokkang2/build-character-sheet-prompt.git "$HOME/.agents/skills/build-character-sheet-prompt"
```

설치 후 스킬이 바로 나타나지 않으면 Codex를 재시작합니다.

## 사용 방법

1. 캐릭터의 전신이 잘 보이는 이미지를 첨부합니다.
2. 스킬 이름과 원하는 결과를 함께 입력합니다.

```text
$build-character-sheet-prompt 첨부한 캐릭터를 분석해서
4패널 캐릭터 시트 이미지 생성 프롬프트를 만들어줘.
```

영문 요청 예시:

```text
Use $build-character-sheet-prompt to analyze the attached character image
and create a production-ready four-panel character reference sheet prompt.
```

## 입력 권장사항

- 머리부터 신발까지 선명하게 보이는 전신 이미지
- 의상과 액세서리가 가려지지 않은 이미지
- 가능하면 높은 해상도와 중립적인 자세
- 추가 정면·측면·후면·얼굴 이미지가 있다면 함께 첨부

한 장에서 보이지 않는 영역은 눈에 보이는 디자인을 바탕으로 가장 단순하고 일관된 형태로 이어지며, 새로운 로고·무기·액세서리를 임의로 추가하지 않습니다.

## 출력 형식

스킬은 다음 형식으로 결과를 반환합니다.

1. 빈칸이나 플레이스홀더가 없는 완성형 영문 이미지 생성 프롬프트
2. 캐릭터 핵심 특징과 프레이밍 규칙을 설명하는 2–3문장의 한국어 요약

> 이 스킬은 기본적으로 **이미지를 직접 생성하지 않고 프롬프트를 작성**합니다. 이미지 생성은 별도로 요청해야 합니다.

## 배경과 조명 규격

- 모든 패널에 동일한 neutral light grey studio background
- soft studio product photography lighting
- 전신 패널의 발밑에 subtle grounded contact shadows
- 동일한 광원 방향, 노출, 색온도와 재질 표현

## 저장소 구조

```text
build-character-sheet-prompt/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── four-panel-spec.md
```

- `SKILL.md`: 스킬 실행 절차와 핵심 프레이밍 규칙
- `references/four-panel-spec.md`: 상세 4패널 구성과 보존·네거티브 제약
- `agents/openai.yaml`: Codex UI 표시용 메타데이터

## 수동 설치본 업데이트

Git으로 직접 설치했다면 다음 명령으로 최신 버전을 받을 수 있습니다.

```powershell
git -C "$HOME\.agents\skills\build-character-sheet-prompt" pull
```

## 참고

Codex 스킬의 구조, 설치 위치와 호출 방식은 [OpenAI 공식 스킬 문서](https://learn.chatgpt.com/docs/build-skills)를 참고하세요.
