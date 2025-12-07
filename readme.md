# Semiglutide Simulator 💊

A comprehensive web-based simulator for tracking and understanding GLP-1 medication (Semiglutide/Ozempic) effects on appetite, energy, weight loss, and overall treatment progression.

## 🌟 Features

### Core Functionality
- **12-Week Treatment Simulation**: Track your GLP-1 medication journey week by week
- **Dose Escalation**: Realistic dose progression (0.25mg → 0.5mg → 1.0mg → 2.0mg)
- **Appetite Suppression Tracking**: Real-time appetite level monitoring with GLP-1 effects
- **Hunger Visualization**: Modern visual representation of hunger levels with color-coded indicators
- **Weight Loss Tracking**: Monitor cumulative weight loss against your personal goals

### Vital Stats Monitoring
- **Appetite Level**: Tracks GLP-1 appetite suppression effects
- **Energy Status**: Monitors energy fluctuations throughout treatment
- **Nausea Tracking**: Records common side effects, especially during dose increases
- **Cravings Intensity**: Measures cravings that decrease over time with medication effectiveness

### Interactive Features
- **Meal Logging**: Record meals and track post-meal hunger reduction
- **Time Simulation**: Advance time (+1 hour, +4 hours, +1 day) to see realistic body responses
- **Craving Checks**: Test your appetite suppression at any time
- **Meal History**: Keep a record of recent meals with hunger before/after metrics
- **Thought Chain**: Real-time event log documenting treatment journey and side effects

### Customization
- **Settings Panel**: Adjust dose, week, weight goals, and current progress
- **Supplement Scheduling**: Add and track supplements with specific times
- **Dark Mode**: Easy-on-the-eyes dark theme toggle
- **Time Controls**: Optional time simulation controls for advanced tracking

### Motivational Features
- **50+ Motivational Quotes**: Random health and wellness quotes on each session
- **Treatment Progress Dots**: Visual 12-week treatment progress indicator
- **Persistent Data**: All progress saved to browser localStorage

## 📋 Available Versions

The project includes multiple implementations:

| File | Style | Features |
|------|-------|----------|
| `semiglutide_optimized.html` | Modern responsive | Best overall, dark mode, supplements |
| `semiglutide_final.html` | Clean modern | Desktop-focused, comprehensive |
| `semiglutide_modern.html` | Polished modern | Feature-rich desktop version |
| `semiglutide.html` | Retro CRT | Retro '80s aesthetics (fun) |

**Recommended**: Start with `semiglutide_optimized.html` for best mobile and desktop experience.

## 🚀 Quick Start

### Opening the Simulator

1. Download one of the HTML files
2. Double-click to open in your web browser (no installation needed)
3. Or deploy to any web server

```bash
# Optional: Run a local server
python -m http.server 8000
# Then visit http://localhost:8000/semiglutide_optimized.html
```

### First Time Usage

1. **Settings** appears automatically on first load
2. Configure your starting dose and weight loss goal
3. Click "Save Settings"
4. Start logging meals and tracking your journey!

## 📊 How It Works

### Realistic Simulation
- **Hourly Updates**: Effects change throughout the day
- **Meal Impact**: Hunger reduces significantly after eating
- **Dose Escalation Effects**: Increased side effects at weeks 5, 9, and 13
- **Time-Based Hunger**: Morning/afternoon/evening appetite patterns
- **Medication Effectiveness**: Cravings decrease over time as medication builds up

### Key Metrics

**Hunger Level (0-100%)**
- ≤20%: Very Satisfied (green)
- 20-40%: Satisfied (blue)
- 40-60%: Slightly Hungry (yellow)
- 60-80%: Hungry (orange)
- >80%: Very Hungry (red)

**Appetite States**
- Very Low: Medication is highly effective
- Low: Standard GLP-1 suppression
- Moderate: Less suppression, possible dose adjustment needed

**Energy Patterns**
- Stable: Normal energy levels
- Declining: Post-meal energy drop
- Low: Significant fatigue (especially weeks 1-2)

## 🎮 Usage Guide

### Main Controls

