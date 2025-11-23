# Lab 2: Create a Scheduled Alert in Splunk

## 🎯 Goal
Practice building a scheduled search alert that triggers when a condition is met.

---

### 1. SPL for the alert
Detect if errors exceed a threshold:

```spl
index=_internal log_level=ERROR
| stats count as error_count
```

### 2. Alert condition

Trigger alert when:

``` error_count > 100 ```

### 📝 What I learned

- How to configure alert frequency
- How to add trigger conditions
- How Splunk sends alert notifications

