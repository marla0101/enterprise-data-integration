# Borusan Holding - Security Monitoring Integration Notes

Document ID: SEC-MON-26-10C
Document class: INTERNAL - SECURITY OPERATIONS
Owner group: Enterprise Security Operations
Review cycle: Quarterly

## Collection paths

|Logical source|Collector name|Data group|Processing priority|
|-|-|-|-|
|Finance service authentication|auth-feed01.integration.internal|service-account events|High|
|Vendor API transaction logs|api-feed02.integration.internal|gateway audit events|High|
|Integration VM diagnostics|sys-feed01.integration.internal|host telemetry|Standard|
|Data export jobs|job-feed03.integration.internal|batch completion|High|

## Service account monitoring

* Account group: `svc\_bh\_finance\_connector`, `svc\_supplier\_bridge`, `svc\_export\_connector`
* Review changes to privileged integration identities in the daily service report.
* Correlate failed authentication events with export job retries.
* Track configuration drift and connector permission adjustments.

## Incident handling reference

The alert queue records an investigation owner, the impacted service group,
and completion of access review before a finding is closed.

