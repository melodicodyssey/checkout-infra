# checkout-infra
Infrastructure/DevOps settings for the wider Checkout application (with frontend and backend services)

# Checkout App – Infrastructure

This repository contains the infrastructure, deployment configuration, and service orchestration for the Checkout App platform—a modular, full-stack ecommerce application designed to simulate a real-world microservices architecture.

## Project Overview

The Checkout App is structured as a distributed system of independently deployable services, each responsible for a core domain in the ecommerce workflow. The frontend is a React-based single-page application, while the backend consists of multiple services responsible for authentication, product catalog management, shopping cart, orders, and payments.

This `checkout-infra` repo owns the system architecture, container orchestration, and environment bootstrapping logic.

## Services (Planned)

The system will include:

- `checkout-frontend`: Customer-facing React web app
- `checkout-auth-service`: Handles login, registration, and JWT issuance
- `checkout-product-service`: Manages product data and inventory
- `checkout-cart-service`: Manages user shopping carts
- `checkout-order-service`: Coordinates order creation and lifecycle
- `checkout-payment-service`: Processes and verifies payments

All services will be containerized and wired together using Docker Compose and/or Kubernetes.

## What’s in This Repo

- `docker-compose.yml`: Local dev orchestration for all services
- `k8s/`: Kubernetes manifests for staging and production (WIP)
- `env/`: Centralized `.env` files and environment templates
- `secrets/`: Documentation and tools for managing secrets (no actual secrets)
- `README.md`: This file—explains system architecture and dev workflow

## Goals of This Repo

- Provide a single entry point for setting up the dev environment
- Define service dependencies and ports
- Standardize network naming, volumes, and health checks
- Enable modular scaling via Docker or Kubernetes
- Simulate real team DevOps coordination in a multi-repo codebase

## Getting Started (WIP)

> Instructions for bringing up the local dev environment will go here once services are scaffolded.

## License

This project is licensed under the [MIT License](./LICENSE).

