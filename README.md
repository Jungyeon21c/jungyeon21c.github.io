# 이정연 교수 홈페이지

경북대학교 사회과학대학 사회학과 이정연 교수 개인 홈페이지.

## 구조

```
jungyeon-homepage/
├── index.html       — 홈
├── about.html       — 소개 (학력·경력)
├── research.html    — 연구 (논문 목록)
├── teaching.html    — 강의 (강의 목록)
├── lab.html         — 연구실 (멤버 소개)
├── contact.html     — 연락
├── css/
│   └── style.css    — 전체 스타일
├── images/          — 사진 등 이미지
└── papers/          — PDF 첨부용 폴더
```

## 콘텐츠 수정 방법

### 1. 새 논문 추가
`research.html`을 텍스트 편집기로 열어 해당 연도의 `<ul class="pub-list">` 안에 다음 형식으로 한 줄을 추가한다.

```html
<li>
  <span class="pub-title">논문 제목</span>
  <span class="pub-meta"><em>학술지명</em> 권호, 쪽수.</span>
</li>
```

### 2. 강의 추가
`teaching.html`의 `course-list` 안에 다음 블록을 추가한다.

```html
<div class="course-item">
  <div class="course-semester">2025-2학기</div>
  <div class="course-name">의료사회학 <span class="course-meta">(학부)</span></div>
</div>
```

### 3. 연구실 멤버 추가
`lab.html`의 `member-grid` 안에 다음 블록을 추가한다.

```html
<div class="member-card">
  <h3>홍길동</h3>
  <div class="member-role">박사과정</div>
  <p>연구주제: 한국 의료화의 사회사</p>
</div>
```

### 4. 사진 추가
1. 사진 파일을 `images/` 폴더에 넣는다 (예: `images/profile.jpg`).
2. `index.html`에서 다음 줄을 찾는다.
   ```html
   <!-- 이미지 추가 시: <img src="images/profile.jpg" alt="이정연 교수 사진"> -->
   사진 영역
   ```
3. 주석을 풀고 "사진 영역" 글자를 지운다.

### 5. 색상 변경
`css/style.css` 맨 위의 `:root` 부분에서 색상 코드만 바꾸면 전체에 반영된다.

```css
:root {
  --accent: #2c3e50;   /* 진한 남색을 다른 색으로 변경 가능 */
}
```

## GitHub Pages 배포

1. GitHub에 새 저장소(repository)를 만든다. 이름은 `사용자명.github.io`로 한다.
   예: `jungyeon-knu.github.io`
2. 이 폴더의 모든 파일을 그 저장소에 업로드한다.
3. 저장소 Settings → Pages → Source를 `main` 브랜치, 폴더는 `/ (root)`로 설정한다.
4. 몇 분 뒤 `https://사용자명.github.io`에서 접속할 수 있다.

업로드는 GitHub Desktop 앱이나 웹의 "Add file → Upload files"로 간편하게 할 수 있다.

## 로컬에서 미리보기

폴더 안의 `index.html`을 더블 클릭하면 브라우저에서 바로 열린다.

또는 터미널에서:
```bash
cd ~/Documents/jungyeon-homepage
python3 -m http.server 8000
```
브라우저에서 `http://localhost:8000` 접속.
