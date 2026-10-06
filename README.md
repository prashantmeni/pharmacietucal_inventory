# 💊 Pharmacy Inventory Management System

[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue)](https://prashantmeni.github.io/pharmacietucal_inventory/html/)
[![License](https://img.shields.io/badge/License-MIT-green)](#license)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-success)](#status)

A modern, lightweight inventory management dashboard for pharmaceutical stock tracking. Built as a static web application and optimized for GitHub Pages deployment.

## 🚀 Live Demo

**[Open Application →](https://prashantmeni.github.io/pharmacietucal_inventory/html/)**

## ✨ Features

### Dashboard
- 📊 Real-time inventory overview with gauges
- 📈 Total stock units tracking
- 🆔 Total SKUs (Stock Keeping Units) count
- ⚠️ Expired items counter
- 🔴 Expiry risk monitoring

### Inventory Management
- 🔍 Search and filter medicines
- 📅 Filter by expiry status (OK, ≤30d, ≤90d, Expired)
- ➕ Add new stock entries
- ✏️ Update stock quantities and expiry dates
- 🛒 Record sales
- 🗑️ Delete stock entries
- 💾 Local browser storage (no server required)

### User Experience
- 📱 Fully responsive design (desktop, tablet, mobile)
- 🎨 Modern, professional UI with green pharmaceutical theme
- ⚡ Fast and lightweight
- 🔄 Real-time updates across tabs
- 🌐 Works offline

## 🏗️ Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
- **Charts:** Chart.js 4.4.1
- **Storage:** Browser LocalStorage
- **Hosting:** GitHub Pages
- **Fonts:** Google Fonts (Inter, Poppins)

## 📦 Project Structure

```
pharmacietucal_inventory/
├── .github/
│   └── workflows/
│       └── jekyll-gh-pages.yml      # GitHub Pages deployment
├── html/
│   ├── index.html                   # Dashboard page
│   ├── inventory.html               # Inventory management
│   ├── add-stock.html               # Add/import stock
│   └── default-data.js              # Default seed data
├── .gitignore                       # Git ignore rules
├── _config.yml                      # Jekyll configuration
├── index.html                       # Root redirect
├── README.md                        # This file
└── package-lock.json                # Dependencies lock
```

## 🎯 How It Works

1. **Data Storage:** All inventory data is stored in browser's LocalStorage with key `pharmacy_inventory_v1`
2. **First Launch:** If localStorage is empty, the app seeds with default sample data
3. **Offline First:** Application works completely offline with full functionality
4. **Cross-Tab Sync:** Changes in one tab automatically update others via storage events
5. **No Backend Required:** Static HTML/JS/CSS – deploy anywhere, no server needed

## 📋 Sample Data

The application comes with pre-loaded sample medicines:
- Paracetamol 500mg
- Amoxicillin 250mg
- Cetrizine 10mg
- Ibuprofen 200mg
- Vitamin C 1000mg
- Amlodipine 5mg

## 🚀 Getting Started

### Option 1: Use Live Version
Simply open the [live application](https://prashantmeni.github.io/pharmacietucal_inventory/html/) in your browser.

### Option 2: Local Development

1. Clone the repository:
```bash
git clone https://github.com/prashantmeni/pharmacietucal_inventory.git
cd pharmacietucal_inventory
```

2. Serve locally with Python:
```bash
python -m http.server 8000
```

3. Open in browser:
```
http://localhost:8000/html/index.html
```

### Option 3: GitHub Pages
The repository is already configured for GitHub Pages. Just enable it in Settings → Pages.

## 📖 Usage Guide

### Dashboard
1. Open the application
2. View real-time metrics in the inventory overview
3. Check critical stock items at a glance

### Add Stock
1. Click "➕ Add Stock" in the navigation
2. Fill in medicine details (name, strength, quantity, expiry)
3. Click "Add Stock" to save
4. Or import from JSON file for bulk operations

### Manage Inventory
1. Click "📦 Inventory" to view all items
2. Search by medicine name or strength
3. Filter by expiry status
4. Click "Save" to update quantities/dates
5. Click "Sell" to record sales
6. Click "Delete" to remove entries

### View Dashboard
1. Click "🏠 Dashboard" to return to overview
2. See updated metrics and top-priority items

## ⚙️ Configuration

### Default Data (html/default-data.js)
Modify the `DEFAULT_PHARMACY_INVENTORY` array to customize seed data:

```javascript
window.DEFAULT_PHARMACY_INVENTORY = [
  { id: 'demo-1', name: 'Medicine Name', strength: '500mg', quantity: 100, expiryDate: '2027-01-15' },
  // Add more items...
];
```

### Brand Customization
Edit the following files to rebrand:
- `html/index.html` (line 6, 566: title and logo)
- `html/inventory.html` (line 6, 384: title and logo)
- `html/add-stock.html` (line 6, 384: title and logo)

## 🔒 Data Privacy

- ✅ All data stays in your browser
- ✅ No server-side storage
- ✅ No tracking or analytics
- ✅ No external API calls
- ⚠️ Data persists only in browser (clears if localStorage is cleared)

## 📱 Browser Support

- ✅ Chrome/Chromium (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers

## 🎨 Design System

### Color Palette
- Primary Green: `#1e7e34`
- Success: `#10b981`
- Warning: `#f59e0b`
- Danger: `#dc2626`
- Text Dark: `#0f172a`
- Background: `#f0f9ff`

### Typography
- Headings: Poppins (600, 700, 800)
- Body: Inter (400, 500, 600, 700)

## 🔄 Export/Import

### Export Data
Access your data via browser console:
```javascript
JSON.stringify(JSON.parse(localStorage.getItem('pharmacy_inventory_v1')))
```

### Import Data
Use the "Import from JSON" feature in Add Stock page with this format:
```json
[
  { "name": "Paracetamol", "strength": "500mg", "quantity": 100, "expiryDate": "2027-01-15" },
  { "name": "Ibuprofen", "strength": "200mg", "quantity": 50, "expiryDate": "2027-02-20" }
]
```

## 📊 Roadmap

- [ ] CSV export functionality
- [ ] Category and supplier tracking
- [ ] Barcode/QR code support
- [ ] Cloud sync option
- [ ] User authentication
- [ ] Multi-location support
- [ ] Advanced reporting
- [ ] Database backend option

## 🐛 Known Limitations

1. Data is browser-specific (not synced across devices)
2. Data clears if browser cache is cleared
3. Maximum storage depends on browser (typically 5-10MB)
4. No built-in backup mechanism

## 💡 Tips & Tricks

1. **Bulk Import:** Use JSON import in Add Stock page to quickly populate database
2. **Data Backup:** Regularly export your data using browser console
3. **Cross-Device:** Keep this window open for real-time updates
4. **Mobile Use:** Save to home screen for app-like experience

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests
- Improve documentation

## 📄 License

MIT License - feel free to use this in personal, educational, or commercial projects.

## 👨‍💻 Author

**Prashant Meni**
- GitHub: [@prashantmeni](https://github.com/prashantmeni)
- Portfolio: [prashantmeni.github.io](https://prashantmeni.github.io)

## 🙏 Acknowledgments

- Chart.js for beautiful data visualization
- Google Fonts for typography
- GitHub Pages for free hosting

## 📞 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Check existing documentation
- Review sample data configuration

---

**Made with ❤️ for better pharmacy management**

**[🚀 Launch Application](https://prashantmeni.github.io/pharmacietucal_inventory/html/)**
