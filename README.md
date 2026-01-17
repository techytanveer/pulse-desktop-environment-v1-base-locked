Pulse Desktop Environment
<p align="center"> <img src="https://img.shields.io/badge/Version-0.1.0-blue" alt="Version"> <img src="https://img.shields.io/badge/Qt-6.4.2-green" alt="Qt Version"> <img src="https://img.shields.io/badge/Wayland-Native-purple" alt="Wayland Native"> <img src="https://img.shields.io/badge/License-GPLv3-orange" alt="License"> <img src="https://img.shields.io/badge/Platform-Linux-lightgrey" alt="Platform"> </p><p align="center"> <strong>A modern, rhythmic desktop environment built with Qt6 and Wayland from scratch</strong> </p><p align="center"> <em>Rhythmic, Responsive, Refined</em> </p>
✨ Overview

Pulse is a modern desktop environment designed from the ground up using Qt6 and Wayland, focusing on smooth animations, polished visuals, and responsive interactions. Built with modern C++20 and QML, Pulse offers a clean, intuitive experience that feels alive with subtle animations and thoughtful design.

🚀 Features

    Modern Wayland Native: Built on Qt6's WaylandCompositor for smooth, secure desktop experience

    Polished Visuals: Rounded corners, subtle shadows, and smooth animations

    Responsive Design: Fluid transitions and real-time visual feedback

    Extensible Architecture: Plugin-based system for customization

    Dynamic Theming: Built-in light/dark modes with accent color customization

    Modern C++20: Clean, maintainable codebase using latest C++ standards

    Modular Design: Separated core, compositor, shell, and services

📋 Current Status

Component	Status	Description
Core System	
✅ Complete	Configuration, logging, plugin framework
Wayland Compositor	
✅ Complete	Window management, GUI interface
Desktop Shell	
✅ Complete	QML-based interface with panel
Window Manager	
✅ Complete	Move, resize, minimize, maximize windows
Plugin System	
✅ Complete	Extensible architecture
XDG Shell Protocol	
🔄 In Progress	Standard Wayland window protocol
Input Handling	
📋 Planned	Mouse, keyboard, touchpad support
Session Management	
📋 Planned	Login, logout, session restore

🏗️ Architecture
text

┌─────────────────────────────────────────────────────┐
│                    Pulse Shell                      │
│           (QML/JavaScript - Visual Layer)           │
├─────────────────────────────────────────────────────┤
│                Pulse Compositor                     │
│           (C++ - Window Management/Layout)          │
├─────────────────────────────────────────────────────┤
│                  Pulse Core                         │
│       (C++ - Core Services & Plugin System)         │
├─────────────────────────────────────────────────────┤
│                    Wayland                          │
│           (Protocol - Display Server)               │
└─────────────────────────────────────────────────────┘

Core Components

    Pulse Core: Configuration, logging, plugin framework, IPC (DBus)

    Pulse Compositor: Modern Wayland compositor with window management

    Pulse Shell: Intuitive desktop interface with dock and panel

    Window Manager: Complete window management with tiling, cascading, focus

🛠️ Building from Source

Prerequisites (Ubuntu 24.04)
bash

# Install build dependencies
sudo apt update && sudo apt install -y \
    build-essential \
    cmake \
    ninja-build \
    git \
    qt6-base-dev \
    qt6-wayland-dev \
    qt6-declarative-dev \
    qt6-tools-dev \
    qml6-module-qtquick \
    qml6-module-qtquick-controls \
    wayland-protocols \
    extra-cmake-modules \
    libwayland-dev \
    libxkbcommon-dev \
    libdrm-dev \
    libgbm-dev \
    libinput-dev

Build Instructions

bash

# Clone repository
git clone https://github.com/yourusername/pulse.git
cd pulse

# Configure build
mkdir build && cd build
cmake -GNinja -DCMAKE_BUILD_TYPE=RelWithDebInfo ..

# Build
ninja

# Install (optional)
sudo ninja install

Testing
bash

# Test core system
./src/core/pulse-core-test

# Run compositor (in nested session)
./src/compositor/pulse-compositor

# Run shell
./src/shell/pulse-shell

🎯 Roadmap

Pulse 0.2.0 "Rhythm" (Current Development)

    XDG Shell protocol implementation

    Basic input handling (mouse/keyboard)

    Window decorations with title bars

    Application launcher

    System tray integration

Pulse 0.3.0 "Harmony"

    Complete desktop shell with panel

    Workspace management

    Notification system

    Settings panel

    Power management

Pulse 1.0.0 "Symphony"

    Complete Wayland protocol support

    Advanced visual effects

    Plugin ecosystem

    Multi-monitor support

    Production-ready stability

📁 Project Structure

text

pulse/
├── src/
│   ├── core/                 # Core libraries and services
│   │   ├── pulse-core/       # Core system
│   │   ├── pulse-config/     # Configuration management
│   │   ├── pulse-ipc/        # IPC (DBus) interfaces
│   │   └── pulse-plugins/    # Plugin framework
│   ├── compositor/           # Wayland compositor
│   │   └── pulse-compositor-src/
│   │       ├── Window.cpp    # Window management
│   │       ├── WindowManager.cpp
│   │       └── CompositorView.qml  # GUI interface
│   └── shell/                # Desktop shell
│       └── pulse-shell-src/
│           ├── main.qml      # Shell interface
│           └── SimplePanel.qml
├── resources/                # Icons, wallpapers, themes
├── scripts/                  # Build and development scripts
└── tests/                    # Test suites


Code Style

    Follow Qt coding conventions

    Use clang-format for C++ code

    Use meaningful commit messages

    Write tests for new functionality

    Document public APIs

📄 License

Pulse Desktop Environment is licensed under the GNU General Public License v3.0. See the LICENSE file for details.

Acknowledgments

    Qt Project for the amazing framework

    Wayland developers for the modern display protocol

    KDE Plasma and GNOME for inspiration

    All open-source desktop environments that paved the way


🌟 Show Your Support

If you find Pulse interesting, please give it a ⭐ on GitHub!
<p align="center"> <em>Made with ❤️ for the Linux desktop community</em> <br> <strong>Keep the pulse of innovation beating</strong> </p><div align="center">
Quick Links

Getting Started • Architecture • Building • Contributing
</div>
Screenshots


Related Projects

    Qt - Application framework

    Wayland - Display server protocol

    wlroots - Wayland compositor library

Note: Pulse is under active development. Features and APIs may change.
