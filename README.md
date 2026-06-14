# NeverSleep

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![TypeScript](https://img.shields.io/badge/code-TypeScript-blue)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Responsive](https://img.shields.io/badge/Responsive-Design-purple)
![Made with ❤️](https://img.shields.io/badge/Made%20with-%E2%9D%A4-red)

**NeverSleep** is a simple yet powerful web application designed to prevent your device's screen from automatically going into sleep mode. It's perfect for reading long articles, monitoring dashboards, or giving presentations.

Beyond its core functionality, NeverSleep provides several handy productivity widgets:
- **Digital Clock** — Keep track of the current time and date.
- **Battery Status** — Monitor your device's battery level and charging status.
- **To-Do List** — Jot down quick tasks and manage them directly within the app.
- **Pomodoro Timer** — Implement the Pomodoro Technique for focused work sessions and breaks.

The application saves your preferences (widget visibility, positions, clock format) and To-Do list items locally in your browser.

## Screenshots

Here's how NeverSleep looks in action:

| Awake | Almost Sleepy |
|:---:|:---:|
| <img src="/screenshots/NeverSleep_Awake.png" width="450" alt="NeverSleep - Awake" /> | <img src="/screenshots/NeverSleep_Almost_Sleepy.png" width="450" alt="NeverSleep - Almost Sleepy" /> |

| Minimal Mode - Awake | Minimal Mode - Almost Sleepy |
|:---:|:---:|
| <img src="/screenshots/NeverSleep_Minimal_Mode_Awake.png" width="450" alt="NeverSleep - Minimal Mode - Awake" /> | <img src="/screenshots/NeverSleep_Minimal_Mode_Almost_Sleepy.png" width="450" alt="NeverSleep - Minimal Mode - Almost Sleepy" /> |

## Features

### Screen Wake Lock
Prevents the screen from sleeping **while NeverSleep is the active (foreground) browser tab**, using the Screen Wake Lock API or fallback methods. Ideal for:
- Reading long articles without interruptions.
- Keeping dashboards or logs visible.
- Presenting content from within the NeverSleep tab.

### Interactive Widgets
- **Draggable** Clock, Battery, To-Do, and Pomodoro widgets — reposition them anywhere on the screen.
- **Resizable** To-Do list widget — drag the bottom-right handle to resize.
- **Persistent positions** saved in local storage across sessions.
- **Toggle visibility** for each widget via settings.

### Personalization
- Greets you by name (prompts on first visit).
- Switch between **12-hour and 24-hour** clock formats.

### Minimal Mode
Hide all widgets for a distraction-free experience with just the main toggle switch.

### Responsive Design
Adapts to different screen sizes — from desktop monitors to mobile phones — with intuitive widget repositioning.

## How to Use

1. **Open the app** in your web browser.
2. **Keep Awake Switch** — The main switch controls the screen wake lock. By default it's ON, keeping your screen awake. Toggle it OFF to let your screen sleep normally.
3. **Widgets:**
   - **Drag:** Click and hold the header of any widget to drag it around the screen.
   - **Resize (To-Do):** Click and drag the handle in the bottom-right corner of the To-Do widget to resize it.
   - **Show/Hide:** Click the Settings icon in the navbar to toggle individual widget visibility or activate Minimal Mode.
4. **Settings:** Use the Settings dropdown to:
   - Switch between 12/24-hour clock.
   - Toggle widget visibility.
   - Activate Minimal Mode.
   - Copy the app link.
   - Share the app.
   - Access Help/Troubleshooting.

## Technology Stack

| Technology | Purpose |
|---|---|
| **HTML5** | Structure and content |
| **CSS3** | Styling, layout, responsiveness (custom properties, flexbox/grid) |
| **TypeScript** | Core application logic, state management, and interactivity (compiled to JavaScript) |
| **Bootstrap 5** | CSS framework for layout, components (modals, dropdowns), and responsive utilities |
| **Font Awesome 6** | Icons |
| **NoSleep.js (adapted)** | Underlying wake lock functionality |
| **Local Storage** | Storing user preferences, widget state, and To-Do items |

## Development Setup

If you want to run or modify the project locally:

1. **Clone the repository:**

    ```bash
    git clone <your-repo-url>
    cd StayAwake
    ```

2. **Install Node.js and npm:** If you don't have them, download from [nodejs.org](https://nodejs.org/).

3. **Install TypeScript:**

    ```bash
    # Global install (optional)
    npm install -g typescript

    # Or install as dev dependency (recommended)
    npm install --save-dev typescript
    ```

4. **Compile TypeScript:**

    ```bash
    # If installed globally
    tsc

    # If installed as dev dependency
    npx tsc

    # Automatically recompile on changes
    npx tsc --watch
    ```

5. **Serve the files:**

    ```bash
    # Using http-server (Node.js)
    npx http-server .

    # Using Python 3
    python -m http.server

    # Or use VS Code Live Server extension
    ```

6. **Open your browser** — Navigate to the local server address (e.g., `http://localhost:8080` or `http://localhost:8000`).

## Deployment Instructions

### Deploy on GitHub Pages
1. Push your project to GitHub.
2. Go to your repo **Settings → Pages**.
3. Under "Source", choose the `main` branch and root directory (`/`).
4. Click **Save** — your site will be available at `https://your-username.github.io/StayAwake`.

### Deploy on Netlify
1. Go to [netlify.com](https://netlify.com/).
2. Click "Add New Site" → "Import an Existing Project".
3. Connect your GitHub repository.
4. Use default settings, deploy, and get a custom URL.

### Deploy on Cloudflare Pages
1. Visit [pages.cloudflare.com](https://pages.cloudflare.com/).
2. Click **"Create a Project"** → Link GitHub → Select repo.
3. Choose build settings (usually no build command required).
4. Click **Deploy** — your app will be hosted.

## Inspiration & Credits

- Based on [keep-awake](https://github.com/CarolinaMoraes/keep-awake) by Carolina Moraes.
- Inspired by [nosleep.page](https://nosleep.page/).
- Uses wake lock logic adapted from [NoSleep.js](https://github.com/richtr/NoSleep.js).
- Developed by [Vedant Gupta](https://www.linkedin.com/in/vedant-gupta-4bab5121b/).

## License

This project is licensed under the MIT License.

It incorporates or is inspired by the following open-source projects, each also licensed under the MIT License:

- **NoSleep.js** by Rich Tibbett — A JavaScript library to prevent display sleep in mobile web browsers. ([License](https://github.com/richtr/NoSleep.js/blob/master/LICENSE))
- **keep-awake** by Carolina Moraes — A web app to prevent screen sleep, utilizing NoSleep.js. ([License](https://github.com/CarolinaMoraes/keep-awake/blob/main/nosleep/LICENSE))
- **nosleep.page** by Bradley Kemp — A minimalist web page to keep your screen awake. ([License](https://github.com/bradleyjkemp/nosleep.page/blob/main/LICENSE))
