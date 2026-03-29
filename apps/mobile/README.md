# Benjamin Mobile App - Flutter

[![Flutter](https://img.shields.io/badge/Flutter-3.24+-blue)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/platform-iOS%20%7C%20Android%20%7C%20Web%20%7C%20HarmonyOS-lightgrey)](https://github.com/Soros2040/benjamin-fin-space-app)

AI Native financial trading platform mobile application built with Flutter.

## Features

- **Market**: Real-time market data, watchlist, market trends
- **Community**: Investment discussions, strategy sharing
- **Studio**: AI agent creation, workflow orchestration
- **Marketplace**: Trading strategies, data services
- **Settings**: Personal configuration

## Quick Start

### Prerequisites

- Flutter SDK 3.24.0 or higher (included in project root)
- Dart SDK 3.5.0 or higher

### Run on Web

```bash
cd apps/mobile
../../flutter/bin/flutter run -d chrome
```

### Run on Android

```bash
../../flutter/bin/flutter run
```

### Run on iOS (macOS only)

```bash
../../flutter/bin/flutter run -d ios
```

## Project Structure

```
apps/mobile/
├── lib/
│   ├── main.dart                    # App entry
│   ├── core/                        # Core functionality
│   │   ├── theme/                   # Theme system
│   │   └── navigation/              # Navigation
│   ├── features/                    # Feature modules
│   │   ├── market/                  # Market module
│   │   ├── community/               # Community module
│   │   ├── studio/                  # Studio module
│   │   ├── marketplace/             # Marketplace module
│   │   └── settings/                # Settings module
│   └── shared/                      # Shared components
├── assets/                          # Assets
└── pubspec.yaml                     # Dependencies
```

## Development

### Get Dependencies

```bash
../../flutter/bin/flutter pub get
```

### Run Tests

```bash
../../flutter/bin/flutter test
```

### Build for Production

**Android:**
```bash
../../flutter/bin/flutter build apk --release
```

**iOS:**
```bash
../../flutter/bin/flutter build ios --release
```

**Web:**
```bash
../../flutter/bin/flutter build web --release
```

## Design System

- **Brand Color**: #155EEF (Blue)
- **Stock Market Colors**:
  - Up: #F04438 (Red - Chinese market convention)
  - Down: #17B26A (Green)
- **Theme**: Light and Dark modes supported

## License

BSD 3-Clause License
