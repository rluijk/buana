---
tags: daily_note
---
# Daily Log
This shows the files created or modified today.

```dataview
table file.ctime as Created, file.mtime as Modified
where file.cday = date(2022-04-07) or file.mday = date(2022-04-07)
sort file.ctime asc

```

# Fleeting Notes
- [ ] Today is the day that I started to use Zettelkasten