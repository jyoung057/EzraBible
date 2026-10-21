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
| `hymns.js` | 찬송가 장 번호·제목 목록(645장) |
| `icons/` | 앱 아이콘 |

강의 mp3는 저장소에 올리지 않아도 됩니다. 앱을 연 뒤 기기·USB에서 폴더/파일을 선택해 재생합니다.

## 찬송가 악보

- 목록(`hymns.js`)만 앱에 들어 있고, **악보 이미지는 저장소에 올리지 않습니다**(저작권).
- 찬송가 탭 → **악보 가져오기**로 이미지를 선택하면 이 기기(브라우저 저장소)에 저장되어, 이후 다시 고르지 않아도 오프라인으로 열립니다.
- 파일 이름은 장 번호입니다. 예: `1.jpg`, `001.png`, `645.webp`
- 한 번에 고를 수 있는 수가 제한되면 나누어 여러 번 가져오세요(이미 저장된 장은 유지됩니다).
- PC에서 강의 폴더 안에 `hymm`(또는 `hymn`, `찬송가`) 폴더를 두면 자동으로 인식하고, **열린 폴더 악보 저장** 버튼으로 기기에 저장할 수 있습니다.
- `찬송가목록.xlsx`는 목록 원본이며 `.gitignore`로 제외됩니다.
