# xPlatform-Apps

**xPlatform-Apps** is a sample project built using the **Codename One** framework to demonstrate a cross-platform Java application that runs on both desktop (user app) and mobile (Android/iOS admin app). The project demonstrates how different app modes (user/admin) can be configured and used within a single project.

## Key Features

- **Cross-Platform Support**: Develops both a desktop application (for users) and mobile applications (for admin) using a single project in **Codename One**.
- **App Modes**: Implements different modes (`user` and `admin`) within the same project:
  - **User App**: Desktop application.
  - **Admin App**: Mobile Android/iOS application.
- **Dynamic Class Loading**: The desktop user app supports dynamic class loading to load different features/modules as needed, while the admin app (mobile) uses static class loading.
- **Menus and Submenus**: Demonstrates a user interface with menus and submenus for navigating different sections of the apps.
- **Configuration-Based App Mode Separation**: The project uses configuration settings to separate and switch between the different app modes (user/admin).

## Prerequisites

- **Java 21 LTS**: Required for building the desktop and mobile applications.
- **Codename One**: Required for building both the desktop and mobile apps in a single project.

## Codename One Setup

1. **Install Codename One**:
   - Use the **Codename One plugin** for IntelliJ IDEA or NetBeans to set up the project.

2. **Set up Codename One** to target desktop, Android, and iOS by configuring the build targets in the `codenameone_settings.properties` file.

## App Modes

### User App (Desktop)

The user app is the desktop version of the application, focusing on providing a rich feature set for users. It supports dynamic class loading, allowing new modules or features to be loaded at runtime.

- **Dynamic Class Loading**: Modules and features are loaded dynamically from `.jar` files at runtime.
- **Menus and Submenus**: The app features a navigation structure with menus and submenus for accessing different functionalities.

## Configuration for App Modes

The project uses a configuration file (`config.properties`) to separate the two app modes: `user` and `admin`. At runtime, the application detects the current mode and adjusts its behavior accordingly.

Example of the `config.properties` file:

```properties
# Configuration for app mode
app.mode=user    # Can be 'user' or 'admin'
```

