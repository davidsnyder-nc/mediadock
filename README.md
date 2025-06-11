# MediaDock

A comprehensive AI-powered media management hub that provides intelligent content discovery and management across multiple media services. MediaDock integrates with your existing media infrastructure to deliver personalized recommendations, streamlined content management, and an intuitive user experience.

## 🎯 Overview

MediaDock serves as a centralized dashboard for managing your media library, featuring advanced AI-powered recommendations, real-time content tracking, and seamless integration with popular media management tools. Built with a modern responsive design, it works perfectly on both desktop and mobile devices.

## ✨ Key Features

### 🎬 Movies Management
- **Recently Added Movies**: Browse your latest movie downloads with elegant card-based interface
- **Movie Search**: Search and discover new movies using TMDB integration
- **One-Click Adding**: Add movies directly to Radarr with automatic quality profile selection
- **Trailer Integration**: Watch trailers directly from YouTube
- **Card Flip Animation**: Interactive cards showing movie details, ratings, and actions
- **Load More Pagination**: Efficient browsing with paginated results

### 📺 TV Shows Management
- **Smart Calendar View**: See upcoming episodes with intelligent date labeling (Yesterday, Today, Tomorrow)
- **Recently Added Shows**: Track your latest TV show downloads and episodes
- **Episode Tracking**: View episode counts, download status, and air dates
- **TV Show Search**: Discover and add new series to your library
- **Sonarr Integration**: Seamless adding of shows with automatic monitoring

### 🤖 AI-Powered Recommendations
- **Intelligent Analysis**: AI analyzes your existing library to suggest personalized content
- **Mood-Based Search**: Describe what you're in the mood for and get tailored recommendations
- **Dual Mode**: Separate recommendations for movies and TV shows
- **Smart Reasoning**: Each recommendation includes AI-generated explanations
- **Library-Aware**: Avoids suggesting content you already have

### 🔄 Download Management
- **SABnzbd Integration**: Monitor download history and status
- **Real-Time Status**: Track completed, failed, and in-progress downloads
- **Size and Date Tracking**: View download sizes and completion dates
- **Quick Refresh**: One-click refresh of download history

### ⚙️ Advanced Settings
- **API Configuration**: Manage all service connections in one place
- **Gemini AI Toggle**: Enable/disable AI-powered descriptions and recommendations
- **App Preferences**: Customize default pages and TV tabs
- **Statistics Dashboard**: View library counts and statistics
- **Reset Options**: Easy restoration to default settings

### 🎨 User Interface Features
- **Responsive Design**: Optimized for both desktop and mobile experiences
- **Desktop Sidebar**: Dedicated navigation sidebar for desktop users
- **Mobile-First**: Touch-friendly interface with bottom navigation
- **Blue Theme**: Modern blue color scheme replacing traditional green highlights
- **Play Button Icons**: MediaDock branding with play button icons
- **Card Animations**: Smooth flip animations revealing detailed information
- **Loading States**: Elegant loading indicators for all async operations

## 🔧 Technical Integrations

### Supported Services
- **Sonarr**: TV show management and monitoring
- **Radarr**: Movie management and monitoring  
- **SABnzbd**: Download client for Usenet
- **TMDB**: Movie and TV show metadata and search
- **Google Gemini AI**: Intelligent recommendations and witty descriptions
- **YouTube**: Trailer playback integration

### AI Capabilities
- **Gemini AI Integration**: Generates witty, personalized descriptions for movies and TV shows
- **Smart Recommendations**: Analyzes viewing patterns and library contents
- **Mood Understanding**: Interprets natural language mood queries
- **Content Analysis**: Provides reasoning for each recommendation

## 🚀 Setup Instructions

### Prerequisites
- Web server with HTML/JavaScript support
- Active subscriptions/accounts for integrated services
- API keys for external services

