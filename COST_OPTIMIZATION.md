# Cloud Cost Management

## Monthly Cost Breakdown
```mermaid
pie
    title Estimated Monthly Costs
    “RDS (db.t3.micro)” : 45
    “NAT Gateway” : 30
    “Data Transfer” : 15
    “KMS Encryption” : 10
```

## Optimization Strategies
| **Resource**      | **Current Cost** | **Optimized Cost** | **Method** |
|-------------------|------------------|--------------------|------------|
| RDS Instance      | $45.00           | $31.50 (-30%)      | Reserved Instance (1yr) |
| NAT Gateway       | $32.40           | $16.20 (-50%)      | Shared across VPCs |
| Data Transfer     | $15.00           | $7.50 (-50%)       | VPC Endpoints |
| **Total**         | **$92.40**       | **$55.20**         | |

## Cost Monitoring Setup
```bash
# Create budget alert
aws budgets create-budget \
  --account-id <YOUR_ACCOUNT> \
  --budget file://budget.json \
  --notifications-with-subscribers file://notifications.json
```

[Sample budget.json](./budget.json)
