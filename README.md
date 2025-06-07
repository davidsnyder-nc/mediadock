# MediaDock

A comprehensive media hub application designed for seamless media service integration across local networks, featuring intelligent interactions, card flip animations, and adaptive user interfaces.

## Features

### Core Media Management
- **Multi-service Integration**: Connects with Sonarr, Radarr, and SABnzbd for complete media management
- **Recently Added Sections**: Dedicated sections for both movies and TV shows with automatic updates
- **Quick Stats Panel**: Real-time display of total movies and TV series in your collection
- **Smart Default Navigation**: TV Shows Calendar loads by default with intelligent tab switching

### Enhanced User Interface
- **Responsive Design**: Optimized layouts for both mobile (2-column grid) and desktop (3-column grid) with sidebar navigation
- **Card Flip Animations**: Interactive movie/TV show cards with smooth flip transitions and persistent titles
- **Adaptive Grid Layouts**: Consistent 2-column mobile grids across all sections for optimal touch experience
- **Intelligent Search**: Enhanced movie and TV show search with TMDB integration and trailer support

### Advanced Features
- **AI-Enhanced Descriptions**: Gemini AI integration for intelligent content descriptions and recommendations
- **TV Shows Calendar**: Upcoming episodes grouped by day (Today, Tomorrow, weekdays) with air times
- **Real-time Downloads**: SABnzbd download history and status monitoring
- **Settings Management**: Streamlined settings interface with clear field descriptions and API key guidance

## Technologies Used

- **Frontend**: HTML5, CSS3 (Tailwind CSS), Vanilla JavaScript
- **APIs**: TMDB, Gemini AI, Sonarr, Radarr, SABnzbd
- **Icons**: Lucide Icons
- **Server**: Python HTTP Server (development)

## Screenshots

### Desktop View
- Sidebar navigation with Quick Stats panel
- Three-column grid layout for movies and TV shows
- Responsive design that maximizes screen space

### Mobile View
- Bottom navigation bar
- Single-column layout optimized for touch
- Full-screen card interactions

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/mediadock.git
cd mediadock
```

2. Copy the GitHub template to create your working file:
```bash
cp index-github.html index.html
```

3. Edit the `userSettings` object in `index.html` (around line 467) with your API keys:
```javascript
let userSettings = {
    sonarrUrl: "http://your-server-ip:8989",
    sonarrApi: "your-sonarr-api-key-here",
    radarrUrl: "http://your-server-ip:7878", 
    radarrApi: "your-radarr-api-key-here",
    sabnzbdUrl: "http://your-server-ip:8080",
    sabnzbdApi: "your-sabnzbd-api-key-here",
    tmdbApi: "your-tmdb-api-key-here",
    geminiApi: "your-gemini-api-key-here",
    defaultPage: "tv-page"
};
```

4. Start any basic HTTP server:
```bash
python -m http.server 5000
# or any other static file server
```

5. Open your browser and navigate to `http://localhost:5000`

## Configuration

MediaDock uses embedded configuration directly in the HTML file. This approach works with any basic HTTP server and keeps your API keys local while allowing safe GitHub deployment.

### Required APIs

1. **TMDB API Key (Required)**
   - Sign up at [TheMovieDB](https://www.themoviedb.org/settings/api)
   - Generate a v3 API key
   - Add to `tmdbApi` field in config.json

2. **Gemini AI API Key (Optional)**
   - Get your API key from [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Add to `geminiApi` field in config.json

3. **Media Server Configuration (Optional)**
   - **Sonarr**: Enter server URL and API key from Settings > General > Security
   - Get API key from Sonarr Settings > General > API Key

4. **Radarr Configuration**
   - Enter your Radarr server URL (e.g., `http://localhost:7878`)
   - Get API key from Radarr Settings > General > API Key

   - **Radarr**: Enter server URL and API key from Settings > General > Security
   - **SABnzbd**: Enter server URL and API key from Config > General > API Key

### Alternative: Settings Page Configuration

If you prefer to use the web interface to generate your configuration:

1. Start the server with a basic config.json (copy from config.example.json)
2. Navigate to the Settings page in MediaDock
3. Enter your server URLs and API keys in the form fields
4. Click "Copy Config to Clipboard"
5. Paste the configuration into your `config.json` file
6. Refresh the page to load the new configuration

**Note**: The `config.json` file is excluded from Git via `.gitignore` to protect your API keys.

## Usage

### Movies
- Search for movies using the search bar
- Click on movie cards to flip and see details
- Add movies directly to Radarr
- Watch trailers and view TMDB pages

### TV Shows
- **Calendar**: View upcoming episodes grouped by day (Today, Tomorrow, weekdays)
- **Search**: Find TV shows and add them to Sonarr
- Episode information includes air times and series details

### Downloads
- Monitor SABnzbd download history
- View download status and progress

## Features in Detail

### Responsive Design
- **Mobile**: Bottom navigation, single-column layout
- **Desktop**: Sidebar navigation, multi-column grids, Quick Stats panel

### Smart Navigation
- TV page defaults to calendar on initial load
- Clicking TV Shows again switches to search tab
- Configurable default landing page

### Card Interactions
- Flip animations reveal detailed information
- AI-generated descriptions for better content discovery
- Direct integration with media management services

### Real-time Data
- Dynamic API configuration fetching
- Live calendar updates
- Download status monitoring

## Development

### Project Structure
```
mediadock/
├── index.html          # Main application file
├── README.md          # This file
└── .replit           # Replit configuration
```

### Key Components
- **Navigation System**: Responsive mobile/desktop navigation
- **Search Functions**: TMDB API integration for movies and TV shows
- **Media Integration**: Direct API calls to Sonarr, Radarr, SABnzbd
- **AI Enhancement**: Gemini AI for content descriptions
- **Storage**: Local storage for user settings and preferences

## Browser Support

- Chrome/Chromium (recommended)
- Firefox
- Safari
- Edge

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## API Rate Limits

Please be aware of API rate limits:
- **TMDB**: 40 requests per 10 seconds
- **Gemini AI**: Varies by plan
- **Arr Services**: No strict limits for local instances

## Troubleshooting

### Common Issues

1. **API Keys Not Working**
   - Verify all API keys are correctly entered
   - Check that services are accessible from your network
   - Ensure CORS is properly configured for local development

2. **Services Not Connecting**
   - Verify URLs are correct and accessible
   - Check firewall settings
   - Ensure services are running

3. **Search Not Working**
   - Confirm TMDB API key is valid
   - Check browser console for error messages

### Getting Help

- Check the browser console for error messages
- Verify all required APIs are configured
- Ensure media services are running and accessible

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [TMDB](https://www.themoviedb.org/) for movie and TV show data
- [Sonarr](https://sonarr.tv/) and [Radarr](https://radarr.video/) for media management
- [SABnzbd](https://sabnzbd.org/) for download management
- [Gemini AI](https://ai.google.dev/) for intelligent content descriptions
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [Lucide](https://lucide.dev/) for icons

## Roadmap

- [ ] User authentication and multi-user support
- [ ] Custom themes and color schemes
- [ ] Mobile app companion
- [ ] Advanced filtering and sorting options
- [ ] Automated recommendations based on viewing history
- [ ] Integration with additional media services (Plex, Jellyfin)
- [ ] Notification system for new episodes and downloads

---

**MediaDock** - Your personal media management hub