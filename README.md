# Copilot AudioLabs - Mobile App

React Native + Expo mobile application for Copilot AudioLabs.

## Prerequisites

Before you begin, make sure you have:

- **Node.js** installed (v14 or higher) - [Download here](https://nodejs.org/)
- **Yarn** installed - Run `npm install -g yarn`
- **Expo Go** app on your phone - Download from [App Store](https://apps.apple.com/us/app/expo-go/id982107779) or [Play Store](https://play.google.com/store/apps/details?id=host.exp.exponent)
- **Git** installed - [Download here](https://git-scm.com/)
- **VS Code** (recommended) - [Download here](https://code.visualstudio.com/)

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/GabrielaHdzMicrosoft/mobileapp.git
cd mobileapp
```

### 2. Install Dependencies

```bash
yarn install
```

If you get any npm authentication errors, run:

```bash
npm logout
yarn install
```

### 3. Start the Development Server

```bash
npx expo start --tunnel
```

**Note:** We use `--tunnel` to ensure it works across different network configurations.

### 4. Run on Your Phone

1. **Wait for the QR code** to appear in your terminal
2. **On iPhone:**

   - Open your regular **Camera app** (not Expo Go)
   - Point it at the QR code
   - Tap the notification that appears at the top
   - It will open in Expo Go

3. **On Android:**
   - Open **Expo Go** app
   - Tap "Scan QR Code"
   - Scan the QR code from your terminal

### 5. You're Running! 🎉

The app will load on your phone. Any changes you make to the code will automatically refresh on your device!

## Development Workflow

### Making Changes

1. **Open the project in VS Code:**

   ```bash
   code .
   ```

2. **Edit files** - The main app entry point is:

   - `app/index.tsx` - Main screen (if using single screen)
   - `app/(tabs)/` - Tab screens (if using tab navigation)

3. **Save your changes** (Ctrl+S or Cmd+S)

4. **Watch your phone** - Changes appear automatically in 1-2 seconds!

### Project Structure

```
mobileapp/
├── app/                # App screens and navigation
│   ├── (tabs)/        # Tab-based screens
│   └── index.tsx      # Main entry point
├── assets/            # Images, fonts, etc.
├── components/        # Reusable React components
├── constants/         # App constants and configuration
├── node_modules/      # Dependencies (don't edit)
├── package.json       # Project dependencies
└── app.json          # Expo configuration
```

## Common Commands

```bash
# Start development server with tunnel (recommended)
npx expo start --tunnel

# Start development server (local network only)
yarn start

# Clear cache and start fresh
npx expo start -c

# Install a new package
yarn add package-name

# Check for issues
npx expo doctor
```

## Troubleshooting

### Can't connect to development server?

- Make sure you're using `npx expo start --tunnel`
- Check that your phone has internet connection
- Try refreshing Expo Go (pull down to refresh)

### Changes not showing up?

- Make sure you saved the file (Ctrl+S)
- Shake your phone and tap "Reload"
- Restart the server: Ctrl+C then `npx expo start --tunnel`

### NPM authentication errors?

```bash
npm logout
npm config set registry https://registry.npmjs.org/
yarn install
```

### Build errors?

```bash
# Clear everything and reinstall
rm -rf node_modules
yarn install
npx expo start --tunnel -c
```

## Git Workflow for Team

### Getting latest changes

```bash
git pull origin main
yarn install  # In case new dependencies were added
```

### Making your changes

```bash
git checkout -b feature/your-feature-name
# Make your changes
git add .
git commit -m "Description of your changes"
git push origin feature/your-feature-name
# Create Pull Request on GitHub
```

## Testing on Different Platforms

- **iOS**: Use iPhone with Expo Go
- **Android**: Use Android phone with Expo Go
- **Web**: Press `w` in terminal (limited functionality)

## Useful Resources

- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/docs/getting-started)
- [Project Repository](https://github.com/GabrielaHdzMicrosoft/mobileapp)

## Tech Stack

- **React Native** - Cross-platform mobile framework
- **Expo SDK 51** - Development platform
- **TypeScript** - Type-safe JavaScript
- **Expo Router** - File-based navigation

## Need Help?

1. Check the [Expo Discord](https://chat.expo.dev/)
2. Check terminal for error messages
3. Ask in the team chat
4. Check [Stack Overflow](https://stackoverflow.com/questions/tagged/expo)

## Production Deployment

When ready to deploy to app stores:

```bash
# Install EAS CLI
npm install -g eas-cli

# Build for Android (Play Store)
eas build --platform android

# Build for iOS (App Store)
eas build --platform ios
```

---

**Happy Coding!** 🚀

For questions about this specific project, contact: @GabrielaHdzMicrosoft
