# MaasISO Website

Deze repository bevat de website van MaasISO, geïmplementeerd met een Git-based CMS oplossing voor eenvoudig contentbeheer.

## 🚀 Technische Stack

- **Content Management**: Decap CMS (Git-based)
- **Content Format**: Markdown
- **Version Control**: Git
- **Hosting**: Cloud86
- **Assets**: Geoptimaliseerde afbeeldingen en documenten

## 📁 Project Structuur

```
maasiso-website/
├── content/           # Markdown content
│   ├── pages/        # Pagina content
│   ├── blog/         # Blog posts
│   ├── services/     # Diensten content
│   └── settings/     # Site instellingen
├── static/           # Static assets
│   ├── images/       # Afbeeldingen
│   └── documents/    # Downloadbare bestanden
├── templates/        # HTML templates
├── public/          # Gebouwde website
└── admin/           # CMS configuratie
    └── config.yml   # Decap CMS config
```

## 🛠️ Development Setup

1. Clone de repository:
   ```bash
   git clone [repository-url]
   cd maasiso-website
   ```

2. Start lokale development server:
   ```bash
   npx serve
   ```

3. Start CMS preview:
   ```bash
   npx decap-server
   ```

## 📝 Content Management

### Content Toevoegen/Bewerken

1. Navigeer naar `/admin` op de website
2. Log in met je GitHub account
3. Kies het content type dat je wilt bewerken
4. Maak wijzigingen in de Markdown editor
5. Preview je wijzigingen
6. Publiceer wanneer je tevreden bent

### Content Types

- **Pagina's**: Reguliere website pagina's
- **Diensten**: ISO en compliance diensten
- **Blog Posts**: Nieuws en updates
- **Instellingen**: Site-brede configuratie

### Media & Assets

- Upload afbeeldingen naar `/static/images`
- Optimaliseer afbeeldingen voor web gebruik
- Gebruik relatieve paths in content
- Ondersteunde formaten: jpg, png, svg, webp

## 🔄 Workflow

1. **Content Updates**
   - Werk in feature branches
   - Maak een pull request voor review
   - Merge na goedkeuring

2. **Development**
   - Ontwikkel in lokale omgeving
   - Test alle wijzigingen
   - Commit met duidelijke messages

3. **Deployment**
   - Automatische build na merge naar main
   - Preview deployment voor pull requests
   - Zero-downtime updates

## 🔒 Security

- Branch protection rules
- Pull request reviews verplicht
- GitHub OAuth authenticatie
- Regelmatige backups via Git

## 📚 Documentatie

Uitgebreide documentatie is beschikbaar in de `/cline_docs` directory:
- Project Roadmap
- Development Setup
- Content Guidelines
- Technical Documentation

## 🤝 Bijdragen

1. Fork de repository
2. Maak een feature branch
3. Commit je wijzigingen
4. Push naar de branch
5. Open een Pull Request

## 📫 Contact

Voor vragen of ondersteuning:
- Email: info@maasiso.nl
- GitHub Issues voor technische problemen

## 📄 Licentie

Copyright © 2024 MaasISO. Alle rechten voorbehouden.
