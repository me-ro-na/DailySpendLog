# 📘 DailySpendLog
**Java로 작성된 Notion 소비 기록 자동화 라이브러리**

> 사용자의 소비 내역을 날짜 기반으로 자동 분류하고, Notion 데이터베이스에 기록하여
> 주별/월별/연도별 소비를 자동 집계하고 시각화할 수 있게 해줍니다.

---

## ✨ 주요 기능
- 🧾 소비 항목을 Java 코드 또는 웹 입력을 통해 기록
- 📅 날짜 기반 `연도`, `월`, `주차` 정보 자동 추출
- 🔗 Notion API 연동 – 소비 항목 자동 삽입
- 🗃 Weekly/Monthly/Yearly DB 존재 여부 확인 후 자동 생성
- 📊 Notion Rollup을 활용한 소비 금액 자동 집계
- 🛠 간단한 설정으로 누구나 나만의 자동 가계부 생성 가능

---

## ✅ 왜 만들었나요?
- 매일매일 가계부를 수동으로 템플릿에 맞춰 작성하는 것이 귀찮았고,
- Java 개발자로서 이 과정을 자동화할 수 있다고 생각했습니다.
- Notion의 강력한 시각화 기능을 살리면서,
  소비 입력은 최대한 간편하게 할 수 있는 시스템을 만들고자 했습니다.

---

## 🧱 시스템 구조
```
🖥 사용자 입력 (웹 or CLI)
   ↓
⚙️ Java 라이브러리 처리
   ├─ 소비 항목 / 금액 파싱
   ├─ 날짜 기반 메타데이터 생성
   │   ├─ 연도 (예: 2025)
   │   ├─ 월 (예: 2025-06)
   │   └─ 주차 (예: 25)
   └─ Notion DB 존재 여부 확인 및 자동 생성
        ↓
📝 Notion DB - Spending Items
   ├─ 항목명
   ├─ 금액
   ├─ 날짜
   ├─ 연도 / 월 / 주차
   └─ 관계 필드 (Weekly / Monthly / Yearly 연결)
        ↓
📊 Rollup 집계 (Notion 기능)
   ├─ Weekly Spending DB: 주차별 소비 총합
   ├─ Monthly Spending DB: 월별 소비 총합
   └─ Yearly Spending DB: 연도별 소비 총합
```

---

## ⚙️ 사용 방법

- 추후 작성

---

## 📂 Notion DB 구조
- Spending Items: 소비 항목 기본 기록
- Weekly Spending: 주차 단위 요약 (관계 필드: 주차 + 연도)
- Monthly Spending: 월 단위 요약 (관계 필드: 월)
- Yearly Spending: 연도 단위 요약 (관계 필드: 연도)

---

## 📄 라이선스

MIT License
자유롭게 수정/사용/배포 가능하며, 상업적 사용도 허용됩니다.

