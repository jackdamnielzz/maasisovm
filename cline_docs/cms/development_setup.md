# Development Setup Documentation

Dit document beschrijft de ontwikkelomgeving setup en infrastructuur vereisten voor de Git-based CMS implementatie met Decap CMS.

## Prerequisites

### Required Software
- Git
- VS Code (aanbevolen IDE)
- Web browser
- GitHub account

### Development Tools
- Markdown editor
- ESLint voor code kwaliteit
- Prettier voor code formatting
- Live Server voor lokale development

## Environment Setup

### 1. Git Setup
```bash
# Configureer Git met je gegevens
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Clone de repository
git clone [repository-url]
```

### 2. Project Structuur
```
maasiso-website/
├── content/           # Markdown content
│   ├── pages/        # Pagina content
│   ├── blog/         # Blog posts
│   └── services/     # Diensten content
├── static/           # Static assets
│   ├── images/       # Afbeeldingen
│   └── documents/    # Downloadbare bestanden
├── templates/        # HTML templates
├── public/          # Gebouwde website
└── admin/           # CMS configuratie
    └── config.yml   # Decap CMS config
```

### 3. Decap CMS Setup
```yaml
# admin/config.yml
backend:
  name: git-gateway
  branch: main

media_folder: "static/images"
public_folder: "/images"

collections:
  - name: "pages"
    label: "Pages"
    folder: "content/pages"
    create: true
    fields:
      - {label: "Title", name: "title", widget: "string"}
      - {label: "Body", name: "body", widget: "markdown"}
```

## Development Workflow

### 1. Lokale Ontwikkeling
```bash
# Start lokale server
npx serve

# In een ander terminal venster, voor CMS preview
npx decap-server
```

### 2. Content Management
- Werk in feature branches voor content updates
- Review changes in preview
- Merge via pull requests
- Automatische deployment na merge

### 3. Version Control
- Feature branch workflow
- Pull request reviews
- Conventional commits
- Git-based backup

## Content Workflow

### 1. Content Creatie
- Schrijf content in Markdown
- Preview in lokale omgeving
- Commit changes naar feature branch
- Create pull request voor review

### 2. Media Management
- Upload media naar /static/images
- Optimaliseer afbeeldingen voor web
- Gebruik relatieve paths in content
- Versiebeheer via Git LFS

## Deployment

### 1. Cloud86 Setup
- FTP/SFTP toegang configureren
- SSL certificaat verifiëren
- DNS instellingen controleren
- Backup strategie implementeren

### 2. Deployment Process
- Automatische builds na merge
- Asset optimalisatie tijdens build
- Cache invalidatie
- Zero-downtime updates

## Security

### 1. Authenticatie
- GitHub OAuth integratie
- Role-based toegang
- Secure admin routes
- Session management

### 2. Content Beveiliging
- Branch protection rules
- Pull request reviews
- Input sanitization
- Media upload restricties

## Performance

### 1. Build Optimalisatie
- Markdown naar HTML conversie
- Asset minificatie
- Image optimalisatie
- Cache headers

### 2. Delivery Optimalisatie
- CDN caching
- Gzip compressie
- Lazy loading
- Resource hints

## Backup & Recovery

### 1. Git-based Backup
- Automatische Git backups
- Media backup via Git LFS
- Config file backups
- Regular commits

### 2. Recovery Procedures
- Git revert/reset procedures
- Branch restoration
- Media recovery
- Config recovery

## Monitoring

### 1. Build Monitoring
- Build success/failure alerts
- Deploy status tracking
- Error logging
- Performance metrics

### 2. Content Monitoring
- Content update tracking
- Media usage monitoring
- User activity logs
- Security alerts

## Documentation Updates
Dit document bijwerken bij:
- Workflow veranderingen
- Nieuwe tools/dependencies
- Security updates
- Process verbeteringen

## Troubleshooting Guide

### Common Issues
1. Git Workflow
   - Branch conflicts
   - Merge issues
   - Permission errors

2. Content Management
   - Markdown rendering
   - Media upload issues
   - Preview problemen

3. Deployment
   - Build failures
   - Cache issues
   - FTP/SFTP problemen

### Support Resources
- Decap CMS Documentation
- Git Documentation
- Cloud86 Support
- Project Wiki
