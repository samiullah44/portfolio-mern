# 🚀 Modern Artistic MERN Portfolio - Sami Ullah

A stunning, highly-animated portfolio website featuring rocket animations, diamond portrait, and artistic micro-interactions.

## 🎯 How to Replace with Your Real Content

### Quick Content Update Checklist:
1. **Personal Info**: Update `server/seed.js` - replace demo name, email, bio
2. **Portrait**: Replace `client/public/images/portrait.jpg` with your square photo
3. **Resume**: Replace `client/public/resume.pdf` with your actual resume
4. **Projects**: Edit projects array in `server/seed.js` 
5. **Experience**: Update experience entries in `server/seed.js`
6. **Social Links**: Modify social links in `server/seed.js`
7. **Certificates**: Add your certificates to `server/seed.js` and images to `client/public/images/certificates/`

## ⚡ Quick Start

### Prerequisites
- Node.js 18+
- MongoDB Atlas account
- Git

### Local Development

```bash
# Clone repository
git clone <your-repo-url>
cd portfolio-mern

# Install root dependencies
npm install

# Install client dependencies
cd client && npm install

# Install server dependencies
cd ../server && npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your MongoDB connection string and email credentials

# Seed database with demo content
npm run seed

# Start development servers
npm run dev
```

Visit: http://localhost:5173 (Frontend) and http://localhost:5000 (Backend)

## 🏗️ Project Structure

```
portfolio-mern/
├── client/                 # React frontend (Vite)
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── pages/         # Page components
│   │   ├── hooks/         # Custom hooks
│   │   ├── utils/         # Utilities
│   │   ├── styles/        # Global styles
│   │   └── types/         # TypeScript types
│   ├── public/            # Static assets
│   └── package.json
├── server/                # Express backend
│   ├── src/
│   │   ├── routes/        # API routes
│   │   ├── models/        # MongoDB models
│   │   ├── middleware/    # Express middleware
│   │   └── utils/         # Server utilities
│   ├── seed.js           # Database seeding
│   └── package.json
├── .github/workflows/     # CI/CD
└── docker-compose.yml     # Docker setup
```

## 🎨 Features

### Visual & Interactive
- **Animated Rocket**: Hero section rocket that launches with particle trails
- **Diamond Portrait**: Floating portrait with social links between facets
- **Background Modes**: Toggle between animated strings and vivid colors per section
- **Micro-interactions**: Hover physics, tilt effects, and smooth transitions
- **Theme System**: Light/dark mode with per-section customization

### Technical
- **MERN Stack**: React + Node.js + Express + MongoDB
- **Animations**: Framer Motion + custom WebGL effects
- **Responsive**: Mobile-first design with accessibility
- **Admin Panel**: Content management with token-based auth
- **Email Integration**: Contact form with Nodemailer
- **SEO Optimized**: Meta tags, sitemap, structured data

## 🔧 Environment Variables

Create `.env` file in root:

```env
# Database
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/portfolio

# Email Service
EMAIL_SERVICE=gmail
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password

# Admin
ADMIN_TOKEN=your-secure-admin-token-here

# Server
PORT=5000
NODE_ENV=development
```

## 🚀 Deployment

### Frontend (Vercel)
1. Connect GitHub repo to Vercel
2. Set build command: `cd client && npm run build`
3. Set output directory: `client/dist`
4. Deploy

### Backend (Render)
1. Create new Web Service on Render
2. Connect GitHub repo
3. Set build command: `cd server && npm install && npm run build`
4. Set start command: `cd server && npm start`
5. Add environment variables
6. Deploy

### Full Deployment Commands
```bash
# Build everything
npm run build

# Create deployment zip
npm run deploy:build

# Manual deployment
# Upload portfolio-deploy.zip to your hosting service
```

## 🧪 Testing

```bash
# Run server tests
cd server && npm test

# Run linting
npm run lint

# Format code
npm run format
```

## 🐳 Docker Development

```bash
# Start with Docker
npm run docker:dev
```

## 🎯 Admin Panel

Access admin features at `/admin` with your admin token to:
- Edit projects, experience, and certificates
- Update personal information
- Manage content without database access

## 📱 Accessibility Features

- Keyboard navigation support
- Screen reader optimized
- Reduced motion support
- High contrast mode
- Focus indicators
- ARIA labels and descriptions

## 🎨 Visual Design System

Located in `client/src/styles/design-tokens.json`:
- Color system with 6 color ramps
- Typography scale with Inter fonts
- 8px spacing system
- Animation timing functions
- Responsive breakpoints

## 🔄 Content Management

### Adding Projects
Edit `server/seed.js` projects array:
```javascript
{
  title: "Your Project Name",
  description: "Brief description",
  longDescription: "Detailed description...",
  techStack: ["React", "Node.js"],
  githubUrl: "https://github.com/...",
  liveUrl: "https://your-project.com",
  image: "/images/projects/project-name.jpg",
  featured: true
}
```

### Updating Experience
Edit `server/seed.js` experience array with your work history.

### Managing Certificates
Add certificate images to `client/public/images/certificates/` and update the certificates array in `server/seed.js`.

## 🌟 Animation Controls

- **Rocket Animation**: Click rocket in hero to trigger launch
- **Disable Animations**: Toggle in settings or automatically respects `prefers-reduced-motion`
- **Performance Mode**: Automatically reduces animations on low-power devices

## 🔧 Customization

### Changing Colors
Edit `client/src/styles/design-tokens.json` and update Tailwind config.

### Adding Sections
1. Create new component in `client/src/components/sections/`
2. Add to main page
3. Update navigation
4. Add corresponding backend model if needed

### Modifying Animations
Edit animations in `client/src/components/animations/` using Framer Motion.

## 📞 Support

For issues or questions:
1. Check the GitHub Issues
2. Review the documentation
3. Contact: yourname@example.com

## 📄 License

MIT License - feel free to use this for your own portfolio!

---

**Live URLs:**
- Frontend: [Your Vercel URL]
- Backend API: [Your Render URL]
- Admin Panel: [Frontend URL]/admin (Token: your-admin-token)