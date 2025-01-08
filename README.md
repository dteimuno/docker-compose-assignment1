# Drupal with PostgreSQL - Docker Compose Setup

This repository provides a simple setup for running a Drupal application with a PostgreSQL database using Docker Compose.

## Prerequisites

- Docker installed on your system.
- Docker Compose installed.

## Getting Started

### 1. Clone this repository
```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Start the services
Run the following command to start the services:
```
docker-compose up
```

### 3. Access the application
Once the containers are up and running:

- Open your browser and navigate to: http://localhost:8080
- Follow the Drupal installation process and configure the database using the following details:
  - Database name: postgres (default)
  - Database username: postgres (default)
  - Database password: example
  - Host: postgres
 
  ### 4. Stop the services
To stop the services, use:
```
docker-compose down
```
Project Structure
```
.
├── docker-compose.yml  # Docker Compose configuration
├── volumes/            # Persistent volumes for Drupal data
```

Volumes
The following named volumes are created to persist data:

  - drupal-modules: Stores custom and contributed modules.
  - drupal-profiles: Stores Drupal profiles.
  - drupal-sites: Stores site configurations.
  - drupal-themes: Stores custom and contributed themes.
These volumes are mapped to their respective directories inside the Drupal container.

