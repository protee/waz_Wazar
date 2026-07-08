<!-- Title and badges -->
<div align="center">

# waz_Wazar

[![4D Component](https://img.shields.io/badge/4D-Component-blue)](#)
[![4D v21+](https://img.shields.io/badge/4D-v21%2B-brightgreen)](#)
[![4DPop Compatible](https://img.shields.io/badge/4DPop-Compatible-orange)](#)
[![License: Commercial](https://img.shields.io/badge/License-Commercial-red.svg)](#license)
[![Platform: macOS & Windows](https://img.shields.io/badge/Platform-macOS%20%7C%20Windows-lightgrey)](#)

</div>

---

<img src="https://www.protee.org/images/waz_Wazar/waz_Wazar.png" alt="waz_Wazar Logo" width="120" align="right">

<strong style="font-size:1.2em">UI, Unified</strong><br>
<strong>Mantra:</strong> One syntax to rule them all.<br>
<strong>Tagline:</strong> Build UIs without rewriting time.

<br clear="both">

## Overview

waz_Wazar is the foundational UI component of the ogTools suite, born from three decades of hands-on experience with the 4D platform. It provides an extensive library of UI widgets designed to handle almost every conceivable scenario a 4D programmer will face. Each widget is highly customizable—globally for application-wide theming, and locally for each individual instance—giving you full control over colors, shapes, and sizes to perfectly match your application's design.

It is a **foundational component** of the ogTools suite, providing the UI engine for all other components.

---

## Key Features

### Extensive Widget Library
The component includes a comprehensive set of UI widgets, covering every common interface element:

- **Value Pickers**: `waz_banner`, `waz_button`, `waz_icon`, `waz_integers`, `waz_menuBtn`, `waz_palette`, `waz_popup`, `waz_progress`, `waz_reals`, `waz_rotator`, `waz_ruler`, `waz_rulers`, `waz_search`, `waz_switch`, `waz_switchs`
- **Times, Days, Dates**: `waz_date`, `waz_dates`, `waz_dateWidget`, `waz_days`, `waz_monthDay`, `waz_periodWidget`, `waz_time`, `waz_times`, `waz_timeWidget`, `waz_year`, `waz_yearMonth`, `waz_yearPeriod`
- **Calendar**: `waz_calendar`, `waz_event`, `waz_event_form`
- **IO Module**: `waz_io_asset`, `waz_io_fun`, `waz_io_popup`, `waz_ioWidget`, `waz_io`, `waz_ios`, `waz_curves`
- **Dialogs**: `alert`, `confirm`, `more`, `request`, `progress`, `notification`

### Search Widget (waz_Search)
- **Flexible Triggering**: Configured to execute a search on every keystroke for real-time feedback, or only upon pressing Return—ideal for filtering slow-running queries.
- **Versatile Placement**: Can be styled and positioned either at the top or bottom of another object for seamless UI integration.

### Switch Widgets (waz_Switch, waz_MultiSwitch)
- **Multiple States**: Support both two-state (on/off) and three-state configurations.
- **Precise Customization**: All colors are fully customizable, allowing for pixel-perfect alignment with your application's theme.

### Advanced Progress Indicator System
- **Six Distinct Types**: Choose from six different visual styles to represent progress.
- **Multi-Threshold Coloring**: Define *n* number of thresholds to dynamically change the bar's color as progress advances (e.g., red at 0-30%, yellow at 31-70%, green at 71-100%).
- **Customizable Animation Curves**: Fine-tune the animation behavior by selecting one of five available easing curves.

### Centralized Asset Management
This unique architecture dynamically sources your application's assets—such as buttons and menu icons—from any connected component or the host database itself. Icons are intelligently retrieved and seamlessly provided to the widgets, ensuring a unified and professional interface throughout your application.

- **The waz_menuBtn Widget**: A powerful example, providing a compact, customizable interface for selecting a qualifier value bound to an integer field—all configured through a single parameter object.
- **Built-in Icon Library**: Includes a library of white/transparent icons designed for dynamic asset generation, allowing you to programmatically create customized icons by combining shapes, colors, and symbols.
- **HTML/JS Viewer**: Lightweight HTML viewer enabling entertaining JavaScript animations and visualizations via `waz_io_fun`.

### IO Module: A Unified Dialog System
Provides six essential dialog types for user interaction: Alert, Confirm, More, Query, Progress, and Notification. Each dialog type has its own global configuration, allowing you to define a consistent default look and behavior across your entire application, while easily overriding any aspect for individual instances. The system is managed through dedicated configuration widgets: `waz_io`, `waz_ios`, and `waz_ioPrefs`.

### Advanced Data Binding
Widgets can be bound in two powerful ways:
- To an object and its properties for direct manipulation.
- To an integer value, where each switch controls an individual bit—enabling compact and efficient state management.

### Advanced Scheduling & Calendar Management
- **Event Widget & Editor**: A fully interactive event (time & duration) management system featuring drag-and-drop editing, flexible time configuration, and precision snap-to-grid control.
- **Visual Calendar Component**: A beautiful calendar display dynamically populated by data collections, with intelligent collision handling for displaying multiple concurrent events in the same time slot.

### 4DPop toolbar Compatible. 
- It includes a 4DPop.json manifest for easy integration.

---

## Installation & Dependencies

### Prerequisites
- **4D v21** or higher (Project mode recommended).
- [**wok_Krolific**](https://github.com/protee/wok_Krolific) – Licensing component (mandatory dependency).
- [**wox_Xlibrary**](https://github.com/protee/wox_Xlibrary) – Core utilities (mandatory dependency).
- [**woc_Colours**](https://github.com/protee/woc_Colours) – Color management engine (mandatory dependency).
- The [**4D SVG component**](https://github.com/4d/4D-SVG) must be available in your project.

### Installation via Dependencies Manager (GitHub)

Starting with 4D v21, the recommended way to install waz_Wazar (and any ogTools component) is through the **Dependencies Manager** using the **GitHub repository**:

1. In your 4D project, open the **Dependencies Manager** (`Project > Dependencies`).
2. Click the `+` button and select **Add a dependency from a Git URL**.
3. Enter the following Git URL:`protee/waz_Wazar`
4. Choose the desired version (e.g., `main`, `latest`, or a specific release tag).
5. Confirm the installation – the component will be automatically fetched from GitHub, and linked to your project.
6. Don't forget to open your database structure settings dialog and go to the Security page to enable, if necessary, the Execute the "On host database event" method of the component option. This ensure your component is well initialised automatically.

> **Note**: For team development, commit the dependency configuration file (`dependencies.json`) to your source control so all team members automatically fetch the same version from GitHub.

---

## How It Works

1. **UI Foundation**: Provides the core widget library that powers all user interfaces in the ogTools ecosystem.
2. **Asset Management**: Uniquely sources assets from any connected component or the host database, ensuring visual consistency across your entire application.
3. **Dependency Chain**: Automatically pulled in when installing any UI‑dependent ogTools component, thanks to its dependencies on wok_Krolific, wox_Xlibrary, and woc_Colours for licensing and core functionality.

---

## ogTools Suite – Dependencies

waz_Wazar is the UI foundation of the comprehensive **ogTools suite**—an integrated development ecosystem for 4D. Other key components include:

| Icon | Component | Description |
|------|-----------|-------------|
| <img src="https://www.protee.org/images/wok_Krolific/wok_Krolific.png" alt="wok_Krolific Logo" width="60" style="border-radius: 12px;"> | **wok_Krolific** | License manager. |
| <img src="https://www.protee.org/images/wox_Xlibrary/wox_Xlibrary.png" alt="wox_Xlibrary Logo" width="60" style="border-radius: 12px;"> | **wox_Xlibrary** | Core utilities for everyday development tasks. |
| <img src="https://www.protee.org/images/woc_Colours/woc_Colours.png" alt="woc_Colours Logo" width="60" style="border-radius: 12px;"> | **woc_Colours** | Advanced, indexed color management engine. |

## License

waz_Wazar is a **commercial component** and is part of the paid ogTools suite. A valid license is required for use. For licensing options and trial requests, please contact the sales team directly.

---

## Localization

waz_Wazar supports the following languages out-of-the-box:

- 🇺🇸 English (EN), 🇫🇷 French (FR), 🇪🇸 Spanish (ES), 🇩🇪 German (DE)
- More on demand

Localization affects error messages, UI prompts, and built-in pane texts.

---

## Support & Resources

- **Official Website**: [https://www.protee.org](https://www.protee.org)
- **Documentation**: Full documentation and HDI (Host Database Interface) demos are included with your purchase.

For direct inquiries:
- **Email**: [info@protee.org](mailto:info@protee.org)

---

## About the Creator

waz_Wazar and the ogToolsSuite are developed by **Protée sarl**, a company with over 30 years of expertise in 4D development. Led by Olivier Grimbert, the team focuses on delivering high-quality, production-grade tools that enhance developer productivity and application reliability.

---

<div align="center">
  <sub>Built with ❤️ for the 4D community by Protée sarl. © 2016 - Present</sub>
</div>