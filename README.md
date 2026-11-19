# Nexlevr Internship – Task 3: API Keys Security Guide

## 📌 Overview

This project was completed as part of **Task 3 of the Nexlevr Internship**.

The objective is to create a beginner-friendly guide explaining how to store API keys securely, protect sensitive information, and prevent accidental exposure of credentials.

## 🎯 Objectives

- Understand what API keys are and why they must be protected.
- Learn how to store API keys using `.env` files.
- Understand how to use `.gitignore` to prevent secrets from being uploaded to GitHub.
- Learn what to do if an API key is accidentally exposed.
- Understand API key rotation and security best practices.

## 📚 Topics Covered

### 1. Understanding API Keys
An introduction to API keys, their purpose, and their importance in application authentication.

### 2. Using Environment Variables
Explains how to:
- Create a `.env` file.
- Store API keys securely.
- Load environment variables in Python using `python-dotenv`.

### 3. Protecting Secrets with Git
Explains:
- Why API keys should never be committed to GitHub.
- How to configure `.gitignore`.
- How to create a safe `.env.example` file.
- How to check files before pushing changes.

### 4. Handling Leaked API Keys
Explains the steps to take when an API key is exposed:
- Revoke the compromised key.
- Generate a replacement key.
- Update environment variables.
- Review API usage and activity.
- Remove exposed secrets from repository history where appropriate.

### 5. API Key Rotation
Explains why replacing old credentials regularly or after a security incident helps reduce security risks.

### 6. Additional Security Best Practices
Covers permissions, usage limits, separate development and production keys, and secure production secret management.

## 📁 Project Structure

```text
nexlevr-internship-task-3-api-keys-security-guide/
│
├── README.md
│
└── api_keys_guide.md
```

## 🛠️ Technologies and Tools

- **Markdown:** Documentation and formatting.
- **Git:** Version control.
- **GitHub:** Repository hosting.
- **Python:** Example of loading environment variables.
- **python-dotenv:** Python package for reading `.env` files.

## 🔐 Security Reminder

Never publish real API keys, passwords, access tokens, or other sensitive credentials in public repositories.

If a key is exposed, revoke it immediately and replace it with a new one. Removing the key from a file or Git history alone does not make it safe again.

## ✅ Deliverable

The main deliverable is:

[`api_keys_guide.md`](api_keys_guide.md)

This document provides a practical introduction to API key security for beginners.

---

**Nexlevr Internship – Task 3 of 3**  
*API Keys: How to Store Them Safely*
