# DangChuVMNewb

An Android application built with modern Android development practices using Gradle build system, Material Design components, and support for Android SDK 36.

## Project Overview

**DangChuVMNewb** is an Android application with the following specifications:
- Application ID: `com.dangchuvmnewb`
- Target SDK: 36
- Minimum SDK: 30
- Compile SDK: 36
- Version: 1.0 (versionCode 1)

## Features

- Material Design components for modern UI experience
- View Binding enabled for safer view interactions
- ProGuard enabled for optimized release builds
- Resource shrinking for smaller APK size
- Internet permission for network operations
- Data sync foreground service support

## Prerequisites

Before building this project, ensure you have:

- Android Studio (latest version recommended)
- Android SDK Platform 36
- Android SDK Build-Tools
- Java 17 or higher
- Gradle 8.13.1 or higher

## Setup Instructions

### 1. Clone the repository
```bash
git clone <repository_url>
cd chuoongpro
```

### 2. Build the project
```bash
# Using Gradle wrapper (recommended)
./gradlew build

# For release build
./gradlew assembleRelease

# For debug build
./gradlew assembleDebug
```

### 3. Install on device
```bash
# Install debug APK
./gradlew installDebug

# Install release APK
./gradlew installRelease
```

## Dependencies

The project uses the following main dependencies:

- **AndroidX AppCompat**: `1.7.1` - Provides backward compatibility for Android components
- **Material Components**: `1.13.0` - Material Design components and themes
- **ConstraintLayout**: `2.2.1` - Flexible layout system
- **AndroidX Core**: `1.17.0` - Core AndroidX utilities

These dependencies are managed through the `libs.versions.toml` file for consistent version management.

## Build Configuration

The project is configured with:

- **Java 17** - Both source and target compatibility
- **View Binding** - Enabled for type-safe view handling
- **ProGuard** - Enabled for release builds with optimization rules
- **Resource Shrinking** - Enabled to reduce app size

## Release Signing

The application includes release signing configuration:
- Keystore file: `testkey.keystore`
- Keystore password: `testkey`
- Key alias: `testkey`
- Key password: `testkey`

⚠️ **Note**: The provided keystore is for development/testing purposes only. For production releases, replace with a secure production keystore and update the passwords.

## Project Structure

```
chuoongpro/
├── app/
│   ├── src/main/java/          # Java/Kotlin source files
│   ├── src/main/res/           # Resources (layouts, drawables, etc.)
│   ├── src/main/AndroidManifest.xml  # App manifest
│   ├── build.gradle            # App-specific Gradle configuration
│   └── proguard-rules.pro      # ProGuard rules
├── gradle/
│   └── libs.versions.toml      # Dependency versions management
├── build.gradle                # Project-level Gradle configuration
└── settings.gradle             # Module inclusion settings
```

## Permissions

The app requests the following permissions:
- `android.permission.INTERNET` - Required for network operations
- `android.permission.FOREGROUND_SERVICE_DATA_SYNC` - For data sync operations in foreground

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you encounter any issues or have questions, please file an issue on the GitHub repository.