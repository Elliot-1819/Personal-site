# 🏟️ Elliot's Personal Website

A beautiful, scroll-animated personal website with a unique soccer ball navigation system! Built with modern web technologies and featuring a stunning stadium background.

## ✨ Features

- **Interactive Soccer Ball Navigation**: A soccer ball travels along a dotted line path as you scroll
- **Four Themed Sections**: Home, About Me, Skills, and Projects
- **Smooth Animations**: Beautiful transitions and hover effects
- **Responsive Design**: Looks great on all devices
- **Modern Tech Stack**: Built with Astro, TailwindCSS, and vanilla JavaScript

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Visit http://localhost:4321
```

## 🎯 Sections

1. **Home**: Welcome message with your name and introduction
2. **About Me**: Personal information about living in Vancouver and programming passion
3. **Skills**: Technical skills with colorful indicators (Python, HTML, CSS, JavaScript, ML)
4. **Projects**: Showcase of your work (currently "TBD" - ready for your projects!)

## 🎨 Navigation

- **Scroll Navigation**: The soccer ball automatically moves as you scroll
- **Click Navigation**: Click the soccer ball to advance to the next section  
- **Button Navigation**: Use the labeled buttons (About me, Skills, Projects) to jump directly to sections

## 🛠️ Tech Stack

- **Astro**: Modern static site generator with excellent performance
- **TailwindCSS**: Utility-first CSS framework for rapid styling
- **Vanilla JavaScript**: Smooth scroll interactions and animations
- **SVG Graphics**: Scalable vector graphics for the soccer ball and dotted line

## 📁 Project Structure

```
├── public/                 # Static assets
│   ├── SoccerBall.svg     # Soccer ball icon
│   ├── DottedLine.svg     # Navigation path
│   └── assets_task_...    # Stadium background image
├── src/
│   ├── pages/
│   │   └── index.astro    # Main page
│   └── styles/
│       └── global.css     # TailwindCSS styles
├── package.json
├── astro.config.mjs
├── tailwind.config.mjs
├── README.md
└── SETUP.md              # Detailed customization guide
```

## 🎨 Customization

Check out `SETUP.md` for a comprehensive guide on:
- Changing personal information
- Adding your projects
- Customizing colors and animations
- Modifying the soccer ball positions
- Deployment options

## 🚀 Deployment

The website is ready to deploy to:
- **Vercel** (recommended)
- **Netlify**
- **GitHub Pages**

Simply run `npm run build` to create production files.

---

**Ready to make it yours?** Open `src/pages/index.astro` and start customizing! 🎉
