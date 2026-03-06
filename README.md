# Chronos - Global Meeting Planner

A sleek, modern web application for planning meetings across multiple time zones. Built with vanilla HTML, CSS, and JavaScript — no frameworks required!

## 🔗 Live Demo

**[Try Chronos Live →](https://najiatislam.github.io/chronos)**


## 📸 Screenshots

![Dashboard](assets/ss1.jpeg)
![Timeline Comparison](assets/ss2.jpeg)
![World Clock](assets/ss3.jpeg)

## ✨ Features

### Core Meeting Planner
- **Timeline Comparison** - Visual 24-hour timeline showing working hours for each city
- **Smart Overlap Detection** - Automatically highlights overlapping working hours
- **Multiple Meeting Slots** - Plan up to 3 different meeting options simultaneously
- **Drag & Drop** - Click and drag to set meeting times, resize to adjust duration
- **Week View** - Switch between day and week views for better planning

### World Clock Dashboard
- Pin your favorite cities to track their current time at a glance
- Real-time updates with live seconds
- Date display for each timezone

### Meeting Countdown Timer
- Add upcoming meetings with countdown timers
- Visual urgency indicators (urgent, soon, normal)
- Persistent storage - meetings survive page refreshes

### Team Directory
- Manage your global team members
- Track each member's timezone and working hours
- Live availability status (Available, Away, Busy)
- Avatar with initials

### Holiday Calendar
- View public holidays for 8 countries:
  - 🇺🇸 United States
  - 🇬🇧 United Kingdom
  - 🇩🇪 Germany
  - 🇫🇷 France
  - 🇯🇵 Japan
  - 🇦🇺 Australia
  - 🇨🇦 Canada
  - 🇮🇳 India
- Past holidays appear faded
- Filter by year (2024-2025)

### Meeting Invite Generator
- Create formatted meeting invites with timezone conversions
- Add multiple recipient timezones
- Copy-ready output for email/chat

### Availability Windows
- Interactive weekly grid to mark your availability
- Add multiple people
- Find overlapping availability across team members

### 🔗 Shareable Meeting Links
Share meeting setups with a simple URL! When someone opens the link, cities and meeting time auto-load.

**Example URLs:**
```
?cities=London,Tokyo,New York&meeting=14:00
?cities=Dhaka,Berlin&meeting=09:30&duration=2
?cities=Sydney,London,Mumbai&date=2026-03-15&meeting=10:00
```

**How to use:**
1. Select cities and drag a meeting time on the timeline
2. Click the **Share** button (link icon)
3. Copy and share the generated URL

### Additional Features
- **Quick Time Converter** - Convert any time between selected cities
- **Saved Groups** - Save frequently used city combinations
- **Calendar Export** - Export to .ics files for calendar apps
- **Dark/Light Theme** - Toggle between elegant dark and light modes
- **Keyboard Shortcuts** - Power user controls for efficiency
- **Responsive Design** - Works on desktop and mobile devices

## 🚀 Getting Started

### Option 1: Open Directly
Simply open `index.html` in your web browser. No server required!

### Option 2: Use a Local Server
For the best experience, use a local development server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `←` `→` | Move meeting slot by 30 minutes |
| `Shift` + `←` `→` | Resize meeting slot |
| `1` `2` `3` | Switch between meeting slots |
| `D` | Toggle Day/Week view |

## 🎨 Customization

### Adding Cities
Edit the `cities` array in `js/app.js` to add or modify cities:

```javascript
{ name: "New York", country: "USA", timezone: "EST", offset: -5, dstOffset: -4 }
```

### Adding Holidays
Add holidays to the `holidays` object in `js/app.js`:

```javascript
holidays['XX'] = [
    { date: '01-01', name: "New Year's Day", type: 'National' },
    // ...
];
```

### Theme Colors
Modify CSS variables in `css/styles.css` to customize the color scheme:

```css
:root {
    --accent-primary: #6366f1;
    --accent-secondary: #10b981;
    /* ... */
}
```

## 📁 Project Structure

```
chronos/
├── index.html          # Main HTML file
├── css/
│   └── styles.css      # All styles including dark/light themes
├── js/
│   └── app.js          # Application logic and city data
├── assets/
│   └── preview.png     # Screenshot for README
├── README.md           # This file
└── LICENSE             # MIT License
```

## 🌐 Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

## 💾 Data Storage

All user data is stored in the browser's `localStorage`:
- `tzGroups` - Saved city groups
- `tzTheme` - Theme preference
- `worldClocks` - Pinned world clock cities
- `meetings` - Scheduled meetings for countdown
- `teamMembers` - Team directory entries
- `availabilityPersons` - Availability grid data

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Inter Font](https://fonts.google.com/specimen/Inter) by Rasmus Andersson
- Timezone data based on standard UTC offsets
- Holiday data compiled from public sources

---

Made with ❤️ for remote teams everywhere
