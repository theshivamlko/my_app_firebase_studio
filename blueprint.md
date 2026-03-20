
# Project Blueprint

## Overview

This document outlines the plan for creating a Flutter application with a chat UI. The design will be inspired by the provided image, featuring a modern and visually appealing theme with gradients and clean typography.

## Current Plan

### 1. Setup Dependencies
- Add `google_fonts` for custom typography.
- Add `provider` for state management (specifically for theme toggling).

### 2. Theming
- **Color Scheme:** Create a theme based on the purple and blue gradients from the image. The primary seed color will be `Colors.deepPurple`.
- **Typography:** Use the `google_fonts` package to apply the 'Roboto' font for a clean and modern look.
- **Light & Dark Mode:** Implement both light and dark themes, with a toggle.

### 3. Application Structure
- **`main.dart`:**
    - `main()`: Entry point of the application, initializing the `ThemeProvider`.
    - `ThemeProvider`: A `ChangeNotifier` to manage the app's theme (light/dark/system).
    - `MyApp`: The root widget, which configures the `MaterialApp` with routing and theming.
- **`chat_screen.dart`:**
    - A new file to hold the main chat interface.
    - `ChatScreen`: A `StatefulWidget` that will contain the `ListView` of messages and the text input field.
    - `_MessageBubble`: A custom widget to display individual chat messages, styled differently for the user and the bot.
- **`chat_message.dart`:**
    - A data class to model a chat message, containing the text and the sender type (user or bot).

### 4. UI Implementation
- **Chat Screen:**
    - A `Scaffold` with a background color that matches the light lavender from the design.
    - An `AppBar` with the title "Rak-GPT".
    - A `ListView.builder` to display the chat messages.
    - A text input area at the bottom with a `TextField` and a send `IconButton`.
- **Message Bubbles:**
    - **User's messages:** Styled with a purple-to-blue gradient, white text, and rounded corners, appearing on the right side.
    - **Bot's messages:** Styled with a white background, dark text, and rounded corners, appearing on the left side.

### 5. Initial Data
- The chat will be populated with a few initial welcome messages to demonstrate the UI.

