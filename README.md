# Terminal Dashboard - Real-time System Monitor

A comprehensive terminal-style system monitoring dashboard with real-time metrics.

## 🚀 Features

- **Real-time System Metrics**: CPU, Memory, Storage, Network, Temperature monitoring
- **Live Charts**: Animated visualizations for system trends
- **Terminal Aesthetics**: Matrix rain effect, terminal styling, ASCII art
- **Responsive Design**: Works on desktop and mobile devices
- **Dual Mode**: Works with real backend OR falls back to simulated data

## 📁 Project Structure

```
terminal-dashboard/
├── index.html          # Frontend dashboard
├── server.js            # Node.js backend for real metrics
├── package.json         # Node.js dependencies
└── README.md           # This file
```

## 🛠️ Setup & Installation

### For Real System Metrics (Recommended)

1. **Install Dependencies**:
   ```bash
   npm install
   ```

2. **Start Backend Server**:
   ```bash
   npm start
   ```

3. **Open Dashboard**:
   Navigate to `http://localhost:3001` in your browser

### For Static Deployment

1. Deploy `index.html` to any static hosting (Netlify, Vercel, GitHub Pages)
2. Dashboard will run with **simulated data** (no backend needed)

## 🌐 API Endpoints

When running locally, the backend provides:

- `GET /api/metrics` - All system metrics
- `GET /api/cpu` - CPU information
- `GET /api/memory` - Memory usage
- `GET /api/storage` - Disk space
- `GET /api/network` - Network statistics
- `GET /api/temperature` - System temperature
- `GET /api/system` - System information

## 📊 Data Sources

### Real Metrics (Linux/Unix):
- **CPU**: `/proc/stat`, `/proc/cpuinfo`
- **Memory**: `/proc/meminfo`
- **Storage**: `df -h` command
- **Network**: `/proc/net/dev`
- **Temperature**: `/sys/class/thermal/thermal_zone*/temp`
- **System**: `os` module, `ps`, `who` commands

### Fallback Mode:
- Simulated realistic data for static hosting

## 🎨 Visual Features

- Matrix rain background effect
- Color-coded progress bars (green/yellow/orange/red)
- Real-time mini charts
- Terminal-style ASCII art displays
- Animated status indicators
- Responsive grid layout

## 🚀 Deployment

### Local Development:
```bash
npm start    # Starts server on http://localhost:3001
```

### Static Hosting:
Deploy just the `index.html` file to:
- Netlify
- Vercel  
- GitHub Pages
- Any static hosting service

## 🔧 Customization

- Edit `server.js` to modify metric collection
- Edit `index.html` to adjust UI/styling
- Add new API endpoints in `server.js`
- Extend frontend charts and widgets

## 📱 Browser Support

- Chrome/Edge (Full features)
- Firefox (Full features)  
- Safari (Most features)
- Mobile browsers (Responsive)

## 🛡️ Security

- CORS enabled for development
- No external dependencies in frontend
- Server runs on localhost by default
- Input sanitization for system commands

## 📈 Performance

- Updates every 2 seconds
- Efficient canvas rendering
- Minimal resource usage
- Graceful error handling

## 🤝 Contributing

1. Fork the repository
2. Create feature branch
3. Submit pull request

## 📄 License

MIT License - see LICENSE file for details

---

**Note**: On static hosting deployments, the dashboard uses simulated data. Run locally with `npm start` for real system metrics.