# MediaDock Installation Guide

## Quick Start

1. **Download** the latest release from GitHub
2. **Extract** the files to your web server directory
3. **Rename** `index-github.html` to `index.html`
4. **Open** MediaDock in your web browser
5. **Configure** your API keys in Settings

## Detailed Setup

### Step 1: Download MediaDock

Download the latest release files:
- `index-github.html` (main application file)
- `README.md` (documentation)
- `CHANGELOG.md` (version history)

### Step 2: Web Server Setup

#### Option A: Local Web Server
```bash
# Python 3
python -m http.server 5000

# Python 2
python -m SimpleHTTPServer 5000

# Node.js
npx serve .

# PHP
php -S localhost:5000
```

#### Option B: Apache/Nginx
Place files in your web server document root:
- Apache: `/var/www/html/`
- Nginx: `/usr/share/nginx/html/`
- Windows IIS: `C:\inetpub\wwwroot\`

#### Option C: File Protocol
For basic use, you can open `index.html` directly in your browser using `file://` protocol, though some features may be limited.

### Step 3: Service Configuration

Configure your existing services with proper network access:

#### Sonarr Configuration
1. Open Sonarr web interface
2. Go to Settings → General → Security
3. Copy your API Key
4. Ensure Sonarr is accessible from MediaDock's location

#### Radarr Configuration
1. Open Radarr web interface
2. Go to Settings → General → Security
3. Copy your API Key
4. Ensure Radarr is accessible from MediaDock's location

#### SABnzbd Configuration
1. Open SABnzbd web interface
2. Go to Config → General → SABnzbd Web Server
3. Copy your API Key
4. Ensure SABnzbd is accessible from MediaDock's location

### Step 4: External API Keys

#### TMDB API Key
1. Register at [themoviedb.org](https://www.themoviedb.org/)
2. Go to Settings → API
3. Request an API key
4. Copy your API key (v3 auth)

#### Google Gemini AI API Key
1. Visit [Google AI Studio](https://ai.google.dev/)
2. Create a new project or select existing
3. Generate an API key
4. Copy your Gemini API key

### Step 5: MediaDock Configuration

1. Open MediaDock in your browser
2. Navigate to Settings page
3. Enter your service URLs:
   ```
   Sonarr: http://192.168.1.100:8989
   Radarr: http://192.168.1.100:7878
   SABnzbd: http://192.168.1.100:8080
   ```
4. Enter your API keys
5. Enable Gemini AI if desired
6. Save settings

## Network Requirements

### Local Network Access
MediaDock requires network access to your services:
- Same network segment, or
- Proper firewall rules for cross-network access
- No proxy restrictions blocking API calls

### Port Requirements
Default ports (configurable in each service):
- Sonarr: 8989
- Radarr: 7878
- SABnzbd: 8080
- MediaDock: Any available port

### CORS Considerations
If hosting MediaDock on a different domain than your services, you may need to configure CORS headers in your services.

## Troubleshooting

### Common Issues

#### "Unable to connect" errors
1. Verify service URLs are correct
2. Check that services are running
3. Confirm network connectivity
4. Validate API keys

#### Blank/empty sections
1. Check API keys are valid
2. Verify services have content
3. Review browser console for errors
4. Confirm service accessibility

#### AI features not working
1. Verify Gemini AI is enabled in Settings
2. Check Gemini API key is valid
3. Ensure internet connectivity for AI requests

### Browser Compatibility
MediaDock supports modern browsers:
- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

### Performance Tips
1. Use a local web server rather than file:// protocol
2. Ensure good network connectivity to services
3. Consider limiting large libraries with pagination
4. Enable browser caching for better performance

## Security Considerations

### API Key Security
- Store API keys securely
- Use read-only API keys where possible
- Regularly rotate API keys
- Don't share configuration files containing keys

### Network Security
- Use HTTPS where possible
- Restrict service access to trusted networks
- Consider VPN for remote access
- Keep services updated with security patches

### Browser Security
- Use modern browser versions
- Keep browser updated
- Clear browser data if sharing device
- Use private browsing for sensitive configurations

## Advanced Configuration

### Custom Service Ports
If your services run on non-standard ports, update URLs accordingly:
```
Sonarr: http://localhost:9989
Radarr: http://localhost:9878
SABnzbd: http://localhost:9080
```

### Reverse Proxy Setup
For reverse proxy configurations, ensure:
- Proper header forwarding
- API endpoint accessibility
- CORS headers if needed
- SSL certificate validity

### Multiple Instances
You can run multiple MediaDock instances:
- Different configurations per instance
- Separate API keys per environment
- Isolated settings storage
- Unique hosting directories

## Getting Help

### Documentation
- README.md for feature overview
- CHANGELOG.md for version history
- GitHub Issues for bug reports

### Community Support
- GitHub Discussions for questions
- Issue tracker for bugs
- Feature requests welcome

### Self-Diagnosis
1. Check browser console for errors
2. Verify service accessibility directly
3. Test API keys in service web interfaces
4. Review network connectivity

---

**MediaDock v1.0.0** - Complete installation in minutes, manage media for years.