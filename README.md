# python_automation_suite
A collection of scripts designed to automate common system administration, security, and cloud management tasks. The project focuses on reliability, reusability, and real-world automation scenarios encountered in IT, DevOps, and Cybersecurity roles.

## Why this project matters
Automation reduces human error, save operational time, and improves system consistency. This suite demonstrates how Python can be leveraged to:
- Automate repetitive administrative tasks
- Improve cloud hygeine
- Support security best practices

## Automation Modules
- Log rotation and cleanup
- Backup verification
- API health monitoring
- User acocunt audits
- Cloud resoource checks (AWS)

## Tech Stack
- Python
- argparse
- requests
- boto3
- JSON/CSV reporting

## Design Approach
- Modular scripts for independent execution
- Config-driven execution
- Clear logging and error handling
- Idempotent tasks

## Cloud Integration
- AWS IAM audits
- S3 backup validation
- EC2 resource health checks

## Output
- Console status reports
- Optional CSV logs
- Exit codes suitable for CI/CD pipelines

## Security Considerations
- No hardcoded credentials
- Environment variable-based secrets
- Principle of least-privilege for cloud access

## Future Improvements
- Unified CLI wrapper
- Scheduling integration
- Slack/email alerting
- Expanded cloud provider support

## Example Use Case

```bash
python check_api_health.py --endpoint https://api.example.com



Author
JamesP

