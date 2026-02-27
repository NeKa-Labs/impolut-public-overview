# Impolut – HD Background Remover

Free, production-ready HD background removal tool built to deliver fast and high-quality image processing.

Impolut combines a minimal React frontend, a scalable Firebase backend, and a FastAPI-powered processing engine based on the `rembg` library.

---

## 🚀 Overview

Impolut is a public web tool designed for high-definition background removal.

The platform was built with two primary goals:

- Provide a free, high-quality background removal service.
- Develop a scalable API system later integrated into larger AI platforms (including Zeta AI).

The system runs in production and is optimized for performance, simplicity, and clean output delivery.

---

## 🧠 Core Features

- High-definition background removal
- Output resolution identical to input resolution
- Batch processing support (backend)
- Fully automated processing workflow
- Fast execution (~6 seconds after cold start)
- No frontend image storage
- Free to use
- Scalable backend architecture

All processed images are downloaded as:

impolut-resultado.png

---

## 🏗 System Architecture

High-level architecture:

User (Browser)  
→ React Single-Page Application  
→ Firebase Backend  
→ FastAPI Processing Service  
→ rembg (Python-based background removal engine)  
→ Processed image returned to client  

The first request may experience cold-start delay due to server initialization. Subsequent requests are processed significantly faster.

The architecture is designed to support scalability and API reuse across external systems.

---

## 🔄 Processing Flow

1. User uploads or drags an image.
2. Frontend sends request to backend.
3. Backend forwards request to FastAPI processing service.
4. Image is processed using `rembg`.
5. Processed image is returned with original resolution preserved.
6. User downloads the result.

Images are not stored through the frontend workflow.

API-based storage is available for integrated systems.

---

## 📐 Architecture Documentation

Detailed documentation available in the `/docs` folder:

- architecture-diagram.png
- data-structure.png
- processing-flow.png

These diagrams illustrate the high-level architecture and system design without exposing proprietary implementation details.

---

## 🔌 API Purpose

While Impolut functions as a public web tool, its core objective was to build a reusable and scalable background removal API.

The API is currently integrated into larger AI-based systems, serving as a core media-processing component.

---

## ⚠️ Public Repository Notice

This repository provides a high-level architectural overview of the platform.

Sensitive implementation details, infrastructure configuration, and performance optimizations are intentionally excluded.
