# 🏟️ Personal Website Setup Guide

Welcome to your beautiful personal website! This guide will help you understand how everything works and how to customize it.

## 🚀 Getting Started

### Running Your Website

1. **Start the development server:**
   ```bash
   npm run dev
   ```
   This will start your website at `http://localhost:4321`

2. **Build for production:**
   ```bash
   npm run build
   ```
   This creates optimized files in the `dist/` folder

3. **Preview production build:**
   ```bash
   npm run preview
   ```

## 🎯 How It Works

### The Soccer Ball Navigation
Your website features a unique soccer ball that travels along a dotted line as you scroll! Here's how it works:

- **Automatic Movement**: The soccer ball moves to different positions as you scroll through sections
- **Click Navigation**: Click the soccer ball to go to the next section
- **Button Navigation**: Use the text buttons (About me, Skills, Projects) to jump to specific sections

### The Four Sections

1. **Home (Desktop 1)**: Your main landing page with "Hey There!!" message
2. **About Me (Desktop 2)**: Information about you living in Vancouver and loving to program
3. **Skills (Desktop 3)**: Your technical skills with colorful indicators
4. **Projects (Desktop 4)**: Your projects section (currently shows "TBD...")

## 🎨 Customizing Your Website

### Changing Content

#### Personal Information
Edit `src/pages/index.astro` to update:

- **Your name**: Change "Elliot" to your name
- **Location**: Update "Vancouver BC Canada" 
- **Bio**: Modify the "I love to program..." text
- **Skills**: Add/remove/change skills in the skills section

#### Adding Projects
In the Projects section, replace the "TBD..." with your actual projects:

```html
<div class="bg-white bg-opacity-10 backdrop-blur-sm rounded-2xl p-8 md:p-12 border border-white border-opacity-20">
  <div class="grid md:grid-cols-2 gap-8">
    <div class="text-left">
      <h3 class="text-2xl font-bold mb-4">Project Name</h3>
      <p class="text-lg mb-4">Description of your project...</p>
      <a href="https://github.com/yourusername/project" class="text-yellow-300 hover:text-yellow-200 transition-colors">
        View on GitHub →
      </a>
    </div>
    <!-- Add more projects -->
  </div>
</div>
```

### Changing Colors and Styling

#### Custom Colors
The website uses these main colors (defined in `tailwind.config.mjs`):
- `sky-blue`: #87CEEB
- `cloud-white`: #F0F8FF  
- `grass-green`: #228B22
- `stadium-beige`: #D2B48C

You can change these or add new colors in the `tailwind.config.mjs` file.

#### Section Overlays
Each section has a different colored overlay:
- Home: Black overlay (30% opacity)
- About: Blue overlay (20% opacity)  
- Skills: Green overlay (20% opacity)
- Projects: Purple overlay (20% opacity)

Change these in the `index.astro` file by modifying the `bg-{color}-{shade}` classes.

### Customizing Animations

#### Soccer Ball Position
The soccer ball positions are defined in the JavaScript:

```javascript
const ballPositions = [
  { top: '5%', left: '12px' },    // Home
  { top: '35%', left: '20px' },   // About me  
  { top: '65%', left: '28px' },   // Skills
  { top: '90%', left: '35px' }    // Projects
];
```

Adjust these values to change where the ball appears for each section.

#### Transition Speed
Change the soccer ball animation speed by modifying:
```css
.transition-all duration-500 ease-out
```

#### Float Animation
The soccer ball has a floating animation. You can customize it in `tailwind.config.mjs`:

```javascript
keyframes: {
  float: {
    '0%, 100%': { transform: 'translateY(0px)' },
    '50%': { transform: 'translateY(-10px)' },
  }
}
```

## 🖼️ Changing Assets

### Background Image
Replace `public/assets_task_01jzzp8yv4f4ta2qre3f31g1z1_1752336673_img_0.webp` with your own stadium or background image.

### Soccer Ball Icon
Replace `public/SoccerBall.svg` with your own icon (keep it as an SVG for best results).

### Navigation Path
Replace `public/DottedLine.svg` with your own path design.

## 📱 Mobile Responsiveness

The website is fully responsive and includes:
- **Text scaling**: Larger text on desktop (`md:text-8xl`), smaller on mobile (`text-6xl`)
- **Padding adjustments**: More padding on desktop (`md:p-12`), less on mobile (`p-8`)
- **Flexible layouts**: Content adapts to screen size

## 🚀 Deployment

### Deploy to Vercel (Recommended)
1. Push your code to GitHub
2. Connect your GitHub repo to Vercel
3. Vercel will automatically deploy your site!

### Deploy to Netlify
1. Run `npm run build`
2. Upload the `dist/` folder to Netlify

### Deploy to GitHub Pages
1. Set `base: '/your-repo-name'` in `astro.config.mjs`
2. Run `npm run build`
3. Push the `dist/` folder to the `gh-pages` branch

## 💡 Tips and Tricks

### Adding New Sections
1. Add a new `<section>` with a unique ID
2. Update the `ballPositions` array with a new position
3. Add a new navigation button

### Smooth Scrolling
The website uses smooth scrolling by default. You can disable it by removing:
```css
html {
  scroll-behavior: smooth;
}
```

### Performance
- Images are optimized and use `object-cover` for proper scaling
- Animations use CSS transforms for better performance
- The soccer ball uses efficient position updates

## 🎯 Next Steps

1. **Add More Content**: Fill in your projects, add more sections
2. **Customize Colors**: Make it match your personal style
3. **Add Contact Info**: Include ways for people to reach you
4. **SEO Optimization**: Add meta descriptions and Open Graph tags
5. **Analytics**: Add Google Analytics or similar tracking

## 🐛 Troubleshooting

**Website not loading?**
- Make sure you ran `npm install`
- Check that the dev server is running on `http://localhost:4321`

**Soccer ball not moving?**
- Check browser console for JavaScript errors
- Ensure all assets are in the `public/` folder

**Styling issues?**
- Make sure TailwindCSS is properly configured
- Check that `global.css` is being imported

**Build errors?**
- Ensure all image paths start with `/` (e.g., `/SoccerBall.svg`)
- Check that all dependencies are installed

---

Enjoy your new personal website! 🎉

Feel free to customize it further and make it truly yours. The stadium theme with the soccer ball navigation makes it unique and memorable! 