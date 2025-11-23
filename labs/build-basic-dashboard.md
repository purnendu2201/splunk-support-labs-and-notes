# Lab 1: Build a Basic Splunk Dashboard

## 🎯 Goal
Learn how to create a simple Splunk dashboard with:
- A timechart  
- A single-value panel  
- A table  

---

### 1. SPL for timechart panel

```spl
index=_internal sourcetype=splunkd
| timechart span=5m count
```

### 2. SPL for single value

```spl
index=_internal sourcetype=splunkd
| stats count as total_events
```

### 3. SPL for table panel

```spl
index=_internal sourcetype=splunkd
| stats count by component
```

## 📝 What I learned

- How to add panels
- How to use SPL to build visualizations
- How to connect searches to dashboard components

