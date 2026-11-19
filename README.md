# Nexlevr Internship – Beginner Task 3: API Keys Security Guide

**Organization:** [Nexlevr](https://github.com/Nexlevr)  
**Internship Track:** Beginner  
**Task:** 3 of 3 – API Keys: How to Store Them Safely  
**Focus:** API Security and Environment Variables  
**Documentation Format:** Markdown  
**Status:** Completed

## About the Internship

This project is part of the [Nexlevr](https://github.com/Nexlevr) internship program, which includes Beginner, Intermediate, and Advanced task tracks.

This repository documents my work on the third Beginner-level task, focusing on API key security, environment variables, Git secrets protection, and secure credential management.

## Project Overview

The objective was to create a beginner-friendly guide explaining how developers can store API keys securely and protect sensitive credentials when working on software projects.

The guide introduces practical security techniques, including using `.env` files, configuring `.gitignore`, preventing accidental exposure of secrets on GitHub, and handling compromised API keys.

It also explains the importance of API key rotation and additional security best practices.

## Objectives

- Understand what API keys are and why they must be protected.
- Learn how to store sensitive credentials using `.env` files.
- Understand how to load environment variables in Python.
- Learn how to configure `.gitignore` to prevent secrets from being committed.
- Understand the risks of publishing API keys on GitHub.
- Identify the steps to take when an API key is exposed.
- Understand API key rotation and credential replacement.
- Explore additional security best practices.

## Topics Covered

### 1. Understanding API Keys

An introduction to API keys, their purpose, and their role in authenticating applications when accessing external services.

### 2. Using .env Files

Explains how to:

- Create a `.env` file.
- Store API keys as environment variables.
- Load environment variables using Python.
- Use the `python-dotenv` package.

### 3. Protecting Secrets with Git and GitHub

Covers:

- Why API keys should never be committed to public repositories.
- How to configure `.gitignore`.
- How to create a safe `.env.example` file.
- How to check tracked files before pushing changes to GitHub.

### 4. Handling Leaked API Keys

Explains the recommended response when an API key is accidentally exposed:

1. Revoke the compromised API key.
2. Generate a replacement key.
3. Update environment variables.
4. Review API usage and activity logs.
5. Remove exposed credentials from repository history where appropriate.
6. Apply additional security measures to prevent future leaks.

### 5. API Key Rotation

Explains the process of replacing existing API keys regularly or when credentials may have been compromised.

### 6. Additional Security Best Practices

Covers important recommendations, including:

- Using separate keys for development and production.
- Restricting API key permissions.
- Setting usage limits and billing alerts.
- Avoiding exposure of private keys in frontend applications.
- Using secure secrets management for production environments.

## Practical Examples

The guide includes practical examples demonstrating:

- Environment variable configuration.
- Python environment variable loading.
- `.gitignore` configuration.
- `.env.example` templates.
- Secure handling of exposed API credentials.

## Technologies and Tools

- Markdown
- Python
- python-dotenv
- Environment Variables
- Git
- GitHub

## Project Structure

```text
nexlevr-internship-task-3-api-keys-security-guide/
│
├── README.md
│
└── api_keys_guide.md
```

## Main Deliverable

**API Keys: How to Store Them Safely**

The main deliverable is:

[`api_keys_guide.md`](api_keys_guide.md)

This document provides a structured introduction to API key security and practical recommendations for beginners.

## Security Reminder

API keys must always be treated as sensitive credentials.

Never publish real API keys, passwords, access tokens, or other secrets in public repositories.

If a key is exposed, revoke it immediately and generate a replacement. Removing a key from a repository does not invalidate the compromised credential.

## Conclusion

This task provided an introduction to essential security practices in software development.

It demonstrated the importance of environment variables, Git secrets protection, secure credential storage, and API key rotation.

Following these practices helps developers build safer applications and reduce the risk of unauthorized access.

**[Nexlevr](https://github.com/Nexlevr) Internship – Beginner Track | Task 3 of 3**
