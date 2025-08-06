# Zomboid Builds v41.78.16

A modern web application for creating and managing character builds in Project Zomboid. This tool allows players to design their characters intuitively, managing professions, positive and negative traits, and automatically calculating the resulting skills.

## 🎮 What is Zomboid Builds?

Zomboid Builds is a web application that simplifies the character creation process in Project Zomboid. Instead of using the game's interface, players can:

- **Select professions** with their base skills
- **Choose positive and negative traits** with an intelligent compatibility system
- **View final skills** calculated automatically
- **Save and share builds** for later use or with other players
- **Generate random builds** to experiment with different combinations

## 🚀 Key Features

### 🎯 Intelligent Build Management
- **Compatibility system**: Automatic filtering of incompatible traits
- **Automatic calculation**: Skills calculated in real-time
- **Point validation**: Control of remaining points to balance builds
- **Game modes**: Support for Single Player and Multiplayer with specific restrictions

### 💾 Persistence and Sharing
- **Auto-save**: Persistent state in localStorage
- **Shareable URLs**: Generate links to share builds
- **Build management**: Save, load and delete custom builds
- **PDF export**: Generate professional build reports

### 🎵 User Experience
- **Audio system**: Sound effects and background music
- **Responsive interface**: Optimized for mobile and desktop
- **Internationalization**: Complete support in Spanish and English
- **Modern design**: Clean and intuitive UI with Tailwind CSS

### 🔧 Technical Architecture
- **Lazy loading**: Optimized component loading
- **Custom hooks**: Modular and reusable logic
- **Centralized configuration**: Easy maintenance and updates
- **Code obfuscation**: Multiple levels of protection

## 🏗️ Project Architecture

### Folder Structure

```
src/
├── components/           # React components organized by functionality
│   ├── features/        # Specific features
│   │   ├── build-management/  # Build management
│   │   ├── export/           # Data export
│   │   └── media/            # Audio system
│   ├── game/           # Game components
│   │   ├── controls/         # Interface controls
│   │   ├── skills/           # Skills visualization
│   │   └── traits/           # Trait management
│   └── ui/             # Interface components
│       ├── buttons/          # Reusable buttons
│       ├── layout/           # Layout components
│       └── modals/           # Modal windows
├── hooks/              # Custom hooks organized by domain
│   ├── core/           # Main game hooks
│   ├── traits/         # Trait and profession logic
│   ├── ui/             # User interface hooks
│   ├── build/          # Build management
│   └── utils/          # General utilities
├── config/             # Centralized configuration
├── db/                 # Game data (professions, traits)
├── locales/            # Translation files
└── utils/              # General utilities
```

### Key Components

#### 🎮 Game Components
- **ProfessionsList**: Interactive list of available professions
- **PositiveTraitsList/NegativeTraitsList**: Trait management with intelligent filtering
- **SelectedTraitsList**: Visualization of selected traits
- **SkillsList**: Shows calculated combined skills

#### 🎵 Audio System
- **MusicController**: Floating background music control
- **ClickableButton/ClickableDiv**: Components with integrated sound effects

#### 📱 User Interface
- **Navbar**: Main navigation with social links
- **Footer**: Controls and action buttons
- **Modals**: Windows for saving, confirming and displaying information

### Custom Hooks

#### 🧠 Game Logic
- **useGameState**: Main game state (profession, traits, mode)
- **useGameLogic**: Skill and point calculations
- **useTraitsLogic**: Trait compatibility system

#### 🎯 Build Management
- **useBuildManager**: Saved builds and modal management
- **useBuildOperations**: Save/load build operations
- **useDeleteOperations**: Build deletion

#### 🎨 User Interface
- **useClickSound**: Sound effects for interactions
- **useBackgroundMusic**: Background music control
- **useToastManager**: System notifications

#### 🔧 Utilities
- **useShareableURL**: Shareable URL generation
- **useDataUtils**: Data handling utilities
- **useStateUtils**: State management utilities

## 🛠️ Technologies Used

