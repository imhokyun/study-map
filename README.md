# 📚 기말고사 학습맵 (2026년도 1학기)

강의 노트를 **접이식 fishbone 마인드맵**으로 보는 active-recall 학습 도구.
노드(가지)를 눌러 답을 떠올린 뒤 펼쳐서 확인하는 방식.

## 🔗 보기 (모바일 OK)

GitHub Pages: **https://imhokyun.github.io/study-map/**

> 홈 화면에 추가하면 앱처럼 전체화면으로 쓸 수 있습니다.

## 구성

- `index.html` — 과목 선택 랜딩 페이지
- `1. 빅데이터 자연어처리/` — 과목별 학습맵
  - `index.html` — 마인드맵 뷰어 (검색·전체펼치기/접기)
  - `study-data/manifest.json` — 강의 목록
  - `study-data/NN_*.json` — 강의별 노드 데이터 (`{name, children}` 중첩 구조)

새 강의 추가: `study-data/`에 `NN_Topic.json` 추가 → `manifest.json`의 `lectures`에 파일명 등록 → 새로고침.

## 공개 범위

교재 PDF·강의 녹취·발표자료 원본 등은 `.gitignore`로 제외(저작권·개인정보·용량).
공개되는 건 직접 정리한 학습맵 데이터(JSON)와 뷰어뿐.

## 로컬에서 보기

`fetch()`로 JSON을 불러오므로 `file://`로 열면 막힙니다. 로컬 서버로 실행하세요:

```bash
python3 -m http.server 8000
# http://localhost:8000
```
