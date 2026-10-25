# Detection Test Results

| Rule | Attack simulated (on the Windows VM) | Result |
|---|---|---|
| 100001 | Repeated failed logins with a fake user (net use) | Fired, built on Wazuh rule 60204 |
| 100002 | net user (name) (password) /add | Fired |
| 100003 | powershell -enc (base64 command) | Fired, needs Sysmon |
| 100004 | net localgroup administrators (name) /add | Fired |

## Notes
- All tests were run in an isolated lab VM.
- Test accounts were deleted afterwards with net user (name) /delete.
- Screenshots of each alert are in the screenshots folder.
