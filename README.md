# 🎆 New Year Celebration Page

A beautiful, interactive web page to celebrate the New Year with stunning fireworks animations, countdown timer, and festive effects.

![New Year Celebration](preview.png)

## ✨ Features

### 🎇 Interactive Fireworks
- Real-time particle-based fireworks animations
- Multiple firework types (circles, hearts, spirals, starbursts)
- Realistic physics with gravity and particle trails
- Sound effects for launches and explosions

### ⏰ Countdown Timer
- Live countdown to the next New Year
- Animated display with pulse effect
- Updates in real-time

### 🎨 Visual Effects
- Beautiful glassmorphism UI design
- Falling snow animation
- Gradient text animations
- Smooth transitions and hover effects
- Responsive design for all devices

### 🔊 Audio Features
- Multiple firework sound effects
- Background celebration music
- Volume control with custom slider
- Audio preloading for smooth playback

### 🌐 Social Sharing
- Share on Twitter, Facebook, and WhatsApp
- Custom sharing messages
- Elegant social media buttons

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Local web server (optional, for development)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/new-year-celebration.git
```

2. Navigate to the project directory:
```bash
cd new-year-celebration
```

3. Open `index.html` in your web browser or serve it through a local web server.

### Running Locally

You can use any of these methods to run the page locally:

#### Using Python (Python 3):
```bash
python -m http.server 8000
```

#### Using Node.js:
```bash
npx http-server
```

Then open `http://localhost:8000` in your browser.

## 🎮 Usage

1. **Launch Fireworks:**
   - Click the "LAUNCH FIREWORKS" button to start the show
   - Fireworks will automatically launch with sound effects
   - The display lasts for 25 seconds

2. **Audio Controls:**
   - Use the volume slider to adjust sound effects
   - Volume changes affect all sound effects
   - Mute by setting volume to 0

3. **Social Sharing:**
   - Click on any social media icon to share
   - Custom message will be generated automatically
   - Share link will open in a new tab

## 🎨 Customization

### Changing Colors
Edit the CSS variables in the `:root` selector:
```css
:root {
    --primary-color: #4285f4;
    --accent-color: #ff4081;
    --text-color: #ffffff;
    --bg-color: #000000;
    --card-bg: rgba(255, 255, 255, 0.1);
}
```

### Modifying Fireworks
Adjust fireworks parameters in the JavaScript:
```javascript
const particleCount = Math.floor(Math.random() * 50) + 50; // Number of particles
const velocity = Math.random() * 2 + 2; // Particle speed
const gravity = 0.1; // Particle gravity
```

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Android Chrome)

## 🔧 Technical Details

### Technologies Used
- HTML5 Canvas for fireworks
- CSS3 animations and transitions
- Modern JavaScript (ES6+)
- Web Audio API for sound effects
- CSS Custom Properties for theming

### Performance
- Optimized particle system
- Audio preloading
- Efficient canvas rendering
- Smooth animations with requestAnimationFrame
- Automatic cleanup of finished effects

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- Firework sound effects from [Mixkit](https://mixkit.co/)
- Icons from various open-source projects
- Font from Google Fonts (Poppins)

## 📞 Contact

Your Name - [@yourtwitter](https://twitter.com/yourtwitter) - email@example.com

Project Link: [https://github.com/yourusername/new-year-celebration](https://github.com/yourusername/new-year-celebration)

---

Made with ❤️ for the New Year celebration
