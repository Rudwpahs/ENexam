# ENexam — 영어 듣기 수행 연습

중학교 영어 3학년 Lesson 5·6·7 듣기 수행을 반복해서 연습하려고 만든 웹앱입니다. 교과서 MP3를 사이트에 올려두는 대신, 사용자가 가지고 있는 음원을 브라우저에서 직접 불러오는 방식으로 만들었습니다.

## 범위와 기능

- Lesson 5·6·7의 Listen & Talk 1 / 2
- Reading, Do It Yourself는 제외
- 5·6·7과 필터
- 0.8× / 1.0× / 1.2× 재생 속도
- 5초 되감기
- 빈칸 즉시 채점
- 정답 보기
- 혼합 모의 연습

## 음원은 어떻게 처리하나

MP3 파일은 서버로 보내지 않습니다. 사용자가 고른 파일을 브라우저 안에서만 읽습니다.

```text
사용자가 MP3 또는 ZIP 선택
        ↓
ZIP이면 JSZip으로 브라우저에서 압축 해제
        ↓
선택한 파일 중 연습에 필요한 MP3 찾기
        ↓
Lesson / Listen & Talk 항목과 연결
        ↓
브라우저의 Audio 객체로 재생
        ↓
사용자가 빈칸 답 입력
        ↓
정답과 비교해 즉시 채점
```

이 구조를 택한 이유는 간단합니다. 교과서 음원을 저장소나 서버에 복사하지 않고도 실제 가지고 있는 음원으로 연습할 수 있기 때문입니다.

## 사용 방법

1. 사이트에서 `MP3/ZIP 선택`을 누릅니다.
2. NE능률 중3 김성곤 교과서의 전체 ZIP, 5·6·7과 ZIP 또는 개별 MP3를 선택합니다.
3. 처음에는 1.0×로 듣고, 어려운 부분만 0.8×로 다시 듣는 식으로 연습합니다.

## 바로 실행

GitHub HTML Preview:

`https://html-preview.github.io/?url=https://github.com/Rudwpahs/ENexam/blob/main/index.html`

GitHub Pages 주소:

`https://rudwpahs.github.io/ENexam/`

## 기술

- HTML / CSS / JavaScript
- JSZip
- Browser Audio API
- GitHub Pages
