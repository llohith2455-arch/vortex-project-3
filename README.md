# VortexTech AppDev Internship — Week 3 (Intermediate)
## Connect Your App to a Live API

### What I built
A Flutter app screen (`PostsScreen`) that connects to a live public API —
[JSONPlaceholder](https://jsonplaceholder.typicode.com/posts), a free fake
REST API used for testing and prototyping — and displays the fetched data
in a scrollable list of cards.

**Features:**
- Fetches data using the `http` package (`http.get`)
- Parses the JSON response with Dart's built-in `jsonDecode()`
- Shows a `CircularProgressIndicator` while data is loading
- Shows a clear, friendly error message (with a "Try Again" button) if the
  request fails
- Displays each post in a clean `Card` layout with padding, an avatar
  showing the post ID, a bold title, and the post body
- Two manual refresh options:
  - Pull-to-refresh via `RefreshIndicator`
  - A refresh button in the app bar

### How to run it
1. Make sure you have [Flutter](https://docs.flutter.dev/get-started/install)
   installed and set up (`flutter doctor` should pass).
2. Clone this repository and move into the project folder:
   ```
   git clone <your-repo-url>
   cd vortextech_appdev_week3
   ```
3. Install dependencies:
   ```
   flutter pub get
   ```
4. Run the app on a connected device, simulator, or emulator:
   ```
   flutter run
   ```
5. To test the error handling, turn off your internet connection (or use
   airplane mode) and tap the refresh button — the error message and
   "Try Again" button should appear.

### Project structure
```
vortextech_appdev_week3/
├── lib/
│   └── main.dart      # App entry point + PostsScreen (fetch/loading/error/list UI)
├── pubspec.yaml        # Dependencies (http package)
└── README.md
```

### API used
- **JSONPlaceholder** — `https://jsonplaceholder.typicode.com/posts`
- No API key or authentication required.
