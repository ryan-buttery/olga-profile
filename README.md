# English Teaching Website - Olga Profile

A modern, responsive Bootstrap website for English teaching services, specifically designed for Polish speakers.

## 🌟 Features

- **Multi-page architecture**: Home, Work with Me, About Me, Newsletter
- **Responsive design**: Bootstrap 5.3.2 with custom SASS styling
- **Brand colors**: Teal (#00a6a6), Orange (#ffad05), Navy (#0d1f48)
- **Modern UI**: Gradients, animations, and interactive elements
- **Containerized**: Docker-ready for easy deployment

## 🚀 Quick Start

### Development

```bash
# Install dependencies
npm install

# Build CSS from SASS
npm run build

# Watch SASS changes (development)
npm run sass:watch

# Open index.html in your browser
```

### Docker Deployment

#### Option 1: Docker Compose (Recommended)
```bash
# Build and start the container
npm start
# or
docker-compose up -d

# View logs
npm run docker:compose:logs

# Stop the container
npm stop
# or
docker-compose down
```

#### Option 2: Direct Docker Commands
```bash
# Build the image
npm run docker:build

# Run the container
npm run docker:run

# Stop and remove the container
npm run docker:stop
```

## 🌐 Access

Once running, the website will be available at:
- **Local development**: Open `index.html` directly
- **Docker container**: http://localhost:3000
- **Health check**: http://localhost:3000/health

## 📂 Project Structure

```
├── index.html              # Home page
├── work-with-me.html       # Services page
├── about-me.html           # About page
├── newsletter.html         # Newsletter signup
├── assets/
│   ├── scss/              # SASS source files
│   │   ├── _variables.scss # Brand colors & variables
│   │   └── style.scss     # Main stylesheet
│   └── css/               # Compiled CSS
├── Dockerfile             # Container configuration
├── docker-compose.yml     # Docker Compose setup
├── nginx.conf             # Nginx configuration
└── package.json           # Build scripts & dependencies
```

## 🎨 Brand Colors

- **Primary**: `#00a6a6` (Teal) - Main brand color
- **Secondary**: `#ffad05` (Orange) - Highlights & CTAs
- **Accent**: `#0d1f48` (Navy) - Text & emphasis
- **Neutral**: `#ffffff` (White) - Backgrounds & text

## 🔧 Customization

### Updating Colors
Edit `assets/scss/_variables.scss`:
```scss
$brand-primary: #00a6a6;
$brand-secondary: #ffad05;
$brand-accent: #0d1f48;
```

Then rebuild:
```bash
npm run build
```

### Content Updates
- Update HTML files directly
- Replace placeholder images in the teacher photo sections
- Modify contact information and social links
- Connect newsletter form to your email service

## 🐳 Docker Details

### Multi-stage Build
- **Stage 1**: Node.js - Installs dependencies and builds SASS
- **Stage 2**: Nginx Alpine - Serves static files efficiently

### Security Features
- Non-root user execution
- Security headers in nginx
- Health check endpoint
- Minimal attack surface

### Production Ready
- Gzip compression enabled
- Static asset caching
- Error page handling
- Hidden nginx version

## 📧 Newsletter Integration

The newsletter form is ready to integrate with:
- Mailchimp
- ConvertKit
- EmailJS
- Your custom backend

Update the form action in `newsletter.html` and connect to your preferred service.

## 🔒 Security

The nginx configuration includes:
- Security headers (XSS protection, Content Security Policy)
- Hidden server tokens
- Access restrictions for sensitive files
- Gzip compression for performance

## 📱 Responsive Design

- Mobile-first approach
- Bootstrap 5 grid system
- Touch-friendly interactions
- Optimized typography scaling

## 🌍 Deployment Options

This containerized setup works with:
- **Local development**: Docker Desktop
- **Cloud platforms**: AWS ECS, Google Cloud Run, Azure Container Instances
- **VPS hosting**: Any Docker-compatible server
- **Kubernetes**: Can be deployed with k8s manifests

## 📞 Support

For customization or deployment assistance, refer to the inline documentation in the code files.