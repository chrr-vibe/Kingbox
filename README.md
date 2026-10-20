# 임금님 다마고치

임금님 다마고치 웹앱 (PWA)

## 파일 구성
- `index.html` – 게임 본체 (임금님 그림 포함)
- `manifest.webmanifest` – 앱 이름, 아이콘, 홈 화면 설정
- `sw.js` – 오프라인 실행용 서비스워커
- `icon-192.png`, `icon-512.png`, `maskable-512.png`, `apple-touch-icon.png`, `favicon-64.png` – 앱 아이콘
- `.nojekyll` – GitHub Pages가 파일을 그대로 올리게 하는 빈 파일

## GitHub Pages로 올리기
1. GitHub에서 새 저장소(repository)를 만든다.
2. 이 zip을 풀고, 안의 파일을 전부 그대로 저장소에 업로드한다. (`index.html`이 저장소 맨 위에 있어야 함)
3. 저장소 **Settings → Pages** 에서 Branch를 `main` / `/ (root)` 로 고르고 Save.
4. 1~2분 뒤 `https://아이디.github.io/저장소이름/` 으로 접속.
5. 휴대폰 Chrome 메뉴 → **홈 화면에 추가 / 앱 설치**. (아이폰은 Safari → 공유 → 홈 화면에 추가)

## 업데이트할 때
`index.html`을 바꿔서 올린 뒤, `sw.js` 맨 위의 `VERSION` 을 `v2`, `v3` … 처럼 하나씩 올려주면 설치된 앱에도 새 버전이 반영된다.

## 저장 데이터
진행 상황(방, 옷, 테마, 배경, 영감·관심·건강 타이머)은 접속한 브라우저 안(localStorage)에 저장된다.
주소가 바뀌면(예: 파일로 열던 것 → GitHub 주소) 저장 데이터는 새로 시작한다.
