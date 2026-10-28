# AuctionRaffle.Automation 🎯

חבילת בדיקות אוטומציה מקיפה לקצה-לקוח (E2E Automation Test Suite) עבור מערכת המכירה הסינית (**AuctionRaffle**). הפרויקט מפותח בטכנולוגיות C#, NUnit, ו-**Playwright for .NET**, תוך שימוש בתבנית העיצוב המתקדמת **Page Object Model (POM)** להבטחת תחזוקת קוד נקייה, מודולרית ויעילה.

---

## 🏗️ ארכיטקטורת הפרויקט ומבנה התיקיות (Project Architecture & POM)

המאגר מנוהל כפרויקט נפרד ועצמאי לחלוטין מקוד המקור של המערכת, כדי לאפשר סביבת בדיקות קלה וגמישה.

```text
AuctionRaffle.Automation/
│
├── Pages/             # מחלקות Page Object Model - מיפוי רכיבי UI ולוגיקת עמודים
│   ├── LoginPage.cs   # מיפוי שדות התחברות, סיסמה וכפתור כניסה באמצעות Playwright
│   └── RafflePage.cs  # מיפוי כרטיסי הגרלה, הוספה לעגלה וניהול סל הקניות
│
├── Tests/             # תרחישי בדיקה (NUnit Test Scenarios & Assertions)
│   └── RaffleWorkflowTests.cs # תרחישי E2E מלאים (התחברות וביצוע פעולות במערכת)
│
└── Utilities/         # מחלקות עזר, נתוני בדיקה גנריים, והפקת דוחות
