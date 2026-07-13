# Minimal Compose Screen

A minimal, reusable **Jetpack Compose** UI built with **Material3**. It displays a centered title, a spacer, and a button that shows a Toast message on click.

## Prompt

This project was generated using the following prompt:

> Generate a minimal Jetpack Compose UI using Material3.
> Keep the design clean, centered, and clutter-free.
> Include a Column with a title Text, a Spacer, and a Button.
> On button click, show a Toast message.
> Provide all necessary imports.
> Code should be production-ready and reusable.

## Features

- Clean, centered, clutter-free layout
- Built entirely with Material3 components
- Fully reusable via composable parameters (`title`, `buttonText`, `toastMessage`)
- Includes an `@Preview` composable for quick visual checks in Android Studio
- Production-ready: no hardcoded strings/colors, theme-aware styling

## Requirements

- Android Studio (Giraffe or newer recommended)
- Kotlin 1.9+
- Jetpack Compose BOM `2024.x` or newer
- Minimum SDK 21+

## Installation

1. Copy `MinimalComposeScreen.kt` into your project, e.g.:
   ```
   app/src/main/java/com/example/app/ui/MinimalComposeScreen.kt
   ```
2. Update the package declaration at the top of the file to match your project's package structure.
3. Make sure your module's `build.gradle` (or `build.gradle.kts`) includes the Compose dependencies:
   ```kotlin
   dependencies {
       implementation(platform("androidx.compose:compose-bom:2024.06.00"))
       implementation("androidx.compose.material3:material3")
       implementation("androidx.compose.ui:ui")
       implementation("androidx.compose.ui:ui-tooling-preview")
       debugImplementation("androidx.compose.ui:ui-tooling")
   }
   ```

## Usage

Call `MinimalScreen()` from your Activity's `setContent` block, wrapped in your app's theme:

```kotlin
class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            MaterialTheme {
                MinimalScreen(
                    title = "Welcome",
                    buttonText = "Get Started",
                    toastMessage = "Let's go!"
                )
            }
        }
    }
}
```

### Default usage

```kotlin
MinimalScreen()
```

Renders with default values: title `"Welcome"`, button label `"Click Me"`, and toast message `"Button clicked!"`.

## Preview

Open the file in Android Studio and use the built-in **Split** or **Design** view to see `MinimalScreenPreview` render without running the app on a device or emulator.

## Project Structure

```
.
├── MinimalComposeScreen.kt   # Composable UI screen
└── README.md                 # Project documentation
```

## License

This snippet is free to use, modify, and distribute in your own projects.
