# 🌐 InterOS: The Portable Single-File Web Operating System

### Short Description

> **InterOS** is a fully self-contained (single-file) Web Operating System built on React, featuring the classic Windows 95 UI aesthetic. It allows users to **"install"** any web application (via URL or local HTML files) into their personal library, run them in a windowed environment, and carry the entire system environment in a single, portable HTML file.

---

## ✨ Key Features

| Category | Feature | Description |
| :--- | :--- | :--- |
| **Distribution** | **True Single-File Portability** | The entire application, including React, CSS, and all necessary dependencies, is bundled into one `offline_os.html` file using Vite's single-file plugin. |
| **Offline Capability** | **Always Ready** | Can be downloaded and launched instantly on any modern device (PC, tablet, mobile) that has a browser, without requiring an internet connection or web server. |
| **User Interface** | **Retro Desktop Environment** | Built using the `React95` library, featuring an authentic Taskbar, Start Menu, and Desktop. |
| **Window Manager** | **Interactive Windows** | Implements a full window manager with support for opening, closing, minimizing, and focusing windows. Windows are draggable using `react-draggable`.  |
| **App Installation** | **"Browser" (Installer)** | The dedicated "Browser" app allows users to "install" external web links or upload **local HTML files**, saving them permanently to the user's library via `localStorage`. |
| **App Runtime** | **Isolated Webview** | External and local apps are executed within isolated `<iframe>` elements (Webview) in dedicated windows, preventing conflicts with the main OS shell. |
| **User Isolation** | **Login Screen** | Features a simple Login Screen to differentiate users running the OS on a local network or shared device, providing basic isolation for their installed app library. |

---

## 🚀 Use Cases & Scenarios

| Use Case | Description |
| :--- | :--- |
| **Self-Hosting / IoT Dashboards** | Deploy the single `offline_os.html` file on a home NAS, local server, or Raspberry Pi (RPI) to act as a centralized, easy-to-access control dashboard for local services (e.g., Home Assistant, Pi-hole). |
| **Portable Workplace** | Store the file on a USB stick or cloud service. Launch it on any public or private computer to instantly access your personal, customized suite of web tools and utilities. |
| **Development Sandboxing** | Use it as a lightweight environment for testing simple HTML/JS widgets and tools in an isolated, windowed setting. |

---

## 🛠️ Getting Started

### A. Easiest Way (Offline Run)

1.  Download the latest built file, typically named `offline_os.html`, from the repository's releases or build artifacts.
2.  Double-click the file to open it in any modern web browser (Chrome, Firefox, Edge, etc.).
3.  The application will load instantly, requiring no internet connection.

### B. Development & Building

1.  **Clone the repository:**
    ```bash
    git clone [YOUR_REPO_URL]
    cd inter-os
    ```
2.  **Install dependencies:**
    ```bash
    npm install react95 styled-components react-draggable vite-plugin-singlefile
    ```
3.  **Run for development (Hot Reloading):**
    ```bash
    npm run dev
    ```
4.  **Build the Single-File HTML:**
    This command uses `vite-plugin-singlefile` to generate the highly portable version.
    ```bash
    npm run build
    # The final, single HTML file will be located in the 'dist' directory.
    ```

---

## ⚙️ Technical Details

| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Framework** | React 18 (Functional Components & Hooks) | Core UI logic and state management. |
| **UI Library** | React95 | Provides the iconic Windows 95 aesthetic and components. |
| **Bundler** | Vite + `vite-plugin-singlefile` | Compiles the entire application into a single, self-contained HTML file. |
| **Window Management** | `react-draggable` | Enables drag-and-drop functionality for application windows. |
| **Data Storage** | `localStorage` | Used to simulate a persistent file system, storing the user's installed application list. |

---

## ✅ TODO & Future Plans

* [ ] Implement full, reliable Drag-and-Drop functionality for Desktop icons.
* [ ] Introduce an **Export/Import** function for the app library (JSON) to easily migrate settings between different browsers/devices.
* [ ] Explore **WebRTC** integration to enable basic peer-to-peer (P2P) communication (chat, data exchange) between users on a local network.
* [ ] Add a visual status bar or tray icon area.
