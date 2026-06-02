# 📊 GitHub Follow Analyzer - Professional Edition

A professional GitHub follower analysis tool. Analyze any GitHub user's following list, followers, and unfollowers.

![GitHub Follow Analyzer](https://img.shields.io/badge/Version-2.0-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 📸 Screenshots

### Main Interface
![GitHub Analyzer Main Screen](./assets/screenshots/main-screen.png)

### Analysis Results
![Analysis Results](./assets/screenshots/analysis-results.png)

### Excel Export
![Excel Report](./assets/screenshots/excel-export.png)

## 🌐 Demo

**[🚀 Try Live Demo](https://yourusername.github.io/github-analyzer/)**

> Note: Click the link above to use the demo page. Sample user: `octocat`

## ✨ Features

- 🔍 **Detailed Analysis**: View following, followers, and unfollowers
- 🤝 **Mutual Follow**: Two-way following analysis
- 📥 **Excel Export**: Download all data in XLSX format
- 🎨 **Modern UI**: Professional and user-friendly interface
- 🔎 **Real-time Filtering**: Search users instantly
- 📊 **Rate Limit Tracking**: View API limit status
- 🌙 **Dark Mode**: Eye-friendly dark theme
- 📱 **Responsive**: Works perfectly on all devices
- ⚡ **Fast**: Optimized data fetching with pagination
- 🔒 **Secure**: Completely client-side, your data stays in your browser

## 🚀 Quick Start

### Option 1: Online Usage (Recommended)
1. Visit the [Live Demo](https://yourusername.github.io/github-analyzer/) page
2. Enter GitHub username
3. Analyze!

### Option 2: Local Usage
1. Download or clone the project:
   ```bash
   git clone https://github.com/yourusername/github-analyzer.git
   ```
2. Open **index.html** in your browser
3. Enter GitHub username (example: `octocat`)
4. Click "Analyze" button
5. View results and export to Excel!

> **Note**: No server or build process required. Just a browser is enough.

## 📖 Usage

### Basic Usage

```
1. Enter GitHub username
2. Click "🔍 Analyze" button
3. View results in tabs:
   - ❌ Not Following Back
   - 👥 Following
   - 💚 Followers
   - 🤝 Mutual Follows
4. Create report with "📥 Download Excel"
```

### Advanced Usage (With Token)

GitHub API's default rate limit is 60 requests per hour. For higher limits, use a Personal Access Token:

1. Go to [GitHub Settings → Developer settings → Personal access tokens](https://github.com/settings/tokens)
2. Click "Generate new token (classic)"
3. Select **public_repo** permission (sufficient for reading)
4. Copy the token and paste it into the application

⚠️ **Security Warning**: Never share your token with others or upload it to a public server!

## 📊 Excel Report

The Excel file contains 5 sheets:

1. **Summary**: General statistics and date
2. **Following**: People the user follows
3. **Followers**: People who follow the user
4. **Not Following Back**: Following but not followed back
5. **Mutual**: Two-way follows

## 🎯 Feature Details

### Tabs

- **Not Following Back**: Accounts you follow but don't follow you back
- **Following**: All accounts being followed
- **Followers**: All accounts following you
- **Mutual**: Two-way follows

### Filtering

Use the real-time search box to filter usernames.

### Settings

- **Records Per Page**: 30, 50, or 100 (recommended)
  - Higher value = fewer requests but slower
  - Lower value = more requests but faster progress

## 🛠️ Technical Details

### Technologies Used

- **HTML5**: Structure
- **CSS3**: Modern glassmorphism design
- **Vanilla JavaScript**: Pure JS, no frameworks
- **GitHub REST API v3**: Data source
- **SheetJS (XLSX)**: Excel export

### API Endpoints

```javascript
GET https://api.github.com/users/{username}/following
GET https://api.github.com/users/{username}/followers
```

### Rate Limits

- **Without Token**: 60 requests/hour
- **With Token**: 5000 requests/hour

### Browser Support

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 📁 Project Structure

```
Github Control/
├── index.html          # Main application (single file)
├── README.md           # Turkish documentation
├── README_EN.md        # English documentation
└── LICENSE             # MIT License
```

## 🔐 Privacy & Security

- ✅ All operations are done in your browser (client-side)
- ✅ No data is sent to any server
- ✅ Tokens are not stored in localStorage
- ✅ Connects to GitHub API over HTTPS

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

For more details, see [CONTRIBUTING.md](CONTRIBUTING.md)

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details.

## 🐛 Known Issues

- Token is required when rate limit is exceeded
- May work slowly on very large accounts (10,000+ follows)
- GitHub API may occasionally return 502 errors (try again)

## ❓ Frequently Asked Questions (FAQ)

### Q: Is the application secure?
**A:** Yes! All operations are performed in your browser. No data is sent to any server.

### Q: Can I use it without a token?
**A:** Yes, but there's a limit of 60 requests per hour. Token may be required for large accounts.

### Q: How do I create a token?
**A:** Go to [GitHub Settings → Developer settings → Personal access tokens](https://github.com/settings/tokens), select "Generate new token (classic)" and grant **public_repo** permission.

### Q: Is my data being saved?
**A:** No. No data, including tokens, is stored in localStorage.

### Q: I'm getting a rate limit error, what should I do?
**A:** Add a Personal Access Token or wait until the limit resets (hourly).

### Q: Excel file is not downloading?
**A:** Check your browser's pop-up blocker or try a different browser.

### Q: Which browsers are supported?
**A:** Chrome 90+, Firefox 88+, Safari 14+, Edge 90+ are supported.

## 🔧 Troubleshooting

### "User not found" error
- Make sure the username is spelled correctly
- Verify the user is active on GitHub

### "Rate limit exceeded" error
- Add a Personal Access Token
- Reduce records per page (to 30)
- Wait until the limit resets

### "API Error" or 502 error
- Check your internet connection
- Wait a few seconds and try again
- Check GitHub API status: [GitHub Status](https://www.githubstatus.com/)

### Excel download not working
- Open browser console (F12) and check error messages
- Try a different browser
- Disable pop-up blocker

### Running slow
- Increase records per page (to 100)
- Use a token (for rate limit increase)
- Large accounts (~10,000+ follows) normally take longer to analyze

## 🔮 Future Features

- [ ] Dark/Light theme switcher
- [ ] Charts and statistics
- [ ] Follow history comparison
- [ ] PDF export
- [ ] Multi-user comparison
- [ ] Automatic token refresh

## 📞 Contact

Feel free to open an issue for questions or suggestions.

## 🙏 Acknowledgments

- [GitHub API](https://docs.github.com/en/rest) - Data source
- [SheetJS](https://sheetjs.com/) - Excel export library
- GitHub community - For inspiration

---

⭐ If you like the project, don't forget to star it!

**Copyright GitHub Analyzer developed by Baver Koca.**
