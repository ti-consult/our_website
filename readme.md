# Tactic Intel Website

Professional database performance consulting website for European and UK markets.

## Project Overview

**Business:** Database performance consulting specialist serving growing European companies  
**Target Market:** CTOs and Tech Leads experiencing database scaling challenges  
**Positioning:** Multi-platform database expertise with systematic optimization methodologies  

## Technical Stack

- **Frontend:** Pure HTML5/CSS3/JavaScript (no frameworks)
- **Hosting:** AWS CloudFront + S3 (Swiss hosting for security positioning)
- **Domain:** tacticintel.com
- **SSL:** AWS Certificate Manager
- **Email:** ashley@tacticintel.com

## Services & Pricing

| Service | Price (EUR/GBP) | Timeline |
|---------|-----------------|----------|
| Database Health Check | €600 / £500 | 2 hours |
| Database Performance Analysis | €1,800 / £1,500 | 1 week |
| AI-Enhanced Infrastructure Assessment | €2,200 / £1,800 | 2 weeks |
| Query Optimisation Package | €1,500 / £1,200 | 3-5 days |
| Database Emergency Response | €2,400 / £2,000 | 24-48 hours |
| Database Architecture Review | €2,600 / £2,200 | 2-3 weeks |
| Monthly Performance Monitoring | €300 / £250 | Ongoing |

## File Structure

```
├── index.html          # Main website file
├── README.md           # This file
└── deployment/         # AWS deployment files (if using Terraform)
```

## Key Features

- **Responsive Design:** Works on desktop, tablet, mobile
- **Professional Branding:** Tactic Intel letterhead styling
- **Service Progression:** Clear pricing ladder from €600 to €2,600
- **Contact Integration:** Direct mailto links with pre-filled subjects
- **Swiss Security Positioning:** Subtle professional security credibility
- **Market Positioning:** Euro-first pricing for European market focus

## Deployment

### Manual S3 Upload
```bash
aws s3 cp index.html s3://your-bucket-name/
aws cloudfront create-invalidation --distribution-id YOUR_ID --paths "/*"
```

### CloudFront Setup Required
- S3 bucket with static website hosting
- CloudFront distribution for CDN and custom domain
- Route53 DNS management
- SSL certificate from ACM

## Content Strategy

**Problem Scenarios:** Realistic database performance challenges without fabricated case studies  
**Pricing Validation:** Based on UK database consultant market research (£445-450/day contractor rates)  
**Service Differentiation:** AI-enhanced systematic methodology vs traditional ad-hoc consulting  
**Target Personas:** Growing SaaS, Fintech, E-commerce companies experiencing scaling issues  

## Business Context

**Strategic Purpose:** Market validation for database consulting services before full business launch  
**Geographic Focus:** UK and European markets (340M+ addressable market vs 67M UK-only)  
**Technology Coverage:** PostgreSQL, MySQL, SQL Server, Oracle, MongoDB, Redis, Elasticsearch  
**Revenue Model:** Project-based services with recurring monitoring opportunities  

## Development Notes

### Character Encoding
- **Critical:** Always save files as UTF-8 to prevent currency symbol corruption
- VS Code: Bottom-right corner → encoding → "Save with Encoding" → "UTF-8"
- Corrupted characters break mailto functionality and display

### Button Functionality  
- Contact buttons use `mailto:` links requiring configured email client
- Pre-filled subject: "Free Database Performance Assessment"
- Fallback: Display email address for manual copying if mailto fails

### Cache Management
- CloudFront invalidation required after content updates
- Command: `aws cloudfront create-invalidation --distribution-id YOUR_ID --paths "/*"`
- Browser cache: Use Ctrl+Shift+R for hard refresh during testing

## Security Configuration

### S3 Bucket Settings
- **Keep "Block all public access" ENABLED**
- CloudFront uses Origin Access Control (OAC) for secure access
- Bucket remains private while CloudFront serves content publicly

### Swiss Hosting Positioning
- AWS Zurich region deployment for genuine Swiss hosting claims
- GDPR+ compliance through Swiss data protection standards
- Professional security differentiation without heavy-handed marketing

## Market Validation Metrics

**Pricing Benchmarks:**
- UK PostgreSQL DBA contractors: £445/day (£56/hour)
- UK database consultants: $65/hour average (£52/hour)
- London data consulting: £2,000-£30,000 project range
- Competitor monitoring: £250-300/month (matches our €300/£250)

**Service Positioning:**
- Entry point: €600 health check removes friction
- Premium services: €2,200-2,600 for comprehensive engagements
- Recurring revenue: €300/month monitoring at market rates
- Emergency response: €2,400 justified by 24-48 hour SLA

## Known Issues & Troubleshooting

1. **Mailto links not working:**
   - Check default email client configuration
   - Test with simple `<a href="mailto:test@example.com">Test</a>`
   - Corporate firewalls may block external email links

2. **Currency symbols corrupted:**
   - File encoding issue - resave as UTF-8
   - Avoid copy/paste between different systems
   - Characters like â‚¬ instead of € indicate encoding problems

3. **CloudFront caching:**
   - Changes may take 5-15 minutes to propagate globally
   - Create invalidation for immediate updates
   - Use incognito browser for testing fresh content

## Future Enhancements

**Planned Improvements:**
- Migration to Fargate-based platform after market validation
- Contact form integration (current uses mailto)
- Analytics integration for conversion tracking
- A/B testing framework for service descriptions

**Content Evolution:**
- Real client testimonials after first engagements
- Case study development with actual results
- Thought leadership blog integration
- Service tier optimization based on demand

## Contact Information

**Business Email:** ashley@tacticintel.com  
**Website:** tacticintel.com  
**Target Markets:** UK & European companies (€1M-50M revenue range)  
**Core Specialization:** Database performance optimization across PostgreSQL, MySQL, SQL Server, Oracle, NoSQL platforms

---

**Project Status:** Initial market validation phase - ready for prospect testing and lead generation.