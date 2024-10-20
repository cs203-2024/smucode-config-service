# smucode-config-service

## Overview
The smucode-config-service is a centralized configuration server for the SMUCode tournament management system.
It utilizes Spring Cloud Config Server to externalize configuration for all microservices, providing a scalable and maintainable approach to configuration management.

## Features
- AWS S3 backend for storing configuration files
- Integration with Eureka for service discovery
- Configurable server port and application name

## Prerequisites
- Java 17 or higher
- Maven
- AWS account with S3 access
- Eureka Server (for service registration)

## Configuration
The service is configured via the `application.yaml` file:

- AWS S3 configuration:
  - Region: Configurable via `AWS_REGION` environment variable (default: ap-southeast-1)
  - Bucket: Specified by `AWS_CONFIG_BUCKET_NAME` environment variable
- Eureka client configuration:
  - Enabled by default
  - Service URL: Configurable via `EUREKA_CLIENT_SERVICEURL_DEFAULTZONE` environment variable

## Running the Application
1. Ensure you have set the required environment variables:
   - `AWS_REGION` (optional)
   - `AWS_CONFIG_BUCKET_NAME`
   - `EUREKA_CLIENT_SERVICEURL_DEFAULTZONE` (optional)

2. Run the application using Maven:
   ```
   mvn spring-boot:run
   ```
