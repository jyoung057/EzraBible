# 노우호목사님 성경강해 플레이어

로컬 mp3 강의 폴더를 선택해 재생하는 PWA입니다.

## GitHub Pages 배포

1. GitHub에 새 저장소를 만들고 이 폴더를 올립니다.

```bash
git init
git add .
git commit -m "Add Bible lecture PWA player"
git branch -M main
git remote add origin https://github.com/사용자이름/저장소이름.git
git push -u origin main
```

2. GitHub 저장소 → **Settings** → **Pages**
3. **Source**: `Deploy from a branch`
4. **Branch**: `main` / `/ (root)` 저장
5. 수 분 후 아래 주소로 접속합니다.

`https://사용자이름.github.io/저장소이름/`

6. 안드로이드 Chrome에서 연 뒤 **⋮ → 홈 화면에 추가 / 앱 설치**

## 로컬 확인

```bash
python -m http.server 8000
```

브라우저에서 `http://127.0.0.1:8000/` 접속

## 구성

| 파일 | 설명 |
|------|------|
| `EZRA_Bible.html` | 플레이어 |
| `index.html` | Pages 진입점 |
| `manifest.webmanifest` | PWA 설정 |
| `sw.js` | 오프라인 캐시 |
| `icons/` | 앱 아이콘 |

강의 mp3는 저장소에 올리지 않아도 됩니다. 앱을 연 뒤 기기·USB에서 폴더/파일을 선택해 재생합니다.
