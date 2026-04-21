# Morning Market Panel 운영 메모

- 목표: 무료 데이터 기반 모바일 PWA
- 업데이트 기준: 매일 07:00, 15:00
- 권장 구조:
  1. 서버 스케줄러(cron / GitHub Actions / Cloudflare Workers Cron)
  2. Alpha Vantage 등 무료 API 호출
  3. 최신 스냅샷 JSON 생성
  4. PWA는 열릴 때 최신 JSON 표시

- 포함된 핵심 섹션:
  - 블룸버그TV 참고용 핵심 종합 분석
  - 꼭 알아야 하는 지수 변화 심층 분석
  - 세부 지수별 정의 리스트

- 중요한 제약:
  - PWA는 iPhone 등에서 백그라운드 정시 실행이 제한됨
  - 따라서 07:00/15:00 자동 갱신은 앱이 아니라 서버 스케줄러가 담당해야 함
