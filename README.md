# 💃 Roblox Dance & Emote GUI

A modern, minimalist GUI for playing dance animations and emotes in Roblox with **instant response** and **zero delay** switching.

![Version](https://img.shields.io/badge/version-2.0-blue)
![Platform](https://img.shields.io/badge/platform-Roblox-red)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

- 🚀 **Instant Animation Switching** - Zero delay between animations
- 📱 **Mobile & PC Support** - Responsive design for all devices
- 🎨 **Modern UI Design** - Clean, minimalist interface with smooth transitions
- 🔍 **Search Functionality** - Quickly find your favorite animations
- 🎭 **100+ Animations** - Large collection of dances and emotes
- 💾 **Persistent GUI** - Doesn't reset on character respawn
- ⚡ **Lightweight** - Clean code with no complex effects

## 📸 Preview

The GUI features:
- Compact header design
- Two categories: Dance & Emote
- Search bar for quick filtering
- Scrollable animation list
- One-click stop button

## 🎯 Animation Categories

### 💃 Dances (80+ animations)
Including popular dances like:
- Griddy, Floss, Take The L
- K-pop dances (TWICE, NCT, Stray Kids)
- Trending TikTok dances
- Classic dances (Macarena, Gangnam Style)

### 🎭 Emotes (60+ animations)
Including various emotes like:
- Floating poses and sits
- Cute kawaii poses
- Action emotes
- Idle animations

## 🔧 Installation

### Method 1: Direct Script
1. Open Roblox Studio
2. Create a **ScreenGui** in **StarterGui**
3. Create a **LocalScript** inside the ScreenGui
4. Copy and paste the script code into the LocalScript
5. Play and enjoy!

### Method 2: Model (Coming Soon)
- Install directly from Roblox library

## 📋 Usage

1. **Open GUI**: Click the 💃 button on the left side of your screen
2. **Choose Category**: Switch between "Dance" and "Emote" tabs
3. **Search**: Use the search bar to filter animations
4. **Play Animation**: Click any animation name to play it instantly
5. **Stop**: Click the "⏹ STOP" button to stop the current animation
6. **Close GUI**: Click the X button to close the panel

## 🎮 Controls

- **Left-click** - Select animation / Toggle GUI
- **Search bar** - Type to filter animations
- **Scroll** - Browse through animation list

## ⚙️ Technical Details

### Performance
- **Animation Switch**: 0ms delay
- **Fade Time**: 0 seconds for instant response
- **Priority**: Action priority for dances, Idle for emotes
- **Memory**: Lightweight with minimal overhead

### Compatibility
- ✅ Works on **PC** (keyboard + mouse)
- ✅ Works on **Mobile** (touch controls)
- ✅ Works on **Tablet**
- ✅ Auto-adjusts UI size based on platform

## 🎨 Customization

You can easily customize:
- **Colors**: Modify the `COLORS` table
- **UI Sizes**: Adjust `UI_CONFIG` values
- **Animations**: Add/remove from `animations` table

Example - Change accent color:
```lua
accent = Color3.fromRGB(100, 150, 255), -- Change these RGB values
```

## 🐛 Troubleshooting

**GUI not showing?**
- Make sure the script is in StarterGui > ScreenGui > LocalScript
- Check if ResetOnSpawn is set to false

**Animations not playing?**
- Wait for your character to fully load
- Check console for any error messages
- Make sure you're in a game, not Studio edit mode

**Lag or delay?**
- This version has zero artificial delays
- If experiencing lag, check your internet connection

## 📝 Changelog

### Version 2.0 (Current)
- ✅ Instant animation switching (0ms delay)
- ✅ Removed all complex effects for maximum performance
- ✅ Cleaner, simpler codebase
- ✅ Improved tab switching response
- ✅ Optimized UI rendering

### Version 1.x
- Dynamic weight blending
- Hip offset animations
- Micro speed fluctuations
- Joint damping effects

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new animations
- Submit pull requests
- Improve documentation

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**ItoRenz**
- Platform: Roblox
- Version: 2.0 - Clean & Instant

## ⭐ Support

If you find this GUI useful, please consider:
- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting features
- 📢 Sharing with friends

## 🔗 Links

- [Roblox Profile](#) (Add your profile)
- [Report Issues](../../issues)
- [Request Features](../../issues/new)

---

**Made with ❤️ for the Roblox community**

*Last Updated: October 2025*
