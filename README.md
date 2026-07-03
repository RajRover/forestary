# 🌲 Forestary: Comprehensive System Documentation

Forestary is an advanced, end-to-end environmental intelligence platform engineered to detect active **Wildfires** and map **Deforestation** zones. By combining multi-spectral satellite/aerial image classification via Deep Learning pipelines with a robust Node.js backend and an interactive web interface, Forestary provides real-time tracking, analytical deep-dives, and reporting structures.

---

## 🏗️ Architectural Overview & File System

Below is the complete architectural layout mapping out every critical micro-directory, logic layer, and processing script across the repository:

```text
C:.
└───forestary
    ├───backend/                      # Express.js Application Server
    │   ├───node_modules/             # Resolved backend server dependencies
    │   │   ├───axios/                # Handles outward HTTP requests (e.g., to Python ML APIs)
    │   │   ├───busboy/ & multer/     # High-throughput multipart/form-data parsing for imagery uploads
    │   │   ├───cors/                 # Cross-Origin Resource Sharing handling for frontend security
    │   │   ├───dayjs/                # Optimized analytical time & date computation
    │   │   └───express/              # Core routing framework
    │   ├───package.json              # Server dependencies and lifecycle runner configurations
    │   └───server.js                 # Server entryway, API endpoint map, middleware setups
    │
    ├───frontend/                     # React / Vite Client Application
    │   ├───public/                   # Static application assets (icons, layout configuration mapping)
    │   └───src/                      # Reactive Application Layer
    │       ├───assets/               # Images, localized styles, and dynamic design elements
    │       ├───components/           # Reusable UI elements (Dashboards, Map wrappers, Upload boxes)
    │       └───services/             # Axios abstractions handles connection endpoints to backend API
    │
    ├───data/                         # Multi-modal analytical target datasets
    │   ├───deforestation_dataset/    # Categorized computer vision structure for deforest evaluation
    │   │   ├───train/                # Training baseline arrays (deforested vs non-deforested)
    │   │   ├───val/                  # Out-of-sample tuning array partitions
    │   │   └───test/                 # Production simulation holdout verification sets
    │   ├───wildfire_dataset/         # Targeted thermal/smoke image structures
    │   └───processed/                # Standardized artifacts (Resized, Normalised, Augmentation targets)
    │
    ├───fireModel/                    # Active Wildfire AI Core (CNN architectures / Transfer Learning)
    │   └───__pycache__/              # Compiled Python runtime evaluation cache
    │
    ├───deforestModel/                # Deforestation Temporal AI Core (Satellite Segmentation / Classifier)
    │   └───__pycache__/              # Compiled Python runtime evaluation cache
    │
    └───notebooks/                    # Explanatory Model prototyping, Feature Engineering, & Training EDA
```
