# Spotify Web Player Clone

A responsive Spotify-inspired web music player built with HTML, CSS, and vanilla JavaScript. Stream music from your local server with an intuitive, modern interface.

## Features

- 🎵 **Music Playback** - Play, pause, skip, and navigate through your music library
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile devices
- 🎨 **Modern UI** - Dark theme with Spotify-inspired design
- 🔊 **Volume Control** - Adjust volume with a slider and mute toggle
- ⏱️ **Progress Bar** - Seek through songs with an interactive progress bar
- 📚 **Album Library** - Browse and select from multiple album folders
- 🏠 **Sidebar Navigation** - Quick access to home, search, and your library

---

## Preview
<img width="1885" height="860" alt="image" src="https://github.com/user-attachments/assets/58ca3650-c12b-4d2b-b039-0c4ea450565c" />


---

## Project Structure

```
.
├── index.html          # Main HTML file
├── js/
│   └── script.js       # JavaScript logic and event listeners
├── css/
│   ├── style.css       # Main styles
│   └── utility.css     # Utility classes
├── img/                # SVG icons and images
│   ├── logo.svg
│   ├── home.svg
│   ├── search.svg
│   ├── play.svg
│   ├── pause.svg
│   ├── nextsong.svg
│   ├── prevsong.svg
│   ├── volume.svg
│   ├── mute.svg
│   ├── music.svg
│   ├── playlist.svg
│   ├── hamburger.svg
│   └── close.svg
├── songs/              # Music files organized by album
│   ├── album-1/
│   │   ├── cover.jpg   # Album artwork (required)
│   │   ├── info.json   # Album metadata
│   │   └── *.mp3       # Music files
│   ├── album-2/
│   │   ├── cover.jpg
│   │   ├── info.json
│   │   └── *.mp3
│   └── ...
└── README.md
```

## Getting Started

### Prerequisites
- A local web server (required for CORS and fetch operations)
- Modern web browser with ES6 support

### Installation

1. Clone this repository
```bash
git clone https://github.com/yourusername/spotify-web-player.git
cd spotify-web-player
```

2. Set up your music folder structure
```
songs/
├── neon-horizon/
│   ├── cover.jpg
│   ├── info.json
│   └── song1.mp3
│   └── song2.mp3
```

3. Start a local web server
```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (with http-server)
npx http-server
```

4. Open your browser and navigate to `http://localhost:8000`

## Album Metadata

Each album folder must contain an `info.json` file with metadata:

```json
{
  "title": "Neon Horizon",
  "description": "A journey through electric soundscapes"
}
```

## Usage

### Controls
- **Play/Pause** - Click the play button or select a song from the library
- **Next/Previous** - Navigate between songs in the album
- **Volume** - Use the volume slider or click the speaker icon to mute
- **Seek** - Click anywhere on the progress bar to jump to that position
- **Mobile Menu** - Click the hamburger icon to toggle the sidebar

### Adding Music
1. Create a new folder in the `songs/` directory
2. Add your MP3 files to the folder
3. Add a `cover.jpg` file (album artwork)
4. Create an `info.json` file with the album metadata
5. Refresh the page - your album will appear automatically

## Technical Details

### JavaScript Functions

**`secondsToMinutesSeconds(seconds)`**
- Converts seconds to MM:SS format for display

**`getSongs(folder)`**
- Fetches all MP3 files from a specified folder
- Populates the song list in the library
- Returns array of song filenames

**`playMusic(track, pause = false)`**
- Loads and plays a track
- Updates the song info display
- Handles pause state

**`displayAlbums()`**
- Fetches all albums from the songs directory
- Loads metadata from each album's info.json
- Creates card elements for each album
- Attaches click listeners for album selection

**`main()`**
- Initializes the application
- Sets up all event listeners for player controls
- Loads the first album on startup

### Event Listeners
- Play/Pause button
- Previous/Next navigation
- Volume control slider
- Mute toggle
- Seek bar interaction
- Auto-play next track on song end
- Mobile menu toggle

## Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Modern mobile browsers

## Known Issues & Limitations

- Requires a local server (CORS restrictions)
- Only supports MP3 format
- Album artwork must be in JPG format named `cover.jpg`
- Search functionality not yet implemented
- Login/signup buttons are placeholder elements

## Future Enhancements

- [ ] Search and filter functionality
- [ ] Playlist creation
- [ ] User authentication
- [ ] Shuffle and repeat modes
- [ ] Song queue management
- [ ] Keyboard shortcuts
- [ ] Persistent playback state
- [ ] Support for additional audio formats

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to fork this project and submit pull requests for any improvements!

## Support

For issues, questions, or suggestions, please open an issue on GitHub.

---

**Note:** This is a clone/fan project inspired by Spotify. It's intended for educational purposes and personal use only.
