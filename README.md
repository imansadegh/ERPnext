# Company Warranty Management System

This repository contains the Docker-based setup for our company's Warranty Management System using ERPNext v15, integrated with Warranty Management and RMA (Return Merchandise Authorization) modules.

## Overview

This system manages our warranty and returns processes, including:
- Product warranty tracking
- RMA processing
- Customer service management
- Warranty claims handling
- Product returns workflow
- Quality control integration

## System Requirements

- Docker Engine (20.10.x or higher)
- Docker Compose (2.x or higher)
- Minimum 4GB RAM
- 20GB available storage
- Linux/Unix-based OS (recommended)
- Python: Version 3.10.12+
- Node.js: Version 18.x+
- MariaDB: Version 10.6+
- Redis: Latest version


## System Purpose

This system manages the complete lifecycle of product warranties and returns, enabling:

### Warranty Management
- Product warranty registration and tracking
- Warranty period monitoring
- Warranty claim processing
- Service history tracking
- Parts replacement management

### RMA (Return Merchandise Authorization)
- Customer return requests
- RMA ticket generation
- Return approval workflow
- Defect tracking
- Quality control integration

## Warranty Process Flow

1. **Product Registration**
   - Record product details
   - Register warranty period
   - Store customer information
   - Assign warranty terms

2. **Warranty Claim Processing**
   - Customer reports issue
   - Technician assessment
   - Problem diagnosis
   - Repair/replacement decision
   - Service tracking

3. **RMA Workflow**
   - Customer initiates return request
   - RMA number generation
   - Return authorization
   - Product receipt and inspection
   - Resolution (repair/replace/refund)

4. **Quality Control**
   - Defect analysis
   - Root cause investigation
   - Quality reports generation
   - Improvement recommendations

# Let's Start.

### apps.json ----> file
The `apps.json` file is a configuration file that specifies which Frappe/ERPNext apps should be installed in your ERPNext instance. It contains a list of apps with their repository URLs and branches.

Example of apps.json:
    "url": "https://github.com/frappe/warranty_management",

### .env-example ----> file
The `.env-example` file is a template file that contains example environment variables needed for configuring your ERPNext installation. This file should be copied to `.env` and customized with your specific values.

Key environment variables include:

- Database Configuration:
  - MYSQL_ROOT_PASSWORD: Root password for MariaDB
  - MYSQL_USER: Database user for ERPNext
  - MYSQL_PASSWORD: Database password
  - MYSQL_DATABASE: Database name

- ERPNext Configuration: 
  - ADMIN_PASSWORD: Administrator password
  - DB_HOST: Database host (usually mariadb)
  - DB_NAME: Database name
  - DB_PASSWORD: Database password
  - DB_USER: Database user

- Ports Configuration:
  - ERPNEXT_PORT: Port for ERPNext web interface (default 8000)
  - SOCKETIO_PORT: Port for Socket.IO (default 9000)

Make sure to copy this file to `.env` and update the values according to your needs before starting the installation.

## Installation
1. Clone repository:
```bash
git clone [repository-url]
cd warranty-management
```

2. Configure environment:
```bash
cp .env.example .env
# Update .env with your settings
```

3. Start system:
```bash
docker-compose up -d
```

4. Access system:
- URL: `http://localhost:8000`
- Default login: `Administrator`
- Password: Set in `.env` file


## License

This is an internal company tool. All rights reserved.

## Version History

- v1.0.0 (2024-XX-XX)
  - Initial setup with ERPNext v15
  - Warranty Management integration
  - RMA system implementation

## Acknowledgments

- Based on ERPNext v15
- Warranty Management module
- RMA Management module