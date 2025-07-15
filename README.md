# GitHub Commit Scraper

A modern, web-based tool to fetch and export GitHub repository commit data without requiring API authentication. Built with vanilla JavaScript and styled with Tailwind CSS.

## 🚀 Features

- **No Authentication Required**: Fetch commit data from public repositories without GitHub API tokens
- **Modern UI**: Clean, responsive design with Tailwind CSS and Inter font
- **Flexible Export Options**: Download data in CSV or plain text formats
- **Copy-Paste Ready**: Generate formatted text for easy copying to PDF/DOC files
- **Real-time Feedback**: Loading states and error handling for better user experience
- **Batch Processing**: Fetch up to 100 commits with pagination support

## 📋 Table of Contents

- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Demo

Simply open `index.html` in your browser to start using the application. No server setup required!

## 🛠️ Installation

### Option 1: Direct Download

1. Clone or download this repository
2. Open `index.html` in any modern web browser
3. Start scraping commit data!

### Option 2: Local Development

```bash
# Clone the repository
git clone https://github.com/0xASR-dev/git-commit-scrapper.git

# Navigate to project directory
cd git-commit-scrapper

# Open in browser
# Simply double-click index.html or serve with any local server
```

## 🎮 Usage

### Basic Usage

1. **Enter Repository URL**: Paste a GitHub repository URL in the format:

   ```
   https://github.com/owner/repository-name
   ```

2. **Set Commit Count**: Choose how many commits to fetch (1-100)

3. **Fetch Commits**: Click "Fetch Commits" to retrieve data

4. **Export Data**: Choose your preferred format and download or copy the results


### Export Formats

#### CSV Format

```csv
Commit Hash,Author,Date,Message
abc123...,John Doe,2024-01-15T10:30:00Z,Initial commit
def456...,Jane Smith,2024-01-14T15:45:00Z,Add feature X
```

#### Plain Text Format

```
Commit: abc123...
Author: John Doe
Date: 2024-01-15T10:30:00Z
Message: Initial commit

Commit: def456...
Author: Jane Smith
Date: 2024-01-14T15:45:00Z
Message: Add feature X
```




## 📁 File Structure

```
git-commit-scrapper/
├── index.html          # Main application file
├── README.md          # Project documentation

```

### Key Components in `index.html`

```html
<!-- Core Sections -->
<div class="input-section">
  <!-- URL and count inputs -->
  <div class="export-section">
    <!-- Export controls -->
    <div class="message-display">
      <!-- Status messages -->

      <!-- JavaScript Modules -->
      <script>
        // UI Management
        // Data Processing
        // Export Functionality
      </script>
    </div>
  </div>
</div>
```

## 🎨 Styling

The application uses:

- **Tailwind CSS**: Utility-first CSS framework
- **Inter Font**: Modern, readable typography
- **Responsive Design**: Works on desktop and mobile
- **Custom Components**: Spinners, form controls, buttons

### Color Scheme

- Primary: Indigo (`#6366f1`)
- Success: Green (`#10b981`)
- Error: Red (`#ef4444`)
- Background: Light Gray (`#f3f4f6`)

## 🚦 Error Handling

The application handles various error scenarios:

### Common Errors

- **Invalid URL**: Displays format requirements
- **API Rate Limiting**: Shows retry suggestions
- **Network Issues**: Provides connectivity troubleshooting
- **Repository Not Found**: Confirms repository existence

### Error Messages

```javascript
// Examples of error handling
if (!repoUrl) {
  showMessage("Please enter a GitHub repository URL.", "error");
}

if (response.status === 403) {
  showMessage("API rate limit exceeded. Please try again later.", "error");
}
```

## 🔒 Privacy & Security

- **No Data Storage**: All processing happens in the browser
- **No Authentication**: Works with public repositories only
- **Client-Side Only**: No server-side data processing
- **HTTPS**: Uses secure GitHub API endpoints

## 🌐 Browser Compatibility

### Supported Browsers

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

### Required Features

- ES6+ JavaScript support
- Fetch API
- CSS Grid and Flexbox
- Modern DOM APIs

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Use semantic commit messages
- Follow existing code style
- Test in multiple browsers
- Update documentation as needed

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🆘 Support

If you encounter issues:

1. Check the [Issues](https://github.com/0xASR-dev/git-commit-scrapper/issues) page
2. Verify your repository URL format
3. Check your internet connection
4. Try with a different repository

## 🔮 Future Enhancements

- [ ] Support for private repositories
- [ ] Additional export formats (JSON, XML)
- [ ] Commit diff visualization
- [ ] Advanced filtering options
- [ ] Bulk repository processing
- [ ] Dark mode support

## 📊 Technical Details

### Performance

- Efficient pagination for large repositories
- Minimal DOM manipulation
- Optimized API requests

### Dependencies

- **Tailwind CSS**: Styling framework
- **Google Fonts**: Inter font family
- **GitHub API**: Data source

### Browser Storage

- Uses temporary variables only
- No localStorage or cookies
- Privacy-focused design

---

**Made with ❤️ by [0xASR-dev](https://github.com/0xASR-dev)**
