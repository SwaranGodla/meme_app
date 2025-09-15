# Meme App 📱

A beautiful Flutter application that fetches and displays wholesome memes from Reddit using the Meme API. The app features dynamic color extraction from images to create an immersive visual experience.

## ✨ Features

- **Wholesome Memes**: Fetches memes from the `wholesomememes` subreddit
- **Dynamic UI**: Background colors automatically adapt based on meme image colors
- **Cached Images**: Efficient image loading with caching for better performance
- **Interactive Cards**: Tap "View Post" to see the original Reddit post link
- **Modern Design**: Clean Material Design with gradient backgrounds
- **Loading States**: Smooth loading indicators and error handling

## 🏗️ Architecture

The app follows a clean architecture pattern with separation of concerns:

```
lib/
├── main.dart                 # App entry point
├── models/
│   └── meme_model.dart      # Meme data model
├── services/
│   └── meme_service.dart    # API service for fetching memes
├── screens/
│   └── meme_home_page.dart  # Main screen with meme list
└── widgets/
    └── meme_card.dart       # Reusable meme card component
```

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (3.8.1 or higher)
- Dart SDK
- Android Studio / VS Code with Flutter extensions

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd meme_app
```

2. Install dependencies:
```bash
flutter pub get
```

3. Run the app:
```bash
flutter run
```

## 📦 Dependencies

- **http**: ^1.4.0 - For API calls to fetch memes
- **cached_network_image**: ^3.4.1 - Efficient image caching and loading
- **palette_generator**: ^0.3.3+7 - Extract dominant colors from images

## 🎨 Key Features Explained

### Dynamic Color Extraction
The app uses the `palette_generator` package to extract dominant colors from meme images and applies them as gradient backgrounds, creating a cohesive visual experience.

### Meme Data Model
Each meme contains:
- `postLink`: Link to the original Reddit post
- `subreddit`: Source subreddit name
- `title`: Meme title
- `url`: Direct image URL
- `nsfw`/`spoiler`: Content warnings
- `author`: Reddit username
- `ups`: Upvote count
- `preview`: Image preview URLs

### API Integration
The app fetches 50 wholesome memes from the Meme API endpoint:
```
https://meme-api.com/gimme/wholesomememes/50
```

## 🛠️ Development

### Project Structure
- **Models**: Define data structures for memes
- **Services**: Handle API communication and data fetching
- **Screens**: Main UI screens and state management
- **Widgets**: Reusable UI components

### State Management
The app uses Flutter's built-in `StatefulWidget` for state management, handling:
- Loading states
- Meme data storage
- Dynamic color updates
- Error handling

## 📱 Screenshots

The app features:
- A gradient background that changes based on meme colors
- Card-based layout for each meme
- Loading indicators during data fetch
- Error handling with user-friendly messages
- Clean Material Design interface

## 🔧 Customization

You can easily customize the app by:
- Changing the subreddit in `meme_service.dart`
- Modifying the color scheme in `main.dart`
- Adjusting card styling in `meme_card.dart`
- Adding new features like favorites or sharing

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

If you have any questions or need help, please open an issue in the repository.
