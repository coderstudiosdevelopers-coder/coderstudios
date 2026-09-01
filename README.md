# Coder Studios

Coder Studios 앱 소개 웹사이트. 정적 HTML이라 빌드 도구가 필요 없습니다.

**공개 주소:** https://coderstudiosdevelopers-coder.github.io/coderstudios/

## 파일

| 파일 | 설명 |
|---|---|
| `index.html` | 메인 페이지. CSS·JS 모두 이 파일 안에 있습니다. |
| `privacy.html` | 개인정보처리방침 (스토어 심사에 필요) |
| `terms.html` | 이용약관 |
| `.nojekyll` | GitHub Pages의 Jekyll 처리 끄기 |

## 배포

Settings → Pages → Source 를 **Deploy from a branch**, 브랜치 `main` / `(root)` 으로 설정하면 됩니다.
이후 `main` 에 커밋할 때마다 1~2분 내에 자동 반영됩니다.

## 내용 수정

전부 `index.html` 한 파일 안에 있고, 앱마다 `<!-- ===== 앱이름 ===== -->` 주석으로 구분해 뒀습니다.

| 바꿀 것 | 찾을 위치 |
|---|---|
| 앱 이름·설명·특징 | 주석 아래의 `<h3>`, `<p>`, `.feat` |
| 스토어 링크 | `<a class="store" href="...">` |
| 다운로드 수 | `<span class="meta">다운로드 1만+</span>` |
| 앱 카드 추가 | `<article class="app rv">` 블록을 통째로 복사 |
| 아이콘 색 | `class="icon ic-memo"` → CSS의 `.ic-memo` ~ `.ic-stock` |
| 문의 이메일 | `coderstudiosdevelopers@gmail.com` (index·privacy·terms) |
| 브랜드 색 | CSS 상단 `:root` 의 `--blue` |

## 앱 목록 (2026.09 기준)

| 앱 | 패키지 | 다운로드 |
|---|---|---|
| 심플메모 | `com.coderstudios.simplememo` | 1만+ |
| 모두의 신고 | `com.coderstudios.easyreport` | 1천+ |
| 심플 QR | `com.coderstudios.simpleqr` | 1천+ |
| 펫포올 | `com.devnori.petforall` | 100+ |
| 메모라 | `com.coderstudios.memora` | 50+ |
| 쓱 가계부 | `com.coderstudios.cashmate` | 50+ |
| 읽어주는 앱 | `com.coderstudios.textreadingapp` | 50+ |
| 랜덤픽 | `com.kyungservice.randompick` | 10+ |
| 스톡메이트 | `com.coderstudios.stockmate` | 0+ |

스토어 링크 형식: `https://play.google.com/store/apps/details?id=<패키지명>`

## 커스텀 도메인

1. 루트에 `CNAME` 파일을 만들고 도메인만 한 줄 적습니다.
2. DNS에 A 레코드 4개(185.199.108~111.153)를 지정합니다.
3. `index.html` 의 `canonical` 과 `og:url` 주소도 새 도메인으로 바꿉니다.
