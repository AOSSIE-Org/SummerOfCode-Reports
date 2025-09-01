# PictoPy's Final Report for GSoC'25

## Student Information

- **Name:** Rahul Harpal
- **GitHub:** [rahulharpal1603](https://github.com/rahulharpal1603)
- **Social Profiles:** [Linkedin](https://www.linkedin.com/in/rahulharpal/)
- **Organization:** [Australian Open Source Software Innovation and Education (AOSSIE)](https://www.aossie.org/)
- **Project:** [PictoPy](https://github.com/AOSSIE-Org/PictoPy)
- **Updated project timeline:** [Link](https://docs.google.com/document/d/1w2nTQ5nLkWb824FT27L6YKCgT6dThwRLa1gt33h7UfM/edit?tab=t.dw71m7dpokgi)
- **GSoC'25 Proposal:** [Link](https://docs.google.com/document/d/1F0HhIUfv1OJQ_D1lViH0wzECE_ueWQtdz8jDvBwu0Vw/edit?tab=t.0)
- **Documentation Site:** [Link](https://aossie-org.github.io/PictoPy/)

## Abstract

For GSoC'25, I aimed at an all-around enhancement to PictoPy by improving its backend scalability, frontend usability, and deployment accessibility. Key backend upgrades include implementing user-named face clusters, optimizing face clustering with dimensionality reduction, upgrading to YOLOv11 for better detection, adding GPU-accelerated inferencing, and redesigning inefficient database schemas. A fresh modern UI using Radix UI will be introduced on the frontend, along with a unified folder selection, an advanced search bar supporting face and object queries, object bounding box display, and user notifications. To ensure broader accessibility, the project will package and publish PictoPy for Windows, macOS, and Linux. This will involve the creation of CI/CD pipelines on the GitHub repository. Comprehensive documentation will encourage new developers to contribute, including contributing guides, API references, and a setup video. These improvements will make PictoPy more user-friendly, scalable, and ready for widespread adoption.

## Technologies Used

- Frontend: Tauri, ReactJS, and ShadCN
- Backend: FastAPI(Python)
- Database: SQLite
- AI: ONNX Runtime, YOLOv11, FaceNet

## Demos

### Demo Videos
1. [Mid Term Eval Demo](https://www.youtube.com/watch?v=8mgXXvdWQ5U)


### Test Released Desktop Apps:

- [GitHub Releases Page](https://github.com/AOSSIE-Org/PictoPy/releases/latest)

## Project Description

PictoPy is an intelligent photo management application that combines AI-powered features with efficient file organization. Built with a modern tech stack, it provides users with advanced photo discovery and management capabilities.

### Key Features

* **AI-Powered Tagging**: Automatic image classification and tagging using deep learning models
* **Face Recognition**: Intelligent face clustering and recognition for organizing photos by people
* **Smart Albums**: Create and manage photo albums with advanced filtering capabilities
* **File System Sync**: Real-time monitoring and synchronization of photo directories
* **Cross-Platform**: Desktop application built with Tauri for Windows, macOS, and Linux

<img width="2499" height="1932" alt="image" src="https://github.com/user-attachments/assets/4d409bb2-a676-455f-968e-2560508b0749" />






## Relevant Pull Requests (ordered by the date of merge)

1. PR #423: [Added caching in the PictoPy-build-check workflow](https://github.com/AOSSIE-Org/PictoPy/pull/423)
2. PR #426: [Configure auto-updater, Redux toolkit setup, update dependencies](https://github.com/AOSSIE-Org/PictoPy/pull/426)
3. PR #449: [Rename workflows and set up GitHub secrets to generate builds](https://github.com/AOSSIE-Org/PictoPy/pull/449)
4. PR #466: [GSoC 2025 Backend Revamp](https://github.com/AOSSIE-Org/PictoPy/pull/466)
5. PR #484: [Update documentation deployment workflow and add requirements file](https://github.com/AOSSIE-Org/PictoPy/pull/484)
6. PR #486: [Add sync microservice for watching file system events](https://github.com/AOSSIE-Org/PictoPy/pull/486)
7. PR #489: [GSoC 2025 Frontend Revamp](https://github.com/AOSSIE-Org/PictoPy/pull/489)
8. PR #492: [Update build pipeline to support the microservice.](https://github.com/AOSSIE-Org/PictoPy/pull/492)
9. PR #493: [Fix flag error in build pipeline](https://github.com/AOSSIE-Org/PictoPy/pull/493)

## Challenges and Solutions: 

1. **Packaging the Desktop App:** Unlike websites, which can be easily hosted and deployed on various platforms, building Desktop apps is a different game altogether. We must consider all the edge cases for each of the three platforms. This was solved by creating a fully customized CI/CD pipeline that generates app builds for each of the platforms, packaging the frontend, backend, and models into a single installer for each platform.
2. **Syncing system folders with the app state:** The app allows users to choose which folders to import photos from. But the challenge is keeping the app synced with the changes to the selected folder. These changes could be the addition/deletion of new folders and images. This was solved by developing a microservice that runs separately and monitors file changes inside the folders using the Python package Watchfiles. Based on the changes that happen, the main backend then updates the SQLite DB.
3. **Keeping the API and DB docs up to date:** Due to many changes happening in the APIs, it was hard to keep the API docs updated manually. So we decided to use Swagger to automatically generate API docs based on the changes made in the Python code. (See this [PR](https://github.com/AOSSIE-Org/PictoPy/pull/483) by Anjali). Similarly, for Database design, we used dbdiagram.io to automatically update our docs site (We embed the link provided by dbdiagram. See this [Link](https://aossie-org.github.io/PictoPy/backend/backend_python/database/))


## Future Plans

1. Implement a notifications system for the desktop app.
2. Complete some minor changes that are pending.
3. Reduce the final app size by only shipping small models first and then downloading the larger ones later based on the user's requirements.
4. Implement the memories feature in the app.
5. Consider further performance improvements for the backend(especially for inferencing DL models).
6. Set up proper logging for both frontend and backend.
7. Open issues and assign them to new contributors to grow the project.
8. Publicize the app to increase the user base.
9. Publish the app on Snap store, Microsoft store and macOS store (Postponed this because of platform fees)


## Acknowledgements
I sincerely thank my mentor, Pranav Aggarwal at AOSSIE, who was always there to provide me guidance and valuable feedback throughout my GSoC journey.

### Thank You 🥹
