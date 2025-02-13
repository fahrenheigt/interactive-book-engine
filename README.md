# Interactive Book Engine

## Table of Contents

1. [Overview](#overview)
2. [Key Features](#key-features)
3. [Project Architecture](#project-architecture)
4. [Technologies Used](#technologies-used)
5. [Prerequisites](#prerequisites)
6. [Installation & Setup](#installation--setup)
7. [Directory Structure](#directory-structure)
8. [Basic Usage](#basic-usage)
9. [Contributing](#contributing)
10. [Testing & Code Quality](#testing--code-quality)
11. [Roadmap](#roadmap)
12. [License](#license)
13. [Code of Conduct](#code-of-conduct)
14. [Authors & Acknowledgments](#authors--acknowledgments)

---

## Overview

**Interactive Book Engine** is a project designed to simplify the creation of interactive books and branching narratives. It uses **Ionic React** for cross-platform deployment (Web, Android, iOS) and **IndexedDB** (via **Dexie.js**) for local data persistence. Authors can create, edit, and read their books without relying on a remote server.

### Goals

- Empower anyone to write **branching stories** or **visual novels**.
- Provide a **visual editor** to manage chapters, choices, and conditional events.
- Offer an **offline-ready** experience by storing data locally in IndexedDB.

---

## Key Features

- **Interactive Book Creation**: Add chapters, branches, images, and more.
- **Local Persistence**: Store and manage stories, variables, and choices in IndexedDB.
- **Visual Editing Interface**: Allows you to edit the story structure without diving into the code.
- **Cross-Platform**: Built with Ionic React for easy deployment to Web, Android, and iOS.
- **Variable Management**: Create booleans, counters, or inventory items to influence the story flow.

---

## Project Architecture

interactive-book-engine/
├── docs/               # General documentation (roadmap, architecture, changelog)
├── tests/              # End-to-end or test scripts
├── .github/            # GitHub templates, CI workflows
├── frontend/           # Ionic React project
│   ├── package.json
│   ├── ionic.config.json
│   ├── public/
│   └── src/
│       ├── pages/      # Pages (StoryList, ReadStory, HomePage, etc.)
│       ├── components/ # Reusable React/Ionic components
│       ├── services/   # Dexie.js config (dbService.ts), business logic
│       ├── App.tsx     # App root
│       └── index.tsx   # React entry point
├── LICENSE             # Project license
├── README.md           # This file
└── ...

---

## Technologies Used

- **Ionic React**: A framework for building cross-platform apps (Web, iOS, Android).
- **React**: A JavaScript library for building user interfaces.
- **Dexie.js**: Simplifies IndexedDB usage for local data storage.
- **TypeScript**: Provides static typing for more robust and maintainable code.
- **ESLint / Prettier**: For linting and code formatting (optional but recommended).
- **GitHub Actions**: For continuous integration (build, tests, etc.).

---

## Prerequisites

1. **Node.js** (version 16+ or 18+ recommended).
2. **npm** (included with Node) or **Yarn**.
3. **Ionic CLI** installed globally:
    
    `npm install -g @ionic/cli`
    
4. (Optional) **Android Studio / Xcode** if you plan to build native apps for Android/iOS.

---

## Installation & Setup

1. **Clone the repository**:
    
    `git clone https://github.com/YourUsername/interactive-book-engine.git cd interactive-book-engine`
    
2. **Install frontend dependencies**:
    
    `cd frontend npm install`
    
    or
    
    `yarn`
    
3. **Start the development server**:
    
    `ionic serve`
    
    - By default, the app will be accessible at http://localhost:8100.

## Directory Structure

### `frontend/src/pages/`

- **HomePage.tsx**: Intro or landing page.
- **StoryList.tsx**: Displays locally stored stories.
- **ReadStory.tsx**: Reading mode for a selected story (chapters, branching choices).
- **EditStory.tsx**: Basic (or advanced) editor to modify a story.

### `frontend/src/services/`

- **dbService.ts**: Dexie.js configuration and table definitions (e.g., stories, chapters, variables).
- **Other services** for business logic as needed.

### `App.tsx`

- The root component, often handles routing (React Router) and wraps everything in `IonApp`.

---

## Basic Usage

1. **Create a new story**
    
    - In the “StoryList” page, click “Add Story” (or a plus button).
    - Enter a title, optionally add sample chapters or test data.
2. **Read a story**
    
    - Select a story from the list.
    - Navigate through chapters and make choices.
3. **Edit a story**
    
    - Go to the “EditStory” page.
    - Add/remove/modify chapters and set variables to control branching paths.

_(Adapt this based on how you implement these features.)_

---

## Contributing

We welcome contributions!

4. **Fork** the project
5. Create a **branch** for your changes (`feature/my-new-feature` or `bugfix/issue-xyz`)
6. **Commit** your work
7. Open a **Pull Request** describing your changes (see the `PULL_REQUEST_TEMPLATE.md`)

For detailed guidelines, check `CONTRIBUTING.md`.

---

## Testing & Code Quality

- **Unit Tests**:
    
    bash
    
    `npm test`
    
    or
    
    `npm run test`
    
    (Depending on your setup with Jest, React Testing Library, etc.)
    
- **Lint**:
    
    `npm run lint`
    
    Runs ESLint to ensure code quality.

---

## Roadmap

8. **MVP**
    - Display a story list, basic reading flow with chapters & choices, local data storage using Dexie.
9. **Enhanced Editor**
    - More visual UI: drag-and-drop scenes, branching flowcharts.
10. **Remote Sync** (optional)
    - Sync stories and data with a server or cloud for cross-device usage.
11. **Store Deployment** (Android/iOS)
    - Configure builds via Capacitor or Cordova for publication.


---

## License

If you are using a **Proprietary License**, mention it here. For instance:

> This project uses a **Proprietary License**. See LICENSE for details.

_(Replace with MIT/Apache/GPL if you prefer open-source licensing.)_

---

## Code of Conduct

To maintain a welcoming and respectful environment, this project follows a Code of Conduct.  
Any harassing or offensive behavior may result in removal from the project.

---

## Authors & Acknowledgments

- **[Axel Le Meur]** ([@fahrenheigt](https://github.com/fahrenheigt)) – Original creator.

Special thanks to the **Ionic**, **React**, and **Dexie.js** communities for their excellent documentation and tools.