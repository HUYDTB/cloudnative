# cloudnative

Practical guidance for running cloud operations smoothly, securely, and professionally.

## 1) Build a professional operating model

- Define clear ownership with a simple **RACI** (who is Responsible, Accountable, Consulted, Informed).
- Separate environments: **dev / staging / production**.
- Use **Infrastructure as Code** (Terraform, Pulumi, CloudFormation) for repeatable changes.
- Require change control for production (pull request review + approval).

## 2) Security baseline (must-have)

- Enforce **least privilege IAM** for users, services, and CI/CD.
- Enable **MFA** and SSO for all human access.
- Keep secrets in a secure manager (never hardcode in source control).
- Encrypt data **in transit** (TLS) and **at rest** (KMS-managed keys).
- Turn on centralized logs and audit trails (CloudTrail / Activity Logs / Audit Logs).
- Patch images and dependencies regularly; block known vulnerable versions.

## 3) Reliable operations

- Set **SLO/SLI** targets (availability, latency, error rate).
- Monitor golden signals: latency, traffic, errors, saturation.
- Create actionable alerts (page only when action is required).
- Use runbooks for common incidents (service down, high latency, cert expiry, data store pressure).
- Perform regular backup and restore tests (do not only “take backups”—verify restore).

## 4) Safe deployment practices

- Automate CI/CD with tests, security checks, and policy checks.
- Use progressive rollouts (blue/green, canary) with fast rollback.
- Tag every deployment with version, owner, and change ticket.
- Block direct manual changes in production when possible.

## 5) Incident and risk management

- Define incident severity levels and response SLAs.
- Maintain an on-call rotation with clear escalation paths.
- Run post-incident reviews focused on learning (not blame).
- Track recurring risks in a risk register and prioritize remediation.

## 6) Weekly cloud operations checklist

- [ ] Review security alerts and unresolved vulnerabilities  
- [ ] Review IAM drift / excessive permissions  
- [ ] Validate backup restore sample  
- [ ] Review error budget burn and top incidents  
- [ ] Confirm cost anomalies and unused resources  

This repository can be used as a starting point for cloud-native operations practices and team standards.