### Frontend
- **React 19.1.0**: User interface framework
- **Vite 7.0.4**: Build tool and development server
- **Tailwind CSS 4.1.11**: Utility-first CSS framework

### Features
- **i18next 25.3.2**: Internationalization system
- **jsPDF 3.0.1**: PDF document generation
- **html2canvas 1.4.1**: Screenshot capture for PDFs
- **react-toastify 11.0.5**: Notification system

### Development
- **ESLint**: Code linting
- **javascript-obfuscator**: Code obfuscation for production
- **terser**: Code minification

## 🎵 Audio System

### Sound Effects
- **Rotating clicks**: Three different sounds that change automatically
- **Save sound**: Special effect when saving builds
- **Controlled volume**: All effects at 50% volume

### Background Music
- **Ambient music**: "Finally Calm" on loop
- **Volume control**: 0-100% slider
- **Play/pause**: Manual music control
- **Low default volume**: 10% to be non-intrusive

## 🌐 Internationalization

The application supports multiple languages using i18next:

- **Spanish** (default language)
- **English** (complete translation)

Translation files are located in `src/locales/` and are loaded dynamically.

## 💾 Persistence System

The application automatically saves to localStorage:

- **Current game state**: Profession, traits, mode
- **Saved builds**: Complete list of custom builds
- **Configuration**: Language, volume, audio preferences

## 🔒 Code Obfuscation

The project includes multiple levels of obfuscation to protect code in production:

- **build:obfuscated**: Standard obfuscation
- **build:basic**: Basic obfuscation
- **build:high**: High obfuscation
- **build:components**: Component-specific obfuscation
- **build:utilities**: Utility-specific obfuscation

## 🎮 Game Features

### Character Creation
- **Profession selection**: Choose from various professions with unique starting skills
- **Trait management**: Select positive and negative traits with intelligent filtering
- **Skill calculation**: Automatic calculation of combined skills from profession and traits
- **Point balance**: Real-time validation of remaining trait points

### Build Management
- **Save builds**: Store custom character builds with descriptive names
- **Load builds**: Quickly access previously saved builds
- **Delete builds**: Remove unwanted builds from storage
- **Random generation**: Generate random builds for experimentation

### Sharing and Export
- **Shareable URLs**: Generate links to share builds with other players
- **PDF export**: Create professional build reports with screenshots
- **Build information**: View detailed information about shared builds

### Game Modes
- **Single Player**: Access to all traits and professions
- **Multiplayer**: Restricted to multiplayer-compatible traits only

## 🔧 Performance Optimizations

### Lazy Loading
- **Component optimization**: Components load only when needed
- **Reduced initial bundle**: Smaller initial download size
- **Faster startup**: Improved application startup time

### State Management
- **Efficient updates**: Minimal re-renders with optimized state updates
- **Memory management**: Proper cleanup of event listeners and timers
- **Local storage**: Efficient data persistence without server requirements

### Audio System
- **Preloaded sounds**: Audio files loaded for instant playback
- **Volume control**: Individual control for effects and background music
- **Performance monitoring**: Audio system optimized for smooth playback

## 📱 User Experience

### Responsive Design
- **Mobile optimized**: Full functionality on mobile devices
- **Desktop enhanced**: Rich interface for desktop users
- **Touch friendly**: Optimized for touch interactions

### Accessibility
- **Keyboard navigation**: Full keyboard support for all features
- **Screen reader support**: Proper ARIA labels and semantic HTML
- **High contrast**: Clear visual hierarchy and readable text

### User Interface
- **Modern design**: Clean and intuitive interface using Tailwind CSS
- **Consistent styling**: Unified design language throughout the application
- **Visual feedback**: Immediate feedback for all user interactions

## 📄 License

This project is under the MIT License.

## 🤝 Contact and Support

- **Discord**: [https://discord.gg/d5yy6jHQJr](https://discord.gg/d5yy6jHQJr)
- **Twitter**: [@ElSantanax](https://x.com/ElSantanax)
- **PayPal**: [https://paypal.me/ElSantanax](https://paypal.me/ElSantanax)

---

**Version**: v41.78.16 
**Last updated**: 2025
