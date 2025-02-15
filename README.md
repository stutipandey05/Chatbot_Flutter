# Food Chatbot - Flutter Application

## Overview
The **Food Chatbot** is a Flutter-based AI-powered chatbot application designed to answer food-related questions. This project leverages Google's Generative AI (`Gemini-2.0-flash`) via the `google_generative_ai` package to provide users with real-time, AI-generated responses about food, recipes, nutrition, and more. The chatbot is built with a clean and modern UI using Flutter and Material Design principles.

## Features
- **Conversational AI**: Uses Google's Generative AI to answer food-related questions.
- **Markdown Support**: Displays responses with formatted text.
- **Interactive UI**: A modern and responsive chat interface.
- **API Integration**: Connects to the `Gemini-2.0-flash` model via an API key.
- **State Management**: Utilizes `StatefulWidget` for efficient UI updates.
- **Error Handling**: Displays user-friendly messages in case of API failures.

## Technology Stack
- **Flutter**: Cross-platform mobile app framework.
- **Dart**: Programming language for Flutter.
- **Google Generative AI API**: Backend AI service for generating chatbot responses.
- **Flutter Markdown**: For rendering AI responses in a readable format.

## Installation
### Prerequisites
Ensure you have the following installed:
- [Flutter SDK](https://flutter.dev/docs/get-started/install)
- Dart SDK (included with Flutter)
- Android Studio or VS Code (with Flutter extension)
- API Key from Google Generative AI

### Clone the Repository
```sh
$ git clone https://github.com/yourusername/food_chatbot_flutter.git
$ cd food_chatbot_flutter
```

### Install Dependencies
```sh
$ flutter pub get
```

### Setup API Key
Replace `YOUR_API_KEY_HERE` in `ChatScreen` with your actual API key:
```dart
const apiKey = 'YOUR_API_KEY_HERE';
```

### Run the Application
```sh
$ flutter run
```

## Project Structure
```
food_chatbot_flutter/
├── lib/
│   ├── main.dart  # Entry point of the app
│   ├── chat_screen.dart  # Chat UI and logic
│   ├── widgets/
│   │   ├── message_bubble.dart  # Message display widget
│   ├── models/
│   │   ├── chat_model.dart  # Chat session model
│   ├── services/
│   │   ├── ai_service.dart  # API integration
├── pubspec.yaml  # Project dependencies
├── README.md  # Project documentation
```

## Usage
1. Open the app.
2. Enter a food-related question in the text field.
3. Click the **send button** to receive an AI-generated response.
4. Read the response in a beautifully formatted markdown style.

## Customization
### Changing the Theme
Modify the `ThemeData` in `main.dart`:
```dart
ThemeData(
  primarySwatch: Colors.teal,
  scaffoldBackgroundColor: Colors.teal[50],
);
```

### Modifying AI Model Parameters
You can adjust response quality by modifying the AI model parameters in `_initializeChatbot()`:
```dart
GenerationConfig(
  temperature: 0.7,  // Controls randomness
  topK: 50,          // Limits vocabulary choices
  topP: 0.9,         // Controls diversity
  maxOutputTokens: 500,  // Limits response length
)
```

## Troubleshooting
- **API Key Error**: Ensure you have replaced `YOUR_API_KEY_HERE` with a valid API key.
- **No Response from AI**: Check network connectivity and API key validity.
- **App Crash on Start**: Run `flutter doctor` to check dependencies.

## Roadmap
- [ ] Add support for voice input.
- [ ] Implement user authentication.
- [ ] Save chat history locally.
- [ ] Deploy as a PWA or mobile app.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing
1. Fork the repository.
2. Create a new feature branch (`git checkout -b feature-name`).
3. Commit changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Create a pull request.

## Contact
For any questions, feel free to reach out:
- Email: your.email@example.com
- GitHub: [YourUsername](https://github.com/yourusername)

