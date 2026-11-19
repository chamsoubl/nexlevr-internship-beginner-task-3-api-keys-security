# API Keys: How to Store Them Safely

## 1. Introduction

API keys are special codes used by applications to authenticate themselves when communicating with external services.

For example, an application might use an API key to access Google Maps, OpenAI, or a payment service.

API keys must be protected because anyone who obtains them may be able to access services using your account, consume your credits, or access restricted resources.

This guide explains how beginners can store API keys safely and avoid exposing sensitive information.

## 2. What Is an API Key?

An API key is a unique string of characters provided by an online service to identify and authorize an application.

Example of a fake API key:

```text
sk-example-1234567890abcdef
```

**Important:** Never use real API keys in examples, screenshots, public documents, or demonstrations.

## 3. Using .env Files

One of the simplest ways to protect API keys during development is to use environment variables.

Instead of writing an API key directly into your source code, you store it in a `.env` file.

### Step 1: Create a .env file

In your project directory, create a file named:

```text
.env
```

### Step 2: Store your API key

Inside the file, write:

```env
API_KEY=your_secret_api_key_here
```

Replace the example value with your actual API key.

### Step 3: Access the environment variable

For example, in Python:

```python
import os
from dotenv import load_dotenv

load_dotenv()

api_key = os.getenv("API_KEY")

if not api_key:
    raise ValueError("API_KEY is not configured")

print("API key loaded successfully")
```

Install the required package using:

```bash
pip install python-dotenv
```

The application can now access the API key without including it directly in the source code.

**Security tip:** Never print your actual API key in the terminal or application logs.

## 4. Never Commit Secrets to GitHub

Git is a version control system that tracks changes in your project. GitHub allows developers to share their repositories online.

If you accidentally upload your `.env` file to a public GitHub repository, other people may be able to obtain your API keys.

### Use a .gitignore File

Create a file named:

```text
.gitignore
```

Add the following lines:

```gitignore
.env
.env.*
!.env.example
```

This tells Git to ignore your environment files while allowing an example configuration file.

### Create a Safe Example File

You can create a file named `.env.example`:

```env
API_KEY=your_api_key_here
```

This file shows other developers which environment variables they need without exposing your actual credentials.

### Check Before Pushing

Before uploading your project to GitHub:

1. Check that `.env` is listed in `.gitignore`.
2. Run `git status` to inspect the files being tracked.
3. Verify that no real API keys appear in your source code.
4. Never upload screenshots containing real credentials.

**Remember:** Adding `.env` to `.gitignore` does not remove it from Git history if it was already committed.

## 5. What to Do If an API Key Leaks

If you accidentally expose an API key, you should act immediately.

Follow these steps:

1. **Revoke the exposed key:** Open the service provider's dashboard and disable the compromised API key.
2. **Generate a new key:** Create a replacement API key.
3. **Update your environment:** Replace the old key in your local `.env` file and any affected deployment environments.
4. **Check usage:** Review API activity, billing, and access logs for suspicious activity.
5. **Remove the exposed secret:** Remove it from your source code and repository history where appropriate.
6. **Prevent future leaks:** Verify your `.gitignore` configuration and review your project before publishing it again.

### What Is Key Rotation?

Key rotation is the process of replacing an existing API key with a new one regularly or whenever a key may have been compromised.

It reduces the risk of unauthorized access from old or exposed credentials.

**Important:** Deleting a leaked key from a GitHub repository is not enough. Anyone who has already accessed it may still use it. Revoke the key first.

## 6. Additional Security Best Practices

- Never share API keys through public messages or repositories.
- Use separate API keys for development and production.
- Restrict API keys to only the permissions they actually need.
- Enable usage limits and billing alerts when available.
- Store production secrets in your hosting provider's environment-variable settings or a dedicated secrets manager.
- Avoid exposing private API keys in frontend JavaScript or browser applications.
- Regularly review and rotate sensitive credentials.

## 7. Conclusion

Protecting API keys is an essential part of software development.

Using `.env` files, configuring `.gitignore`, avoiding public exposure, and rotating compromised keys are simple but important security practices.

By following these recommendations, beginners can build safer applications and reduce the risk of unauthorized access to their services.

**Final Reminder:** An API key should always be treated like a password. Keep it private and never publish it.