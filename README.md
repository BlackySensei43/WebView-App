# MyWebView Android Application

A modern Android WebView application that provides a seamless web browsing experience within a native Android app. This application is designed to load and display web content while maintaining native Android functionality and user experience.

## Features

- **Web Content Display**: Seamlessly displays web content within a native Android application
- **Modern Web Support**: 
  - JavaScript enabled
  - DOM storage support
  - Mixed content support (HTTP/HTTPS)
  - Zoom controls
  - Web caching
- **Storage Access**: 
  - Full storage permission support for Android 13+ (granular media access)
  - Legacy storage support for Android 12 and below
- **User Experience**:
  - Custom user agent
  - Built-in zoom controls
  - Back button navigation support
  - Error handling with user feedback
  - Edge-to-edge display support

## Technical Requirements

- Android Studio Arctic Fox (2020.3.1) or newer
- Minimum SDK: Android 6.0 (API level 23)
- Target SDK: Android 13 (API level 33) or higher
- Gradle version: 7.0.0 or higher

## Permissions

The application requires the following permissions:

### For Android 13+ (API 33+):
- `READ_MEDIA_IMAGES`
- `READ_MEDIA_VIDEO`
- `READ_MEDIA_AUDIO`

### For Android 12 and below:
- `READ_EXTERNAL_STORAGE`
- `WRITE_EXTERNAL_STORAGE`

### Additional Permissions:
- `INTERNET` (Required for web content)

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone [repository-url]
   ```

2. Open the project in Android Studio

3. Sync the project with Gradle files

4. Build and run the application

## Configuration

The WebView is configured with the following settings:

- JavaScript enabled
- DOM storage enabled
- Mixed content allowed
- Zoom controls enabled
- Web caching enabled
- Custom user agent string

To modify the target website, update the URL in the `loadWebsite()` method in `MainActivity.java`:

```java
private void loadWebsite() {
    myWeb.loadUrl("https://exmple.com/");
}
```

## Usage

1. Launch the application
2. Grant the requested permissions when prompted
3. The web content will load automatically
4. Use standard Android gestures for navigation:
   - Swipe to scroll
   - Pinch to zoom
   - Back button to navigate through web history

## Error Handling

The application includes comprehensive error handling:
- Network errors are displayed to the user via Toast messages
- All errors are logged for debugging purposes
- WebView errors are captured and reported

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](License) file for details
