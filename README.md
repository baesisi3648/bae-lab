# bae lab

게임으로 배우는 생명과학 — 수업용 게임 링크 모음 페이지.

페이지는 `index.html` 하나입니다. 빌드도, 설치도 없습니다.
(`fonts/`에는 도트 폰트 파일만 들어 있습니다.)

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
      <span class="visit">VISIT ▶</span>
    </div>
  </a>
</li>
```

- 아직 만드는 중이면 `<span class="badge">LIVE</span>` → `<span class="badge wip">BUILDING</span>`
- 링크가 두 개 이상이면 와일드 더비 카드(`class="links"` 부분)를 참고하세요
- 카드를 늘렸으면 히어로 아래 `2 live` 숫자도 같이 고쳐주세요

## 배포

**Cloudflare Pages** — 대시보드 → Workers & Pages → Create → Pages → Connect to Git →
이 저장소 선택. 설정은 아래처럼 두면 됩니다.

| 항목 | 값 |
| --- | --- |
| Framework preset | `None` |
| Build command | 비움 |
| Build output directory | `/` |

빌드 단계가 없어서 `main`에 푸시하면 몇 초 만에 자동 재배포됩니다.

**GitHub Pages** — Settings → Pages → 브랜치 루트 선택.

## 링크 주의

와일드 더비(Apps Script)는 **재배포할 때마다 주소가 바뀔 수 있습니다.**
앱스 스크립트에서 "배포 관리 → 편집 → 새 버전"으로 올리면 주소가 유지되고,
"새 배포"로 만들면 주소가 새로 생기니 그때는 `index.html`의 두 링크를 갱신해야 합니다.

## 디자인

메이플스토리풍 도트 픽셀. 양피지 바탕에 나무 표지판, 카드는 퀘스트 창처럼 이중선 프레임입니다.
색을 바꾸려면 `index.html` 맨 위 `:root` 블록만 고치면 전체에 반영됩니다.

| 역할 | 값 |
| --- | --- |
| 양피지 배경 | `#f4e4c1` |
| 카드 바탕 | `#fbeed0` |
| 먹색 텍스트·테두리 | `#3d2b17` |
| 나무 (헤더·푸터) | `#8b5a2b` |
| 옅은 선 | `#c9a877` |
| 포인트 | 하늘 `#5fc9f8` · 잔디 `#7ac74f` · 금 `#f2b233` |

### 글자 크기는 아무 값이나 쓰면 안 됩니다

도트 폰트는 **네이티브 크기의 정수배에서만** 또렷합니다. 17px 같은 어중간한 값을 쓰면 도트가 뭉개집니다.

- `Galmuri11` → 11 / 22 / 33px (본문은 22px)
- `Galmuri14` → 14 / 28 / 42 / 56px (제목)
- `GalmuriMono11` → 11px (뱃지·태그·라벨)

같은 이유로 `border-radius`는 0, 테두리는 3~4px, 그림자는 흐림 없는 오프셋만 씁니다.

폰트는 [갈무리](https://github.com/quiple/galmuri)이며 `fonts/`에 직접 담아 씁니다 (SIL OFL, `fonts/GALMURI-LICENSE.txt`).
