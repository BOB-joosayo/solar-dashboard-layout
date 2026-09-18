# 태양광 분석 리포트 HTML Mock (A4) · 다현장

**GitHub:** https://github.com/BOB-joosayo/solar-report-html  
**바로 보기 (Pages):** https://bob-joosayo.github.io/solar-report-html/

Cloud EMS **태양광 빌딩** 공통 일·월·연 리포트 화면 Mock입니다.
숫자·빌딩명은 샘플(`[덕우전자]태양광발전설비`)이며, 설계는 현장별 유동(인버터 N·PV·용량).

## 바로 보기 (권장)

| 파일 | 내용 |
|------|------|
| [index.html](index.html) | 목록 |
| [daily.html](daily.html) | 일간 3p |
| [monthly.html](monthly.html) | 월간 3p |
| [yearly.html](yearly.html) | 연간 2p |

## 왜 HTML만 받으면 “깨져” 보이나?

1. **예전 버전**은 스타일이 `report.css` **별도 파일**이었습니다. HTML만 메일/메신저로 보내면 CSS가 없어 **레이아웃·색·차트가 전부 깨집니다.**
2. HTML·CSS를 다른 폴더에 나눠 두거나, 압축 해제 후 `daily.html`만 다른 곳으로 옮긴 경우도 동일합니다.
3. Outlook 등에서 “첨부 HTML 미리보기”는 CSS/로컬 파일을 막는 경우가 많아 깨져 보입니다.

## 안 깨지게 보는 방법

### 개발자 / 리뷰
- **이 Git 저장소** 링크 또는 Pages URL을 전달한다 (HTML 파일만 보내지 말 것).
- clone / zip 후 `index.html`을 연다.
- `daily.html` / `monthly.html` / `yearly.html`은 **CSS 내장(self-contained)** 이라 파일 하나만 열어도 스타일이 유지된다.
- `report.css`는 스타일 원본. HTML에 다시 넣으려면 `PythonWork/solar_report_design/embed_css_self_contained.py` 실행.

### 고객에게 줄 때 (운영 방향)
- **권장:** 서버에서 생성한 **PDF** 또는 EMS 포털 안 리포트 화면.
- HTML로 줄 경우: **self-contained HTML 1파일** 또는 **폴더 전체(zip)** / **HTTPS URL**. HTML만 메신저 첨부로 보내지 말 것.
- 인쇄: 브라우저 `Ctrl+P` → PDF 저장 · 용지 A4 · **배경 그래픽 켜기**.

## 설계 문서 (로컬)
- `Rwork/docs/solar_report_design_handoff.md`
- `Rwork/docs/solar_report_ai_build_spec.md`
- PPT v1.9 (Desktop 태양광 리포트 설계서)
