# bae lab

게임으로 배우는 생명과학 — 수업용 게임 링크 모음 페이지.

파일은 `index.html` 하나입니다. 빌드도, 설치도 없습니다.

## 보기

`index.html`을 더블클릭하면 브라우저에서 바로 열립니다.

## 게임 추가하기

`index.html`에서 `<ul class="grid">` 안에 카드 블록 하나를 복붙하고 내용만 바꾸면 됩니다.

링크가 하나인 게임:

```html
<li>
  <a class="card" href="게임 주소" target="_blank" rel="noreferrer">
    <div class="card-top">
      <h3>게임 이름</h3>
      <span class="badge">LIVE</span>
    </div>
    <p>한두 문장 설명.</p>
    <div class="card-foot">
      <div class="tags">
        <span>태그1</span>
        <span>태그2</span>
      </div>
      <span class="visit">visit →</span>
    </div>
  </a>
</li>
```

- 아직 만드는 중이면 `<span class="badge">LIVE</span>` → `<span class="badge wip">BUILDING</span>`
- 링크가 두 개 이상이면 와일드 더비 카드(`class="links"` 부분)를 참고하세요
- 카드를 늘렸으면 히어로 아래 `2 live` 숫자도 같이 고쳐주세요

## 배포

**Cloudflare Pages** — 대시보드 → Workers & Pages → Create → Pages → Upload assets → 이 폴더를 드래그.
(Bio Marble이 이미 Cloudflare Pages에 올라가 있어 같은 계정에서 바로 됩니다.)

**GitHub Pages** — 저장소에 올리고 Settings → Pages → 브랜치 루트 선택.

## 링크 주의

와일드 더비(Apps Script)는 **재배포할 때마다 주소가 바뀔 수 있습니다.**
앱스 스크립트에서 "배포 관리 → 편집 → 새 버전"으로 올리면 주소가 유지되고,
"새 배포"로 만들면 주소가 새로 생기니 그때는 `index.html`의 두 링크를 갱신해야 합니다.

## 디자인

[baesisi.org](https://baesisi.org)와 같은 토큰을 씁니다 — 흰 배경(`#ffffff`),
먹색 텍스트(`#0a0a0a`), 회색 보조(`#666666`), 경계선(`#eaeaea`), Pretendard.
색을 바꾸려면 `index.html` 맨 위 `:root` 블록만 고치면 전체에 반영됩니다.
