---
tags: daily_note
---
# Daily Log
This shows the files created or modified today.

```dataview
table file.ctime as Created, file.mtime as Modified
where file.cday = date({{date}}) or file.mday = date({{date}})
sort file.ctime asc

```

# Fleeting Notes
- [x] notes