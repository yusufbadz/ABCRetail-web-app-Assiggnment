# ABC Retail Azure Cloud Solution – CLDV6212

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used and Their Purpose](#technologies-used-and-their-purpose)
- [Architecture Overview](#architecture-overview)
- [Installation & Setup](#installation--setup)
- [Deployment](#deployment)
- [Features](#features)
- [GitHub Repository](#github-repository)
- [Web App URL](#web-app-url)
- [License](#license)

---

## Project Overview

This project presents a cloud-based web solution for **ABC Retail**, developed as part of the Portfolio of Evidence (POE) for the **Cloud Development B (CLDV6212)** module. The goal was to modernize and optimize their e-commerce infrastructure using **Microsoft Azure** cloud services. The project includes data storage, multimedia content handling, transaction queueing, file storage, and integration of scalable and event-driven architecture.

---

## Technologies Used and Their Purpose

### ASP.NET MVC
- Used to build the web application following the Model–View–Controller pattern.
- Handles routing, views, form submissions, and UI logic.
- Provides the main interface for interacting with Azure services.

### Microsoft Visual Studio
- IDE used to develop, debug, and publish the ASP.NET MVC application.
- Integrated tools for Azure deployment and GitHub source control.

### GitHub
- Used for version control and project collaboration.
- Stores all project source code, configurations, and documentation.

### Microsoft Azure  
Azure services used throughout Parts 1–3 of the project:

- **Azure Table Storage**  
  Stores customer profiles and product-related information.  
  *Purpose: NoSQL, scalable, key-value structured data.*

- **Azure Blob Storage**  
  Stores images and multimedia files.  
  *Purpose: Affordable, scalable, unstructured binary storage.*

- **Azure Queue Storage**  
  Holds order processing messages and inventory-related transactions.  
  *Purpose: Decouples processes, improves reliability of asynchronous workflows.*

- **Azure File Storage**  
  Stores log files, documents, and contracts.  
  *Purpose: SMB-compatible file share accessible from cloud and on-prem systems.*

- **Azure App Service**  
  Hosts the deployed ASP.NET MVC application.  
  *Purpose: Fully managed PaaS environment for scalable web hosting.*

- **Azure Functions**  
  Four serverless functions integrated to interact with Azure Storage components.  
  *Purpose: Event-driven processing, reduces compute cost, enables workflow automation.*

- **Azure SQL Database**  
  Centralized relational database storing customer, product, and order information.  
  *Purpose: Provides ACID-compliant structured data storage with high scalability.*

- **Azure SQL Geo-Replication**  
  Secondary database replica in a different region.  
  *Purpose: Disaster recovery, high availability, failover support.*

- **Azure Event Hub**  
  Handles large-scale event streaming for analytics or user activity tracking.  
  *Purpose: Ingests telemetry and supports real-time processing.*

- **Azure Service Bus**  
  Enterprise-grade messaging system used to enhance reliability of communication between services.  
  *Purpose: Supports advanced messaging like topics, sessions, and dead-lettering.*

### Microsoft SQL Server
- Used locally during development for testing the relational database setup.
- *Purpose: Ensures consistency between local and cloud SQL schema.*

### Microsoft Word
- Used for documentation, screenshots, and creating POE submission files.

### Azure Portal
- Management interface to deploy, configure, and monitor all Azure services.

---

## Architecture Overview

The architecture follows a multi-service, event-driven, cloud-native design using:

- **Azure Storage** for structured and unstructured data
- **Azure Functions** for serverless integration
- **Azure App Service** for hosting the ASP.NET MVC app
- **Azure SQL Database** for centralized, scalable relational data
- **Geo-replication** for regional failover and high availability

---

## Installation & Setup

1. Clone the repository from GitHub:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git

2. Open the solution in Visual Studio.

3. Configure your Azure Storage connection strings in appsettings.json 

4. Ensure all services (storage, queues, SQL DB) are deployed and accessible.

5. Run the application locally to verify functionality before deployment.

---

## Deployment

The application was deployed using Azure App Service and includes the following:

Deployment of ASP.NET MVC web application

Publishing of Azure Function App

Creation and replication of Azure SQL Database

Connection to Azure Storage services

---

Features

- Customer and product profile storage using Azure Tables

- Image and media handling via Azure Blob Storage

- Order and inventory transaction queuing with Azure Queue Storage

- Contract and log archiving via Azure File Storage

- Serverless interactions using Azure Functions

- Relational data managed with Azure SQL Database

- High availability through Geo-replication

- Scalable, cloud-native application hosted on Azure App Service

---


