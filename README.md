# 🎵 Cinematic 3D Audio Visualizer

A stunning, real-time 3D audio visualizer built with Three.js that transforms your music into mesmerizing visual experiences.

![Audio Visualizer](https://img.shields.io/badge/Three.js-0.155.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

### 🎨 Multiple Visualization Modes
- **🌊 Waveform** - Classic audio waveform with dynamic colors
- **🌀 Tunnel** - Rotating tunnel effect that pulses with the music
- **🔮 Sphere** - 3D spherical mapping of audio data
- **✨ Particles** - Particle-only mode with beat-reactive bursts
- **⭕ Rings** - Energy rings that pulse and expand with beats

### 🎭 Visual Effects
- **Bloom & Glow** - Adjustable bloom post-processing for ethereal effects
- **Afterimage** - Motion blur trails for smooth animations
- **Film Grain** - Subtle cinematic grain overlay
- **Beat Detection** - Automatic beat detection with visual responses (toggleable)
- **Color Schemes** - 4 beautiful color palettes:
  - 💚 Neon (Cyan/Purple/Pink)
  - 🔥 Fire (Orange/Red/Yellow)
  - 🌊 Ocean (Cyan/Blue/Aqua)
  - 🌅 Sunset (Pink/Orange/Red)

### 🎛️ Controls
- **Intensity Slider** - Control visualization amplitude
- **Bloom Slider** - Adjust glow strength (0-2)
- **Speed Slider** - Playback speed control (0.5x - 2x)
- **Camera Auto-movement** - Automatic camera rotation
- **Beat Effects Toggle** - Enable/disable beat detection flash effects
- **Play/Pause/Stop** - Full playback control
- **File Upload** - Load your own audio files
- **Default Audio** - Quick-load button for demo track

### 📊 Real-time Audio Info
- Duration & current time
- Sample rate
- Frame count
- Beat detection status
- Live frequency spectrum display

## 🚀 Quick Start

### Option 1: Open Directly
1. Clone this repository:
   ```bash
   git clone https://github.com/carthworks/audio-visualizer.git
   cd audio-visualizer
   ```

2. Open `index.html` in your browser and click "Launch Visualizer"

### Option 2: Local Server (Recommended)
1. Install a local server (if you don't have one):
   ```bash
   npm install -g http-server
   ```

2. Start the server:
   ```bash
   http-server
   ```

3. Open `http://localhost:8080` in your browser

4. Click "Launch Visualizer" to start

## 🎮 How to Use

1. **Load Audio**:
   - Click "Default" to load the demo track, OR
   - Click "Choose File" to upload your own audio (MP3, WAV, etc.)

2. **Choose Visualization Mode**:
   - Click any of the mode buttons (Wave, Tunnel, Sphere, Particles, Rings)

3. **Customize Visuals**:
   - Adjust sliders for Intensity, Bloom, Speed, and Camera movement
   - Select a color scheme (Neon, Fire, Ocean, Sunset)
   - Toggle beat effects on/off

4. **Control Playback**:
   - Click "Play" to start the visualization
   - Use "Pause" to pause
   - Click "Animate" to preview without audio

## 🎨 Color Schemes

| Scheme | Primary | Secondary | Tertiary |
|--------|---------|-----------|----------|
| **Neon** | Cyan (#00f5a0) | Purple (#7b61ff) | Pink (#ff6b9d) |
| **Fire** | Orange (#ff6b00) | Red (#ff0844) | Yellow (#ffaa00) |
| **Ocean** | Cyan (#00d4ff) | Blue (#0066ff) | Aqua (#00ffaa) |
| **Sunset** | Pink (#ff6b9d) | Orange (#ffa500) | Red (#ff3366) |

## 🛠️ Technical Details

### Built With
- **Three.js** (v0.155.0) - 3D graphics library
- **OrbitControls** - Camera controls
- **EffectComposer** - Post-processing pipeline
- **UnrealBloomPass** - Bloom effect
- **AfterimagePass** - Motion blur
- **FilmPass** - Film grain effect
- **GSAP** - Smooth animations
- **Web Audio API** - Audio processing and analysis

### Performance Features
- High-performance WebGL rendering
- Optimized particle system with object pooling
- Dynamic buffer updates for smooth animations
- Efficient FFT calculations for real-time analysis
- Instanced rendering for particles

### Audio Processing
- Custom FFT implementation
- Spectral centroid calculation
- Beat detection algorithm
- 64-band frequency analysis
- Real-time waveform visualization

## 📁 Project Structure

```
audio-visualizer/
├── audio/                          # Audio files
│   └── games-worldbeat-466.mp3    # Default demo track
├── cinematic_3_d_sound_visualizer_upgraded.html  # Main visualizer
├── index.html                      # Landing page
├── test_audio_path.html           # Audio path tester
└── README.md                       # This file
```

## 🎵 Supported Audio Formats

- MP3
- WAV
- OGG
- M4A
- FLAC
- Any format supported by the Web Audio API

## 🌐 Browser Compatibility

- ✅ Chrome/Edge (Recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Opera

**Note**: For best performance, use a modern browser with WebGL 2.0 support.

## 🔧 Customization

### Adjust Beat Detection Sensitivity
Edit line 478 in `cinematic_3_d_sound_visualizer_upgraded.html`:
```javascript
beatThreshold: 1.3,  // Lower = more sensitive, Higher = less sensitive
```

### Change Default Bloom Strength
Edit line 475:
```javascript
bloomStrength: 0.4,  // Range: 0-2
```

### Modify Particle Count
Edit the particle spawn calls (e.g., line 1181):
```javascript
spawnParticles(0, 1, 0, 20, 1.0);  // Last params: count, strength
```

## 📝 License

MIT License - feel free to use this project for personal or commercial purposes.

## 🙏 Credits

- Audio processing powered by Web Audio API
- 3D graphics by Three.js
- Default audio track: "Games Worldbeat 466"

## 🐛 Known Issues

- Large audio files (>100MB) may take time to load
- Beat detection works best with music that has clear percussion
- Some browsers may require user interaction before playing audio

## 🚀 Future Enhancements

- [ ] VR/AR support
- [ ] Audio recording and export
- [ ] More visualization modes
- [ ] Custom shader effects
- [ ] Playlist support
- [ ] Social sharing features

## 💬 Feedback

Found a bug or have a feature request? Please open an issue on GitHub!

---

**Made with ❤️ and Three.js**