### Required API Keys
1. **Sonarr API Key**: Found in Sonarr Settings → General → Security → API Key
2. **Radarr API Key**: Found in Radarr Settings → General → Security → API Key  
3. **SABnzbd API Key**: Found in SABnzbd Config → General → SABnzbd Web Server → API Key
4. **TMDB API Key**: Register at themoviedb.org and create an API key
5. **Google Gemini AI API Key**: Get from Google AI Studio (ai.google.dev)

### Configuration
1. Download and host the `index.html` file on your web server
2. Access MediaDock through your web browser
3. Navigate to Settings and enter your API keys and service URLs
4. Configure your preferred default page and TV tab
5. Enable Gemini AI for enhanced descriptions and recommendations

### Service URLs
Configure your service URLs in the format:
- Sonarr: `http://your-server-ip:8989`
- Radarr: `http://your-server-ip:7878`
- SABnzbd: `http://your-server-ip:8080`

## 📱 Usage Guide

### Navigation
- **Desktop**: Use the sidebar navigation to switch between sections
- **Mobile**: Use the bottom navigation bar for easy thumb access

### Adding Content
1. **Search**: Use the search tabs in Movies or TV Shows sections
2. **Browse**: Look through recommendations or recently added content
3. **Add**: Click the "Add to Radarr/Sonarr" button on any content card
4. **Monitor**: Content will automatically be monitored and searched

### AI Recommendations
1. **Generate**: Click "Get AI Recommendations" or use mood-based search
2. **Describe**: Enter natural language descriptions like "funny romantic comedies"
3. **Browse**: Review AI-generated recommendations with explanations
4. **Add**: Add interesting recommendations directly to your library

### Content Discovery
- **Flip Cards**: Click any content card to reveal detailed information
- **Watch Trailers**: Click the play button to watch trailers on YouTube
- **View Details**: Click "View on TMDB" for comprehensive information
- **Track Downloads**: Monitor progress in the Downloads section

## 🎯 Features by Section

### Movies Page
- Recently Added tab with paginated browsing
- Search tab with TMDB integration
- Card flip animations with movie details
- Direct Radarr integration for adding movies
- Trailer viewing and TMDB linking

### TV Shows Page  
- Calendar tab with intelligent date formatting
- Recently Added tab with episode information
- Search tab for discovering new series
- Sonarr integration with automatic monitoring
- Episode tracking and air date information

### Recommended Page
- AI-powered movie and TV show recommendations
- Mood-based search functionality
- Library analysis for personalized suggestions
- Recommendation reasoning and explanations
- Toggle between movie and TV recommendations

### Downloads Page
- SABnzbd history with status tracking
- Download size and completion date information
- Status indicators for completed/failed downloads
- Refresh functionality for real-time updates

### Settings Page
- Comprehensive API configuration
- Gemini AI toggle and preferences
- Default page and tab settings
- Library statistics display
- Reset to defaults functionality

## 🔒 Privacy & Security

- All API keys are stored locally in your browser
- No data is transmitted to external servers except for configured services
- Gemini AI queries are sent directly to Google's API
- TMDB searches use official API endpoints
- All service communications use your configured API keys

## 🎨 Design Philosophy

MediaDock prioritizes user experience with:
- **Clean Interface**: Minimal clutter with focus on content
- **Responsive Design**: Seamless experience across all devices  
- **Intelligent Features**: AI assistance without complexity
- **Fast Performance**: Optimized loading and smooth animations
- **Intuitive Navigation**: Clear organization and easy discovery

## 🔄 Updates & Maintenance

MediaDock is designed for easy maintenance:
- **Self-Contained**: Single HTML file with embedded CSS and JavaScript
- **API-Driven**: Automatically adapts to service updates
- **Settings Persistence**: Configuration saved in browser storage
- **Error Handling**: Graceful degradation when services are unavailable

## 🤝 Contributing

MediaDock is open source and welcomes contributions:
- Report bugs through GitHub issues
- Suggest features and improvements
- Submit pull requests with enhancements
- Share configuration tips and best practices

## 📄 License

MediaDock is released under the MIT License, allowing free use, modification, and distribution.

---

**MediaDock** - Transforming media management with AI-powered intelligence and intuitive design.