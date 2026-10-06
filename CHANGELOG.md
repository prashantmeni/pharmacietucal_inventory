# Changelog

All notable changes to the Pharmacy Inventory Management system will be documented in this file.

## [1.0.0] - 2025-01-06

### Added
- Initial production release
- Dashboard with inventory overview and metrics
- Inventory management page with search and filtering
- Add stock page with manual entry and JSON import
- LocalStorage-based data persistence
- Responsive UI for desktop and mobile
- Sample data seeding
- Professional documentation and README
- GitHub Pages deployment configuration
- Pharmaceutical theme with green color scheme
- Real-time cross-tab synchronization

### Features
- Dashboard metrics (total SKUs, stock units, expired items, expiry risk)
- Inventory table with search and filtering by expiry status
- Add/update/delete stock entries
- Record sales with automatic FIFO expiry management
- Expiry tracking with visual badges
- Low-stock indicators
- Chart.js gauges for data visualization
- Fully responsive mobile-friendly design
- Offline-first functionality
- No backend required (static site)

### Security
- XSS protection on all user inputs
- Data stored locally in browser
- No external API calls
- No tracking or analytics

### Performance
- Lightweight (~50KB total)
- No external dependencies (except Chart.js from CDN)
- Instant load time
- Smooth animations and transitions

## Future Releases

### [1.1.0] - Planned
- CSV export functionality
- Data backup and restore
- Multiple inventory locations
- Category-based organization
- Barcode/QR code support

### [2.0.0] - Future
- Cloud sync option
- User authentication
- Multi-user support
- Database backend
- Advanced reporting
