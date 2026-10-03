# AlienNews Skills | ספריית הסקילים של AlienNews

A small, growing collection of advisory AI-agent workflows for [AlienNews](https://aliennews.co.il).

ספרייה קטנה ומתפתחת של הנחיות עבודה לסוכני AI, עבור [AlienNews](https://aliennews.co.il).

## Catalog | הסקילים

- [Preserve Owner Intent](skills/preserve-owner-intent/SKILL.md): Preserve the user's latest authorized goal and constraints when changing approach. Respect changed instructions and explicit cancellation.
  - שמירה על המטרה והאילוצים העדכניים של המשתמש גם כשצריך לשנות את דרך הביצוע, תוך כיבוד שינוי הנחיות וביטול מפורש.
- [Feedback to Fix](skills/feedback-to-fix/SKILL.md): Turn feedback into focused repairs and check the actual result.
  - הפיכת משוב לתיקון ממוקד ובדיקת התוצאה בפועל.

## Use | שימוש

Read the relevant SKILL.md before using it. Each folder under skills/ is a self-contained skill with optional agent interface metadata in agents/openai.yaml. Import or copy the chosen folder using your assistant's supported skill installation workflow. Support and invocation syntax depend on the host application.

קראו את קובץ SKILL.md של הסקיל לפני השימוש. כל תיקייה תחת skills/ היא סקיל עצמאי, עם פרטי ממשק אופציונליים ב־agents/openai.yaml. ייבאו או העתיקו את התיקייה הרצויה באמצעות תהליך התקנת הסקילים שהעוזר שלכם תומך בו. התמיכה ודרך ההפעלה תלויות ביישום.

Example prompts for assistants that support named skills:

- Use $preserve-owner-intent to continue this task while preserving my latest goals and constraints.
- Use $feedback-to-fix to revise this draft based on my feedback, then check that the stated requirements are satisfied.

דוגמאות לבקשות:

- השתמש ב־$preserve-owner-intent כדי להמשיך במשימה תוך שמירה על המטרות והאילוצים העדכניים שלי.
- השתמש ב־$feedback-to-fix כדי לתקן את הטיוטה לפי המשוב שלי, ואז בדוק שהיא עומדת בדרישות שציינתי.

## Limits and safety | מגבלות ובטיחות

These are text-based workflow aids, not executable integrations, security controls, or guarantees of correct behavior. They do not grant permissions or override higher-priority instructions, safety rules, or user approvals. Review outputs and use only the minimum permissions needed for a task.

These files require no credentials, API keys, or account connections. This repository contains only the two public skills and this README. Do not add private conversations, personal records, credentials, or production configuration when contributing examples. Use fictional examples instead.

אלו הנחיות עבודה טקסטואליות, ללא חיבורים פעילים לשירותים. הן אינן מנגנון אבטחה ואינן מבטיחות התנהגות תקינה. הן אינן מעניקות הרשאות ואינן גוברות על הנחיות בעדיפות גבוהה יותר, כללי בטיחות או אישורי המשתמש. בדקו את התוצרים והעניקו רק את ההרשאות הנחוצות למשימה.

הקבצים אינם דורשים סיסמאות, מפתחות API או חיבור לחשבונות. המאגר מכיל רק את שני הסקילים הציבוריים ואת קובץ ההסבר הזה. אין להוסיף לדוגמאות שיחות פרטיות, מידע אישי, פרטי התחברות או הגדרות סביבת ייצור. השתמשו בדוגמאות בדויות.

## Credit | קרדיט

Created by בן, an OpenAI-powered AI assistant, at Avi Moas's request. Original workflow content; not an official OpenAI product or endorsement.

נוצר על ידי בן, עוזר AI המופעל באמצעות OpenAI, לבקשת אבי מואס (Avi Moas). תוכן עבודה מקורי; אינו מוצר רשמי של OpenAI ואינו מעיד על אישור או חסות מטעמה.
