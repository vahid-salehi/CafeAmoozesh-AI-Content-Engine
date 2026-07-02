# 20 - GITHUB WORKFLOW

Version: 1.0

---

# هدف

این سند فرآیند استاندارد مدیریت Repository، نسخه‌بندی، Commit، Branch و Release را مشخص می‌کند.

هدف ایجاد یک روند قابل تکرار، شفاف و قابل نگهداری برای توسعه پروژه است.

---

# اصل طلایی

هر تغییر باید:

- قابل ردیابی (Traceable)
- مستندسازی شده
- دارای Commit مناسب
- دارای Version مشخص

باشد.

---

# ساختار Branchها

## main

نسخه پایدار پروژه.

فقط کدها و مستندات نهایی وارد این Branch می‌شوند.

---

## feature/*

برای توسعه قابلیت‌های جدید.

نمونه:

feature/semantic-seo

feature/master-prompt

feature/image-guide

---

## fix/*

برای رفع اشکال.

نمونه:

fix/readme

fix/html-standard

---

## docs/*

برای تغییر مستندات.

نمونه:

docs/update-seo

docs/review-checklist

---

# Workflow

ایجاد Branch

↓

اعمال تغییرات

↓

Review

↓

Commit

↓

Push

↓

Merge به main

↓

Release

---

# Commit Message Standard

Commitها باید کوتاه، واضح و انگلیسی باشند.

نمونه‌های مناسب:

```text
Add semantic SEO checklist

Update HTML standard

Improve image prompts

Fix README typo

Refactor article structure

Complete GitHub workflow
```

---

# مواردی که نباید در Commit نوشته شوند

✗ update

✗ fix

✗ changes

✗ test

✗ final

---

# Commit Frequency

Commitهای کوچک و مرتبط ایجاد شوند.

از Commitهای بسیار بزرگ خودداری شود.

---

# Push

پس از هر Commit پایدار:

```bash
git push
```

---

# Versioning

از Semantic Versioning استفاده شود.

فرمت:

MAJOR.MINOR.PATCH

نمونه:

1.0.0

1.1.0

1.2.3

2.0.0

---

# افزایش نسخه

## PATCH

رفع اشکال

نمونه:

1.0.0 → 1.0.1

---

## MINOR

افزودن قابلیت بدون شکستن سازگاری

نمونه:

1.0.0 → 1.1.0

---

## MAJOR

تغییرات ناسازگار

نمونه:

1.0.0 → 2.0.0

---

# Release

قبل از ایجاد Release بررسی شود:

☐ CHANGELOG به‌روز است.

☐ VERSION به‌روز است.

☐ README به‌روز است.

☐ مستندات کامل هستند.

☐ هیچ فایل ناقصی وجود ندارد.

---

# Pull Request Checklist

☐ هدف تغییر مشخص است.

☐ مستندات به‌روزرسانی شده‌اند.

☐ ساختار Repository حفظ شده است.

☐ فایل‌های اضافی حذف شده‌اند.

☐ نسخه در صورت نیاز افزایش یافته است.

---

# فایل‌های مهم Repository

README.md

CHANGELOG.md

VERSION

LICENSE

---

# فایل‌های ممنوع

این فایل‌ها نباید وارد Repository شوند:

- node_modules
- .DS_Store
- Thumbs.db
- *.log
- *.tmp
- *.bak

---

# .gitignore

وجود فایل `.gitignore` الزامی است.

حداقل شامل موارد زیر باشد:

```gitignore
node_modules/
*.log
*.tmp
*.bak
.DS_Store
Thumbs.db
```

---

# Backup

قبل از تغییرات بزرگ:

یک Tag یا Commit پایدار ایجاد شود.

---

# Release Tag

نمونه:

v1.0.0

v1.1.0

v2.0.0

---

# Review

قبل از Merge:

☐ فایل‌ها بررسی شوند.

☐ Markdown صحیح باشد.

☐ لینک‌ها بررسی شوند.

☐ ساختار پروژه حفظ شده باشد.

---

# Definition of Done

یک تغییر زمانی کامل محسوب می‌شود که:

✓ Commit شده باشد.

✓ Push شده باشد.

✓ مستند شده باشد.

✓ در CHANGELOG ثبت شده باشد.

✓ در صورت نیاز Version افزایش یافته باشد.

========================
END OF FILE
========================