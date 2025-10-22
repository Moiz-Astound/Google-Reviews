# Google Reviews Dashboard

A comprehensive analytics dashboard for tracking and visualizing Google Reviews performance across multiple store locations and regions.

## Overview

This project provides an interactive web-based dashboard for monitoring Google Reviews ratings across 45+ locations spanning 7 regions from January 2020 to October 2025. The dashboard features split-table layouts for easy data navigation and interactive Chart.js graphs for visualizing rating trends over time.

## Features

### Main Dashboard (index.html)
- Split-table design with fixed location columns, horizontally scrollable monthly data, and fixed competitor columns
- 70 months of historical rating data (January 2020 - October 2025)
- Color-coded rating system:
  - Excellent: 4.0+ (green)
  - Good: 3.0-3.9 (gray)
  - Fair: 2.5-2.9 (yellow)
  - Poor: Below 2.5 (red)
- Regional organization with 7 regions:
  - Texas (11 locations)
  - Illiana (2 locations)
  - West Coast (21 locations)
  - Massachusetts (3 locations)
  - DC / Maryland (2 locations)
  - Pennsylvania / New Jersey (3 locations)
  - New York (3 locations)
- Competitor comparison data (XFINITY, Spectrum, Verizon, AT&T)
- Clickable region headers with hover animations
- Regional average calculations

### Interactive Graphs
- Dedicated graph page for each region
- Interactive line charts powered by Chart.js
- Toggle individual locations on/off via checkboxes
- Toggle average line visibility
- Select All / Deselect All functionality
- 70 months of trend data visualization
- Y-axis range: 0.0 to 5.0
- Disabled legend click-to-hide functionality (checkbox control only)

## Project Structure

```
november/
├── index.html                          # Main dashboard
├── graph_texas.html                    # Texas region graph
├── graph_illiana.html                  # Illiana region graph
├── graph_west.html                     # West Coast region graph
├── graph_massachusetts.html            # Massachusetts region graph
├── graph_dc_maryland.html              # DC/Maryland region graph
├── graph_pennsylvania.html             # Pennsylvania/New Jersey region graph
├── graph_newyork.html                  # New York region graph
├── update_graphs.py                    # Python script to update graph data
├── generate_dashboard_v2.py            # Python script to generate dashboard
├── generate_full_dashboard.py          # Alternative dashboard generator
└── Google Reviews by Store Month over Month 10_1_2025(Google Overall Ratings).csv
```

## Technology Stack

- HTML5
- CSS3 (with flexbox and CSS Grid)
- JavaScript (ES6+)
- Chart.js for data visualization
- Python 3 for data processing and HTML generation

## Data Source

The dashboard pulls data from a CSV file containing:
- Store locations (address, city, state, zip)
- Monthly Google Reviews ratings (70 months)
- Competitor ratings
- Regional averages

### CSV Column Structure
- Columns 6-65: January 2020 - December 2024 (60 months)
- Columns 66-70: January 2025 - May 2025 (5 months)
- Column 73: June 2025 (1 month)
- Columns 76-79: July 2025 - October 2025 (4 months)
- Columns 81-84: Competitor data (XFINITY, Spectrum, Verizon, AT&T)

## Setup and Usage

### Prerequisites
- Python 3.x
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Viewing the Dashboard
1. Clone this repository
2. Open `index.html` in a web browser
3. Click on any region header to view interactive graphs
4. Use the "Back to Dashboard" link to return to the main view

### Updating Data
1. Update the CSV file with new rating data
2. Run the Python scripts to regenerate HTML files:
   ```bash
   python3 generate_dashboard_v2.py
   python3 update_graphs.py
   ```
3. Refresh the browser to see updated data

## Design Features

### Split-Table Layout
- **Left Fixed Section**: Location information (Address, City, State, Zip)
- **Middle Scrollable Section**: 70 months of rating data
- **Right Fixed Section**: Competitor comparison data

### Column Widths
- Address: 180px - 250px (flexible)
- City: 120px - 180px (flexible)
- State: 50px (fixed)
- Zip: 70px (fixed)
- Competitors: 90px each (fixed)

### Color Scheme
- Primary gradient: Purple to violet (#667eea to #764ba2)
- Hover effects: Lighter gradient (#7688f0 to #8657b0)
- Interactive animations: 0.3s ease transitions

## Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Performance Optimization

- Efficient table rendering with flexbox layout
- Row height synchronization across split tables
- Smooth scrolling with custom scrollbar styling
- Optimized Chart.js configurations for large datasets

## Credits

Created by Moiz Uddin

## License

This project is proprietary. All rights reserved.

## Future Enhancements

- Export data to CSV/Excel
- Date range filtering
- Additional competitor analysis
- Mobile-responsive design improvements
- Real-time data integration via API
