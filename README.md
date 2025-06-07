# MediaDock

A comprehensive media hub application designed for seamless media service integration across local networks, featuring intelligent interactions and adaptive user interfaces.

## Features

- **Multi-service Integration**: Connects with Sonarr, Radarr, and SABnzbd for complete media management
- **Responsive Design**: Optimized layouts for both mobile and desktop with sidebar navigation on larger screens
- **Smart Search**: Movie and TV show search with TMDB integration and trailer support
- **AI-Enhanced Descriptions**: Gemini AI integration for intelligent content descriptions
- **Calendar View**: TV show calendar with upcoming episodes grouped by day
- **Card Flip Animation**: Interactive movie/TV show cards with detailed information
- **Real-time Downloads**: SABnzbd download history and status monitoring

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

2. Start the development server:
```bash
python -m http.server 5000
```

3. Open your browser and navigate to `http://localhost:5000`

## Configuration

Navigate to the Settings page and configure your API endpoints:

### Required APIs

1. **TMDB API Key**
   - Sign up at [TheMovieDB](https://www.themoviedb.org/settings/api)
   - Generate a v3 API key
   - Enter in the TMDB API Key field

2. **Gemini AI API Key**
   - Get your API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Enter in the Gemini API Key field

3. **Sonarr Configuration**
   - Enter your Sonarr server URL (e.g., `http://localhost:8989`)
   - Get API key from Sonarr Settings > General > API Key

4. **Radarr Configuration**
   - Enter your Radarr server URL (e.g., `http://localhost:7878`)
   - Get API key from Radarr Settings > General > API Key

5. **SABnzbd Configuration**
   - Enter your SABnzbd server URL (e.g., `http://localhost:8080`)
   - Get API key from SABnzbd Config > General > API Key

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