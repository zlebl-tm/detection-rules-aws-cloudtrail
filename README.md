# Scanner Detection Rules - AWS CloudTrail

This repository contains Scanner detection rules for AWS CloudTrail logs.

To give you a flavor of the kind of detection rules in this repository, here
are a few examples:
- **Potential Bucket Enumeration on AWS**
- **AWS RDS Master Password Change**
- **Restore Public AWS RDS Instance**
- **AWS GuardDuty Important Change**

When these detection rules are triggered, alerts are sent to the [event sinks](https://docs.scanner.dev/scanner/using-scanner/detection-rules/event-sinks)
in Scanner that are associated with these keys:
- `informational_severity_alerts`
- `low_severity_alerts`
- `medium_severity_alerts`
- `high_severity_alerts`
- `critical_severity_alerts`
- `fatal_severity_alerts`

To deploy these rules into your Scanner instance, you can follow the
instructions in the [Scanner documentation](https://docs.scanner.dev) under
**Detection Rules as Code**. Your Scanner instance will sync with the `main`
branch of this repository, keeping your detections up-to-date.
