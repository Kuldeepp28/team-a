# Security Best Practices

## Overview

This guide describes security practices for developers and operators working with the project.

## Authentication

- Use secure authentication mechanisms.
- Do not share authentication credentials.
- Keep authentication configuration out of source code.
- Use HTTPS for communication between clients and services.

## JWT

- Keep JWT signing secrets secure.
- Never commit JWT secrets to the repository.
- Use appropriate token expiration times.
- Validate JWTs before granting access to protected resources.
- Do not log JWTs or authentication tokens.

## Role-Based Access Control (RBAC)

- Follow the principle of least privilege.
- Give users only the permissions they need.
- Validate permissions on the server side.
- Do not rely only on frontend checks for authorization.
- Review roles and permissions regularly.

## Secrets Management

Never commit the following to Git:

- Passwords
- API keys
- JWT secrets
- Database credentials
- Access tokens
- Private keys

Use environment variables or an approved secrets-management system instead.

## Dependencies

- Keep project dependencies updated.
- Review security advisories for dependencies.
- Remove unused dependencies where possible.

## Logging

- Do not log passwords, tokens, API keys, or other sensitive information.
- Keep security-related errors useful without exposing confidential data.

## Reporting Security Issues

If you discover a security vulnerability, do not post sensitive details publicly in a normal issue.

Follow the project's designated security reporting process.
