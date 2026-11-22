# Python Automation Suite

**Practical Python automation for IT operations, system administration, cybersecurity, and cloud infrastructure.**

Python Automation Suite is a collection of modular Python scripts designed to automate repetitive administrative tasks, monitor infrastructure, validate backups, and support security operations.

The project emphasizes reliability, maintainability, security, and practical automation scenarios commonly encountered in IT Support, DevOps, Cloud Engineering, and Cybersecurity environments.

## Project Objectives

The purpose of this repository is to demonstrate how Python can be used to solve real-world technical challenges while reducing manual intervention.

Key objectives include:

- **Operational Efficiency:** Reduce time spent on repetitive IT administration tasks.
- **System Reliability:** Improve consistency through automated monitoring and validation.
- **Security:** Identify potential risks associated with user accounts, permissions, and cloud resources.
- **Cloud Management:** Support routine auditing and monitoring of AWS infrastructure.
- **Reusability:** Develop modular scripts that can be adapted to different environments.
- **Reporting:** Generate actionable outputs for administrators and technical teams.

## Automation Modules

The suite is organized around several independent automation capabilities.

| Module | Description |
|---|---|
| Log Rotation & Cleanup | Identify, archive, and remove outdated log files according to configurable retention policies. |
| Backup Verification | Validate backup availability, file integrity, and expected backup schedules. |
| API Health Monitoring | Check API availability, response codes, latency, and connection errors. |
| User Account Auditing | Review account information, permissions, and potential security concerns. |
| AWS IAM Auditing | Identify inactive users, outdated access keys, and permission-related risks. |
| AWS S3 Validation | Verify expected backup objects and inspect configured bucket security settings. |
| AWS EC2 Monitoring | Review instance states and relevant infrastructure health indicators. |

*Module descriptions represent the intended functionality. Implementation status should be documented as development progresses.*

## Technology Stack

**Programming Language**
- Python 3.11+

**Libraries and Tools**
- `argparse` — Command-line argument processing
- `requests` — HTTP requests and API monitoring
- `boto3` — AWS service integration
- `logging` — Structured application logging
- `pathlib` — Filesystem operations
- `json` / `csv` — Configuration and reporting
- `hashlib` — File integrity verification
- `unittest` or `pytest` — Automated testing

**Cloud Platform**
- Amazon Web Services (AWS)

**Development Tools**
- Git and GitHub
- Python virtual environments
- GitHub Actions (planned)

## Getting Started

### Prerequisites

- Python 3.11 or newer
- Git
- AWS credentials configured for AWS-related modules
- Network access for API monitoring

### Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/python_automation_suite.git
cd python_automation_suite
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the environment:

macOS/Linux:

```bash
source .venv/bin/activate
```

Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

*Installation commands assume the corresponding files and dependencies have been added to the repository.*

## Example Usage

### API Health Monitoring

Check whether an API endpoint is responding:

```bash
python check_api_health.py --endpoint https://api.example.com
```

**Illustrative console output:**

```text
[INFO] Starting API health check
[INFO] Endpoint: https://api.example.com
[INFO] HTTP Status: 200
[INFO] Response Time: 142 ms
[PASS] API endpoint is operational
```

Additional monitoring capabilities may include configurable timeouts, response validation, and reporting.

### Backup Verification

Example of validating an expected backup:

```bash
python verify_backup.py --path ./backups
```

The module is intended to inspect backup files, validate expected availability, and report issues requiring attention.

### AWS Resource Monitoring

Example of checking EC2 instance health:

```bash
python check_ec2.py --region us-east-1
```

The module is intended to retrieve instance status information using AWS APIs and report relevant operational findings.

*These examples illustrate the intended command-line interfaces and are not verified execution results.*

## Design Principles

**1. Modular Architecture**

Each automation module should operate independently, allowing administrators to execute only the functionality they need.

**2. Configuration-Driven Execution**

Scripts should accept command-line arguments or external configuration files rather than requiring modifications to source code.

**3. Error Handling**

Expected failures, including network timeouts, missing files, and AWS authorization errors, should be handled gracefully and logged appropriately.

**4. Idempotency**

Where applicable, repeated execution should avoid unintended duplicate changes or destructive operations.

**5. Observability**

Automation should produce meaningful logs, structured reports, and status indicators.

**6. Safe Execution**

Potentially destructive operations should support validation, dry-run execution, and clearly defined operational limits.

## Reporting and Exit Codes

Modules should support consistent output formats for operational visibility and integration with other systems.

Planned reporting capabilities include:

- Human-readable console output
- Structured JSON reports
- CSV exports
- Timestamped execution logs
- Nonzero exit codes for operational failures

Suggested exit code conventions:

| Exit Code | Meaning |
|---|---|
| `0` | Execution completed successfully |
| `1` | Operational check failed |
| `2` | Invalid arguments or configuration |
| `3` | Authentication or authorization failure |
| `4` | Network or service connectivity failure |

## Security Considerations

Security is a core design requirement of the project.

- Never hardcode credentials, API keys, or access tokens.
- Use environment variables, AWS profiles, or IAM roles for authentication.
- Apply the principle of least privilege to cloud permissions.
- Avoid writing secrets or sensitive account information to logs.
- Validate user-supplied file paths and configuration parameters.
- Use timeouts for network requests.
- Require explicit confirmation before destructive operations where appropriate.
- Exclude local secrets and credential files from version control.

## Project Roadmap

### Phase 1 — Core Automation

- [ ] Implement API health monitoring
- [ ] Implement log rotation and cleanup
- [ ] Implement local backup verification
- [ ] Establish consistent logging and exit codes
- [ ] Add automated tests

### Phase 2 — Security and Cloud Integration

- [ ] Implement user account auditing
- [ ] Integrate AWS IAM security checks
- [ ] Implement S3 backup validation
- [ ] Implement EC2 monitoring
- [ ] Add JSON and CSV reporting

### Phase 3 — Advanced Automation

- [ ] Develop a unified command-line interface
- [ ] Add scheduling support
- [ ] Integrate email or Slack notifications
- [ ] Introduce GitHub Actions testing
- [ ] Add configurable dry-run functionality
- [ ] Expand support to additional cloud platforms

## Practical Applications

Python Automation Suite is designed around operational scenarios such as:

**IT Support:** Automating account reviews, collecting diagnostic information, and reducing repetitive administrative work.

**Systems Administration:** Managing log retention, monitoring service availability, and validating backup processes.

**Cybersecurity:** Reviewing inactive accounts, identifying configuration risks, and supporting routine security audits.

**Cloud Operations:** Monitoring AWS resources, validating cloud backups, and improving infrastructure visibility.

## Project Status

**Development / Portfolio Project**

This repository is intended to evolve through incremental development, testing, and documentation. Features should be marked complete only after implementation and validation.

## Author

**[JamesP]**

Python Automation | IT Operations | Cloud Infrastructure | Cybersecurity

## License

License information to be added.