| Action | Effect |
|--------|--------|
| **Eat Meal** | Reduces hunger by 15%, logs meal in history |
| **Check Cravings** | Tests current craving intensity |
| **+1/+4/+24 Hour** | Advances time, simulates body responses |
| **Settings** | Customize dose, week, goals, supplements |
| **Dark Mode** | Toggle between light and dark themes |

### Settings Options

- **Starting Dose**: 0.25mg - 2.0mg
- **Current Week**: 1 - 24 (extends beyond standard 12-week protocol)
- **Weight Loss Goal**: Your target weight loss in kg
- **Current Weight Loss**: Track actual progress
- **Enable Time Controls**: Show/hide time simulation buttons
- **Supplements**: Add medications or vitamins to track

## 💾 Data Persistence

All data is saved automatically to your browser's localStorage:
- Current treatment week and dose
- Weight loss progress
- Meal history
- Event log entries
- Settings preferences
- Time of day simulation
- Dark mode preference

**Clear Data**: Settings are persistent. To reset, clear browser cache/localStorage.

## 📱 Device Support

- ✅ Desktop browsers (Chrome, Firefox, Safari, Edge)
- ✅ Tablets (iPad, Android tablets)
- ✅ Mobile phones (responsive design in optimized version)
- ⚠️ Best experience: Desktop or tablet

## 🔧 Technical Details

### Technology Stack
- **HTML5**: Semantic markup
- **CSS3**: Modern styling with Tailwind CSS
- **Vanilla JavaScript**: No external dependencies (except Tailwind)
- **LocalStorage API**: Client-side data persistence
- **No Backend Required**: Runs entirely in browser

### Browser Requirements
- ES6 JavaScript support
- localStorage enabled
- Modern CSS Grid/Flexbox support
- Recommended: Latest browser versions

## 📚 Understanding GLP-1 Effects

This simulator models realistic GLP-1 medication effects:

### Week 1-4 (0.25mg)
- Appetite suppression begins
- Side effects: Mild nausea possible
- Hunger reduction: ~15-20% baseline

### Week 5-8 (0.5mg)
- Significant appetite suppression
- Post-meal satiety increases
- Cravings noticeably reduced
- Side effects peak at week 5

### Week 9-12 (1.0mg)
- Strong appetite control
- Consistent energy levels
- Cravings minimal
- Side effects stabilize

### Week 13+ (2.0mg)
- Maximum appetite suppression
- Long-term sustainability mode
- Minimal side effects
- Stable weight loss trajectory

## ⚙️ Customization

### Modifying Cravings
Edit the `initializeCravings()` method in the JavaScript section:

```javascript
this.cravings = [
    { food: "Pizza", intensity: 0.6, time: "evening" },
    { food: "Chocolate", intensity: 0.5, time: "night" },
    // Add more...
];
```

### Changing Motivational Quotes
Modify the `motivationalQuotes` array in the script section.

### Adjusting Simulation Speed
Change the intervals in `startSimulation()`:
- Update display: every 1000ms
- Auto-save: every 30000ms (30 seconds)
- Simulate effects: every 10000ms (10 seconds)

## 📝 Notes & Disclaimers

⚠️ **This is a simulation tool for educational purposes only**

- Not a medical device or replacement for professional medical advice
- Consult your healthcare provider about actual GLP-1 treatment
- Weight loss and side effects vary greatly between individuals
- This simulator uses generalized, average-case scenarios
- Always follow your doctor's dosing schedule and recommendations

## 🤝 Contributing

To suggest improvements:
1. Identify the issue or feature
2. Test with the latest browser
3. Document the expected behavior
4. Share suggestions via comments in the code

## 📄 License

This simulator is provided as-is for educational and personal use.

## 🙋 Support

**Common Issues:**

**Q: Data not saving?**
- A: Check if localStorage is enabled in browser settings

**Q: Time controls not showing?**
- A: Enable them in Settings → "Enable Time Controls"

**Q: Dark mode not working?**
- A: Try refreshing the page or clearing browser cache

**Q: Hunger not decreasing after meals?**
- A: Ensure week is not too high (medication becomes very effective)

---

**Version**: 2.0  
**Last Updated**: 2025  
**Best Experience**: `semiglutide_optimized.html`

*Made with ❤️ for health-conscious individuals tracking their GLP-1 journey.*