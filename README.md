# Capstone Team Finder

A web-based platform designed to help students find and connect with capstone project teams. This application displays team listings from a Google Sheet and allows users to filter teams by category and contact potential teammates.

**🚀 Live URL**: https://tejaatexploring.github.io/CapstoneTeamFinder/main.html

## Overview

**Capstone Team Finder** is a student collaboration tool that streamlines the process of finding and joining capstone project teams. It leverages Google Sheets for data management and provides a clean, responsive interface for browsing team postings.

Currently deployed on **GitHub Pages** was actively used by college students to form their capstone project teams!

## Features

✨ **Key Features:**
- **Team Browsing**: Display all available capstone teams with member information
- **Category Filtering**: Filter teams by student categories (Category A, B, C)
- **Infinite Scroll**: Load teams progressively as you scroll down the page
- **Team Details**: View team members, SRNs, project domains, and contact information
- **Post New Team**: Quick link to Google Forms for posting new teams
- **Delete Teams**: Option to remove team posts via Google Forms
- **Responsive Design**: Fully optimized for mobile, tablet, and desktop devices
- **Analytics Tracking**: Built-in Google Analytics integration
- **Loading States**: User-friendly loading spinner while data is fetched

## Project Structure

```
CapstoneTeamFinder/
├── main.html           # Main HTML page with interactive functionality
├── Stylesheet1.css     # Complete styling and responsive design
└── README.md           # Project documentation
```

## File Descriptions

### main.html
The main application file containing:
- **Header & Navigation**: Title and action buttons
- **Filter Controls**: Dropdown to filter teams by category
- **Data Display**: Card-based layout for team listings
- **JavaScript Logic**:
  - Fetches data from Google Sheets API (OpenSheet)
  - Implements category filtering
  - Handles infinite scroll loading
  - Extracts and displays team member information
  - Manages contact information display

**Key Variables:**
- `SHEET_URL`: Google Sheets endpoint for fetching team data
- `allData`: Stores all teams from the sheet
- `filteredData`: Stores filtered team results
- `batchSize`: Number of teams loaded per scroll (20)

**Main Functions:**
- `extractCategories()`: Extracts team categories from sheet data
- `renderCard()`: Creates and displays individual team cards
- `renderNextBatch()`: Loads next batch of teams on scroll

### Stylesheet1.css
Complete styling including:
- **Layout**: Flexbox-based card grid system
- **Colors**: Professional color scheme with category-based badges
  - Category A (Red): `#ff6b6b`
  - Category B (Teal): `#4ecdc4`
  - Category C (Orange): `#ffa502`
- **Animations**: Loading spinner with smooth rotation
- **Responsive Breakpoints**: 
  - Tablets (≤768px)
  - Mobile phones (≤400px)
- **Hover Effects**: Card elevation and shadow on hover
- **Typography**: Google Fonts (Poppins, 400 & 600 weights)

## How to Use

1. **Open the Application**
   - Open `main.html` in a web browser

2. **Browse Teams**
   - The page automatically loads and displays available teams
   - Teams appear as cards with member details and contact information

3. **Filter by Category**
   - Use the dropdown menu to filter teams by category
   - Select "Show All Categories" to view all teams

4. **Scroll to Load More**
   - Scroll down to automatically load more team listings
   - Teams load in batches of 20 for better performance

5. **Post a Team**
   - Click "➕ Post a New Team" button to open the Google Form
   - Fill in your team details and submit

6. **Delete a Team**
   - Click "🗑️ Delete My Team Post" button to open the deletion form
   - Follow instructions to remove your team posting

## Data Source

The application fetches team data from a Google Sheet via the **OpenSheet API**:
- **API Endpoint**: `https://opensheet.elk.sh/1CYF6BsqAAN3ThqjgyPxPhLJL23Uf1TBeLL5ZEtDDjQA/posts_public`
- **Data Format**: JSON array of team objects

### Expected Data Fields
- `Name 1`, `Name 2`, `Name 3`: Team member names
- `SRN 1`, `SRN 2`, `SRN 3`: Student Registration Numbers
- `Category of Student Needed - 01/1/02/2`: Team category requirements
- `Mention the Domain Your team is working on`: Project domain description
- `Primary Contact number/email`: Primary contact information
- `Secondary Contact number/email`: Secondary contact information

## Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Data Source**: Google Sheets + OpenSheet API
- **Fonts**: Google Fonts (Poppins)
- **Analytics**: Google Analytics
- **Responsive Design**: Mobile-first CSS media queries

## Features in Detail

### Infinite Scroll Loading
- Teams load progressively (20 per batch) as users scroll
- Improves page performance and reduces initial load time

### Dynamic Filtering
- Real-time filtering based on selected category
- Resets page position and loads filtered results

### Responsive Design
Optimized breakpoints:
- **Desktop**: Full 300px card width in grid layout
- **Tablet (768px and below)**: Cards take 90% width
- **Mobile (400px and below)**: Adjusted font sizes and button widths

### Loading State
- Spinner animation displayed while fetching data
- Auto-hides once data is loaded
- Error handling for failed data fetches

## Browser Compatibility

- Chrome/Edge (Latest)
- Firefox (Latest)
- Safari (Latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Optimizations

✅ Batch Loading: Teams load in groups of 20 to reduce rendering overhead
✅ Event Delegation: Scroll event listener optimized for efficiency
✅ CSS Animations: GPU-accelerated transforms for smooth interactions
✅ Lazy Data Extraction: Categories extracted only when rendering

## Future Enhancement Ideas

- 💡 Add team search by keywords
- 💡 Advanced filters (domain-based, team size)
- 💡 User authentication and profile management
- 💡 Direct messaging between team members
- 💡 Team skill requirement matching
- 💡 Save favorite teams
- 💡 Notifications for new teams
- 💡 Dark mode support

## Troubleshooting

**Issue**: Teams not loading
- **Solution**: Check internet connection and ensure Google Sheets API is accessible

**Issue**: Filter not working
- **Solution**: Clear browser cache or refresh the page

**Issue**: Buttons not opening forms
- **Solution**: Ensure pop-ups are not blocked in browser settings

## Deployment

This project is deployed on **GitHub Pages** and is live and accessible at:
- **URL**: https://tejaatexploring.github.io/CapstoneTeamFinder/main.html
- **Repository**: Built and deployed for college student usage

## Getting Started

Simply open the live link above in your web browser. No installation or setup required!

## Contact & Support

For issues, feature requests, or suggestions related to the Capstone Team Finder:
- **Phone**: +91 9019259474
- **Note**: Data may take a few moments to load/update

## Project Highlights

⚡ **Built in 4 hours** - Rapid development for immediate student needs
🎓 **Actively used by college students** - Real-world impact on campus
🔐 **Privacy-first** - Doesn't collect or display CGPA
🤝 **Hassle-free team formation** - Simple, straightforward interface

## How It Started

This tool was created to solve a real problem: making capstone team formation easy and stress-free. In just 4 hours, the platform was built and deployed, allowing students to:
- List their teams and member requirements
- Discover and connect with other teams
- Manage team posts without worrying about privacy
- Complete their teams efficiently

The tool has since been shared widely across the college and is actively helping students form their capstone project teams!

## License

This project is developed for educational purposes within the capstone program.

---

**Last Updated**: January 2026
**Version**: 1.0 (Production - Live on GitHub Pages)
**Status**: ✅ Active and In Use