# SPeventpage — 블랙 오너 위크 이벤트 페이지

`https://thehyoosik-bow.preview.webdot.co.kr/` 프리뷰 사이트를 원본 그대로 가져온 소스입니다.
HTML·이미지 모두 서버에서 받은 바이트 그대로이며(SHA-256 검증 완료), 경로는 전부 상대경로라 별도 수정 없이 바로 동작합니다.

**테스트 페이지 (GitHub Pages):** https://dwww9292-collab.github.io/SPeventpage/
`main` 브랜치에 푸시하면 1~2분 뒤 자동으로 반영됩니다.

## 페이지

| 파일 | 내용 |
| --- | --- |
| `dark.html` | 시안 A · DARK (메인 이벤트 페이지) |
| `light.html` | 시안 G · LIGHT |
| `kv.html` | 메인 배너(KV) — `kv.html?k=...` 파라미터로 배너 전환 |
| `index.html` | 시안 선택 페이지 (dark / light 썸네일) |

## 폴더 구조

```
.
├── index.html
├── dark.html
├── light.html
├── kv.html
├── assets/
│   ├── person.png, h-*.png      # 지점(호텔) 이미지
│   ├── icon-1.png ~ icon-13.png # 아이콘
│   └── kv/                      # 메인 배너용 이미지·SVG
└── shots/                       # index.html 썸네일
```

CSS·JS는 각 HTML 파일 안에 인라인으로 들어 있습니다. 폰트(Pretendard)는 jsDelivr CDN에서 불러옵니다.

## 로컬에서 미리보기

```bash
python3 -m http.server 8000
# → http://localhost:8000/dark.html
```

## 배포

정적 파일만으로 구성되어 있어 GitHub Pages(Settings → Pages → `main` 브랜치 / root)나 기존 웹 서버에 그대로 올리면 됩니다.
