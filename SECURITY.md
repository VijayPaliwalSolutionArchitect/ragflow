# Security Policy

## Supported Versions

This fork tracks a single pinned upstream commit and is supported on that baseline only.

| Version | Supported          |
|---------|--------------------|
| `313ca90f` (pinned fork baseline) | :white_check_mark: |
| Later upstream releases | :x: not tracked |

Security fixes land as deliberate fork updates, not as ad-hoc cherry-picks. If you depend on this fork in production, subscribe to this repository's releases and watch for fork-baseline updates.

## Reporting a Vulnerability

### Private, named, time-bound reporting

**Do not file public issues for vulnerability reports.** GitHub Issues is not a secure channel and is monitored only for feature and bug reports. Instead, email **MD@ShivamITConsultancy.com** with:

- A clear description of the issue and its impact.
- Steps to reproduce (proof-of-concept or minimal repro is ideal).
- Affected versions and environments.
- Your preferred contact method and a deadline for acknowledgment.

We will acknowledge receipt within **2 business days** and aim to provide an initial assessment within **5 business days**.

### Severity and response timelines

| Severity | Criteria | Target response | Target fix |
|----------|----------|-----------------|------------|
| Critical | Remote code execution, data exfiltration, tenant-isolation bypass | 24 hours | 7 days |
| High | Privilege escalation, authentication bypass, arbitrary file read | 48 hours | 30 days |
| Medium | Information disclosure, denial of service, non-trivial config weakness | 5 business days | 90 days |
| Low | Cosmetic, hardening suggestions, documentation gaps | Next fork baseline | Next fork baseline |

### Coordinated disclosure

We practice coordinated vulnerability disclosure. If you report in good faith, we will not pursue legal action and will credit you by name (or anonymously, your choice) in the advisory that accompanies the fix. We ask that you:

- Hold the vulnerability privately until we confirm a fix is in progress.
- Notify us before disclosing publicly so we can coordinate timing.

## Security posture

This fork inherits the upstream security design unchanged. What follows is what a reviewer should know about the fork's specific posture.

- **No upstream code is modified.** The fork is a pinned-source intake: the security surface is exactly the upstream baseline at `313ca90f`, and any vulnerability in that baseline is an upstream vulnerability, not a fork-introduced one.
- **No dedicated security team.** SHIVAM ITCS is a consultancy, not a vendor with a Security Operations Centre. The contact above is the only reporting path, and response is best-effort against the timelines in this policy.
- **Local-first AI data residency.** The fork's retrieval and generation pipeline is designed for local deployment; no user documents or query content are transmitted to third-party services as part of the default operation.
- **Upstream-source vulnerabilities belong upstream.** If you discover a vulnerability that exists in the upstream codebase, the most effective path is to report it through [infiniflow/ragflow](https://github.com/infiniflow/ragflow)'s own security policy. We will not act on reports about code we have not modified, but we will route valid reports to upstream maintainers where we can.

## What this fork is not

- Not affiliated with InfiniFlow or the upstream ragflow project.
- Not a product with a dedicated security team or SLA-backed vulnerability response.
- Not a redistribution or commercial offering of the upstream work.
- Not claiming any authorship over the upstream codebase.

If you need guaranteed response times, a named security team, or a formal security program, this fork does not provide them. Evaluate the upstream project or a commercial distribution for those requirements.