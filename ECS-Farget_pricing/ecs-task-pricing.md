# ECS Task Cost Calculation

## EC2 Launch Type

For the EC2 launch type, the main cost is the EC2 instance itself. Assuming you use an instance type like `t3.large` which has 2 vCPUs and 8 GB of memory:

- **t3.large in US East (N. Virginia)**:
  - On-Demand price: ~$0.0832 per hour

### Monthly Cost Calculation

\[ \text{Monthly cost} = \text{Hourly price} \times 24 \text{ hours/day} \times 30 \text{ days/month} \]

\[ \text{Monthly cost} = \$0.0832 \times 24 \times 30 \approx \$59.90 \]

## Fargate Launch Type

For the Fargate launch type, you pay for vCPU and memory resources used by your containerized applications:

- **vCPU**: $0.04048 per vCPU per hour
- **Memory**: $0.004445 per GB per hour

### Monthly Cost Calculation

For 2 vCPUs and 8 GB memory:

\[ \text{vCPU cost} = 2 \times \$0.04048 = \$0.08096 \]
\[ \text{Memory cost} = 8 \times \$0.004445 = \$0.03556 \]
\[ \text{Total hourly cost} = \$0.08096 + \$0.03556 = \$0.11652 \]
\[ \text{Monthly cost} = \$0.11652 \times 24 \times 30 \approx \$84.70 \]

## Summary

- **EC2 Launch Type**: 
  - Estimated monthly cost for `t3.large`: **$59.90**
- **Fargate Launch Type**: 
  - Estimated monthly cost: **$84.70**

