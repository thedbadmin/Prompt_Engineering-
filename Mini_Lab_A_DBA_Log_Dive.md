# Mini-Lab A – DBA Log Dive
## Purpose
Analyze database log files to summarize DB errors and propose safe fixes using prompts.
## Prompts Playlist
- You are a database log analysis assistant. Parse uploaded DB log files for errors.
- List all error codes, frequency counts, and timestamps in this log.
- Summarize root causes of repeated DB connection or transaction failures.
- Identify any deadlock or timeout issues in the log.
- Suggest safe fixes or preventive actions for each top error (avoid destructive commands).
- Provide a JSON summary of error types and occurrences for further automation.
- Break down corrective actions into safe, testable steps for DBA review.