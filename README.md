# 💃 Roblox Dance & Emote GUI v4.0

<div align="center">

![Version](https://img.shields.io/badge/version-4.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Roblox-red.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

**Modern GUI for Dance & Emote in Roblox with Server-Side Persistent Favorites**

[Features](#-key-features) • [Installation](#-installation) • [Usage](#-how-to-use) • [Documentation](#-technical-features)

</div>

---

## ✨ Key Features

- 🎭 **300+ Animations** - Most complete Dance & Emote collection
- 💾 **Server-Side DataStore** - Favorites permanently saved on server
- ⚡ **Instant Play** - 0ms delay animation switching with preload system
- ⭐ **Favorites System** - Save favorite animations & auto-sync to server
- 📱 **Mobile & PC Support** - Responsive UI for all platforms
- 🎨 **Modern Minimalist UI** - Sleek design with smooth animations
- 🔄 **Auto-Sync** - Favorites synchronized automatically across sessions
- 💪 **Never Lose Data** - Favorites persist through rejoins & server restarts

---

## 📦 Installation

### Method 1: Manual Installation

#### Step 1: Install Server Script

1. Open **Roblox Studio**
2. Copy the script from **`ServerScript.lua`**
3. In Explorer, find **`ServerScriptService`**
4. Create new **Script** (not LocalScript)
5. Paste the server script code
6. Rename to **"DanceEmoteServer"** (optional)

#### Step 2: Install Client Script

1. Copy the script from **`ClientScript.lua`**
2. In Explorer, navigate to **`StarterPlayer`** → **`StarterPlayerScripts`**
3. Create new **LocalScript**
4. Paste the client script code
5. Rename to **"DanceEmoteClient"** (optional)

#### Step 3: Enable API Services

1. Go to **Home** → **Game Settings**
2. Click **Security** tab
3. Enable **"Enable Studio Access to API Services"**
4. Enable **"Allow HTTP Requests"** (if needed)
5. Click **Save**

#### Step 4: Test

1. Press **F5** or click **Play** button
2. Look for console messages:
   ```
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
   👤 Author: ItoRenz00
   ✅ Dance & Emote Server Script Active
   💾 DataStore System Ready
   📦 Version: 4.0 - SERVER DATASTORE SYSTEM
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
   ```
3. Click the **💃 button** on the left side of screen
4. GUI should slide open smoothly

### Method 2: Model Installation

Coming soon to Roblox Library...

---

## 🎮 How to Use

### Opening the GUI

Click the **💃 button** on the left side of your screen. The GUI will smoothly slide open from the left.

### Playing Animations

1. **Select a Tab:**
   - **Dance** - All dance animations
   - **Emote** - All emote animations
   - **★ Fav** - Your favorite animations

2. **Play Animation:**
   - Click on any animation name
   - Animation plays instantly with 0ms delay
   - Active animation is highlighted in blue

### Managing Favorites

#### Adding to Favorites:
1. Find an animation you like
2. Click the **☆ star icon** on the right side
3. Star turns **yellow (★)** when favorited
4. Automatically saved to server

#### Removing from Favorites:
1. Click the **yellow ★** to unfavorite
2. Star becomes **gray (☆)**
3. Removed from Favorites tab
4. Changes saved to server instantly

### Stopping Animation

Click the red **⏹ STOP** button at the bottom to stop current animation.

### Closing the GUI

Click the **X button** (when open) or **💃 button** (when closed) to toggle GUI visibility.

---

## 🏗️ Project Structure

```
Roblox-Dance-Emote-GUI/
│
├── ServerScriptService/
│   └── ServerScript.lua              # Server-side DataStore handler
│                                     # Manages persistent favorites storage
│
├── StarterPlayer/
│   └── StarterPlayerScripts/
│       └── ClientScript.lua          # Client-side GUI & animation logic
│                                     # Handles UI, animations, and user input
│
├── README.md                         # Documentation (Dual Language)
└── LICENSE                           # MIT License
```

---

## 🔧 Technical Features

### Server-Side System

#### DataStore Integration
- **Persistent Storage** - All favorites saved permanently on Roblox servers
- **Player-Specific Data** - Each player has their own favorites storage
- **DataStore Version** - Uses versioned DataStore for future compatibility

#### Cache System
- **In-Memory Cache** - Reduces DataStore API calls
- **Instant Retrieval** - Favorites load instantly from cache
- **Auto-Update** - Cache updates on every change

#### Save Operations
- **Auto-Save** - Saves automatically on every favorite change
- **Async Operations** - Non-blocking save operations
- **Final Save** - Guaranteed save when player leaves
- **Error Recovery** - Graceful error handling with warnings

#### Remote Events
- **SaveFavorites** - Client → Server communication
- **LoadFavorites** - Server → Client data retrieval
- **Secure** - Server-side validation for data integrity

### Client-Side System

#### Instant Animation System
- **0ms Switch Delay** - Immediate animation switching
- **Preload System** - All animations preloaded in background
- **Memory Efficient** - Smart animation track management
- **Priority Override** - Animations play at highest priority

#### State Management
- **Active Animation Tracking** - Remembers currently playing animation
- **Tab State Persistence** - Maintains state across tab switches
- **Visual Feedback** - Active button highlighted in blue

#### UI/UX Features
- **Smooth Transitions** - TweenService for buttery smooth animations
- **Responsive Design** - Adapts to mobile and desktop screens
- **Touch & Click** - Full support for touch and mouse input
- **Hover Effects** - Interactive hover states on desktop

#### Performance Optimization
- **Lazy Loading** - Buttons created on-demand
- **Efficient Rendering** - Minimal UI updates
- **Frame Rate** - Maintains 60 FPS during animations
- **Memory Management** - Proper cleanup on character respawn

---

## 📱 Platform Support

| Platform | Status | Touch Support | Optimized UI |
|----------|--------|---------------|--------------|
| 💻 PC/Desktop | ✅ Full Support | Mouse | ✅ Yes |
| 📱 Mobile Phone | ✅ Full Support | Touch | ✅ Yes |
| 📲 Tablet | ✅ Full Support | Touch | ✅ Yes |
| 🎮 Console (Xbox) | ⚠️ Limited | Controller | ❌ No |
| 🕶️ VR | ❌ Not Supported | - | ❌ No |

### Platform-Specific Features

**Desktop (PC/Mac):**
- Hover effects on buttons
- Larger UI elements
- Mouse cursor interactions

**Mobile (Phone/Tablet):**
- Touch-optimized buttons
- Slightly smaller UI for more screen space
- Tap interactions
- Swipe-friendly scrolling

---

## 🎨 Customization Guide

### Changing Colors

Edit the `COLORS` table in **ClientScript.lua**:

```lua
local COLORS = {
    background = Color3.fromRGB(15, 15, 25),      -- Main background
    accent = Color3.fromRGB(100, 150, 255),       -- Primary color (blue)
    panel = Color3.fromRGB(25, 25, 40),           -- Panel background
    textPrimary = Color3.fromRGB(255, 255, 255),  -- Primary text
    stopButton = Color3.fromRGB(255, 80, 100),    -- Stop button color
    favoriteActive = Color3.fromRGB(255, 215, 0), -- Favorite star (gold)
    -- ... more colors
}
```

### Adding New Animations

Edit the `animations` table in **ClientScript.lua**:

```lua
local animations = {
    dances = {
        {name = "My Custom Dance", id = 123456789},
        -- Add your animations here
    },
    emotes = {
        {name = "My Custom Emote", id = 987654321},
        -- Add your emotes here
    }
}
```

**Finding Animation IDs:**
1. Go to Roblox website
2. Find the animation you want
3. Copy the number from URL: `roblox.com/library/[ID]/`
4. Add to animations table

### Adjusting UI Size

Modify `UI_CONFIG` in **ClientScript.lua**:

```lua
local UI_CONFIG = {
    panelSize = UDim2.new(0, 200, 0, 420),     -- Panel dimensions
    buttonHeight = 42,                          -- Animation button height
    toggleSize = UDim2.new(0, 35, 0, 35),      -- Toggle button size
    -- ... more settings
}
```

---

## 🐛 Troubleshooting

### Favorites Not Saving

**Symptom:** Favorites disappear after rejoin

**Solutions:**
1. ✅ Enable **API Services** in Game Settings → Security
2. ✅ Enable **Studio Access to API Services**
3. ✅ Check Output window for DataStore errors
4. ✅ Ensure you're testing in a published game (not just Play mode)
5. ✅ Wait a few seconds after favoriting before leaving

**Note:** DataStores don't work in Studio Play Solo mode. Publish your game and test online.

### Animations Not Playing

**Symptom:** Click animation but nothing happens

**Solutions:**
1. ✅ Verify Animation ID is correct
2. ✅ Check if animation is public/available
3. ✅ Ensure Humanoid exists in character
4. ✅ Look for error messages in Output
5. ✅ Check if animation is still available on Roblox

### GUI Not Appearing

**Symptom:** No GUI visible on screen

**Solutions:**
1. ✅ Verify scripts are in correct locations:
   - Server script in `ServerScriptService`
   - Client script in `StarterPlayer/StarterPlayerScripts`
2. ✅ Check if scripts are enabled (green checkmark)
3. ✅ Look for errors in Output window
4. ✅ Restart Roblox Studio
5. ✅ Check `ResetOnSpawn` is false in ScreenGui properties

### Performance Issues

**Symptom:** Lag or stuttering when using GUI

**Solutions:**
1. ✅ Close other running applications
2. ✅ Lower Roblox graphics settings
3. ✅ Reduce number of animations in database
4. ✅ Clear animation cache by restarting game
5. ✅ Check internet connection

### DataStore Quota Exceeded

**Symptom:** Error message about DataStore limits

**Solutions:**
1. ✅ Wait 60 seconds between rapid save operations
2. ✅ Don't spam favorite/unfavorite buttons
3. ✅ Error is temporary, data will save on next attempt
4. ✅ Check Roblox DataStore limits in documentation

---

## 📊 Version History

### v4.0 (Current) - Server-Side DataStore ⭐
**Release Date:** October 2025

**Major Changes:**
- ✨ **NEW:** Server-side persistent favorites
- ✨ **NEW:** DataStore integration for permanent storage
- ✨ **NEW:** Auto-sync system across sessions
- ✨ **NEW:** Never lose favorites data
- 🔧 Enhanced error handling and recovery
- 🔧 Improved save system with caching
- 🔧 Split into two scripts (Server + Client)
- 📝 Complete documentation overhaul

**Breaking Changes:**
- Now requires TWO scripts (server + client)
- Old LocalStorage favorites will not migrate
- API Services must be enabled

### v3.0 - Client-Side Storage
**Release Date:** 2024

**Features:**
- ⭐ Added Favorites system (LocalStorage)
- ⚡ Instant animation switching
- 🎨 Improved UI/UX design
- 📱 Better mobile optimization

**Limitations:**
- Favorites only saved locally
- Lost on game update or cache clear

### v2.0 - Performance Update
**Release Date:** 2023

**Features:**
- ⚡ Added animation preload system
- 📱 Mobile-specific optimizations
- 🎨 UI refinements
- 🐛 Bug fixes and stability improvements

### v1.0 - Initial Release
**Release Date:** 2023

**Features:**
- 🎭 Basic dance & emote GUI
- 📱 Mobile & PC support
- 💃 100+ animations
- 🎨 Simple UI design

---

## 💡 Tips & Best Practices

### For Users

1. **Organize Favorites** - Star your most-used animations for quick access
2. **Test Animations** - Try animations before favoriting
3. **Stay Updated** - Check for new animations regularly
4. **Report Issues** - Help improve the GUI by reporting bugs

### For Developers

1. **Backup Scripts** - Keep copies before making changes
2. **Test Locally** - Test changes in Studio before publishing
3. **Monitor Output** - Watch Output window for errors
4. **Read Documentation** - Review technical docs before customizing

---

## 👤 Credits

**Author:** [ItoRenz00](https://github.com/ItoRenz)

**Special Thanks:**
- Roblox Animation Community - For animation database
- Roblox Developers - For testing and feedback
- Players - For feature suggestions

**Technologies Used:**
- Roblox Luau
- DataStoreService
- TweenService
- RemoteEvents

---

## 📄 License

```
MIT License

Copyright (c) 2025 ItoRenz00

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

**What This Means:**
- ✅ Free to use in any project
- ✅ Free to modify and customize
- ✅ Free to distribute
- ✅ Can be used commercially
- ❌ No warranty provided
- ℹ️ Must include copyright notice

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Reporting Bugs

1. Check if bug already reported in Issues
2. Create new issue with clear description
3. Include steps to reproduce
4. Add screenshots/videos if possible
5. Mention your platform (PC/Mobile)

### Suggesting Features

1. Open new issue with "Feature Request" label
2. Describe feature in detail
3. Explain use case and benefits
4. Be open to discussion and feedback

### Adding Animations

1. Find animation ID on Roblox
2. Test animation works in-game
3. Fork repository
4. Add to animations table
5. Submit pull request with:
   - Animation name
   - Animation ID
   - Category (dance/emote)
   - Brief description

### Code Contributions

1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Test thoroughly
5. Commit (`git commit -m 'Add AmazingFeature'`)
6. Push to branch (`git push origin feature/AmazingFeature`)
7. Open Pull Request

**Code Style:**
- Follow existing code structure
- Add comments for complex logic
- Test on both PC and Mobile
- Ensure no performance degradation

---

## 📞 Support & Community

### Getting Help

**GitHub Issues:**
- Bug reports: [Create Issue](https://github.com/ItoRenz/Roblox-Dance-Emote-Gui/issues)
- Feature requests: [Create Issue](https://github.com/ItoRenz/Roblox-Dance-Emote-Gui/issues)
- Questions: [Discussions](https://github.com/ItoRenz/Roblox-Dance-Emote-Gui/discussions)

**Roblox:**
- Profile: [ItoRenz00](https://www.roblox.com/users/ItoRenz00)
- Messages: Send Roblox DM for direct support

### Community

**Discord Server:** Coming soon...

**Social Media:**
- GitHub: [@ItoRenz](https://github.com/ItoRenz)

### FAQ

**Q: Does this work in all games?**
A: Yes, as long as you have permission to add scripts.

**Q: Can I use this in my game?**
A: Yes! It's free and open-source under MIT License.

**Q: Will my favorites sync between different games?**
A: No, each game has separate DataStore. Favorites are per-game.

**Q: Can I monetize a game using this GUI?**
A: Yes, MIT License allows commercial use.

**Q: How often is this updated?**
A: Updates released as needed for new features and bug fixes.

---

## 🔮 Future Plans

### Planned Features

- 🎵 **Music Sync** - Animations synced with in-game music
- 👥 **Group Dances** - Synchronized multi-player animations
- 🎨 **Themes** - Multiple color themes
- 🔊 **Sound Effects** - Optional UI sounds
- 📊 **Statistics** - Track most-used animations
- 🏆 **Achievements** - Unlock system for animations
- 🌐 **Cloud Sync** - Cross-game favorites sync
- 🎮 **Controller Support** - Full Xbox controller support

### Under Consideration

- Custom animation upload
- Animation speed control
- Animation mixing
- Marketplace integration
- VR support

**Want to see a feature?** Open a feature request!

---

## 🌟 Showcase

Using this GUI in your game? Let us know! We'd love to feature your game here.

**Featured Games:**
- *Your game could be here!*

**Submit your game:**
1. Open an issue with "Showcase" label
2. Include game name and link
3. Add screenshot (optional)

---

<div align="center">

## ⭐ Star This Project!

If you find this project useful, please consider giving it a star on GitHub!

**Made with ❤️ by ItoRenz00**

[⬆ Back to Top](#-roblox-dance--emote-gui-v40)

</div>
