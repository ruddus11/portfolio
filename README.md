# 추경연 포트폴리오 사이트

(주)플랜아이 지원용 한 페이지 정적 포트폴리오입니다. 빌드 과정 없이 `index.html`, `style.css`, `script.js` 세 파일로 동작합니다.

## 로컬에서 확인

```bash
python3 -m http.server 8000
# 브라우저에서 http://localhost:8000 접속
```

## GitHub Pages 배포

1. GitHub에서 새 저장소를 만듭니다. 사용자 사이트로 쓰려면 이름을 `<GitHub아이디>.github.io`로 합니다.
2. 이 폴더의 파일(`index.html`, `style.css`, `script.js`, `README.md`)을 저장소 루트에 올립니다.
   ```bash
   git init
   git add .
   git commit -m "포트폴리오 사이트 추가"
   git branch -M main
   git remote add origin https://github.com/<GitHub아이디>/<저장소이름>.git
   git push -u origin main
   ```
3. 저장소의 Settings > Pages에서 Source를 `Deploy from a branch`, Branch를 `main` / `/ (root)`로 선택하고 저장합니다.
4. 잠시 후 `https://<GitHub아이디>.github.io/` (일반 저장소는 `/<저장소이름>/`) 주소로 공개됩니다.

## PDF로 저장

브라우저에서 인쇄(Ctrl/Cmd + P)를 누르고 대상을 PDF로 저장하면 인쇄용 스타일이 적용됩니다.

## 참고

- 글꼴은 Pretendard를 jsDelivr CDN에서 불러옵니다. 로드되지 않으면 시스템 한글 글꼴로 대체됩니다.
- 색, 간격, 글자 크기는 `style.css` 상단의 토큰(Astryx 디자인 시스템 이름과 단계)으로 관리합니다. 링크 색은 `--color-text-accent` 하나만 바꾸면 됩니다.
- 시스템이 다크 모드면 어두운 색으로 자동 전환됩니다.
