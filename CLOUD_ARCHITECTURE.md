## Service Models
- React Frontend → PaaS (Vercel)
- Express API    → PaaS (Railway)
- Background Jobs → FaaS (AWS Lambda)

## Network Design
VPC: 10.0.0.0/16
├── Public Subnet  (10.0.1.0/24) → Load Balancer
└── Private Subnet (10.0.2.0/24) → API Server

## High Availability
- Deployed across AZ-1 and AZ-2
- Load Balancer uses /api/health for health checks
- Stateless API → easy to scale horizontally

## Cost Model
- API (24/7)        → Reserved  (~40% savings)
- Traffic spikes    → On-Demand
- Background jobs   → Spot
