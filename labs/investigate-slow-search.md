# Lab 3: Investigating a Slow Search

## 🎯 Goal
Understand why searches become slow and how to improve them.

---

### Example Slow SPL
```spl
index=_internal
| lookup big_lookup.csv host OUTPUT field1
| stats count by host, field1
| sort - count
```

## 🔍 Investigation Steps

- Check if the time range is too large
- Validate lookup file size
- Apply filters early (```index```, ```sourcetype```, ``host``)
- Replace ``stats + sort`` with ``top`` (if applicable)
- Use ``tstats`` if data is accelerated

## ✔ Improved SPL
```spl
| tstats count WHERE index=_internal BY host
```
## 📝 What I learned

- How search optimization works
- Why filters should be applied early
- Lookup performance tips
- When to use tstats
