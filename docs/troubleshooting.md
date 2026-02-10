# CI/CD Troubleshooting Guide

## Common Issues

### 1. Workflow Fails on Install
- Ensure `package.json` and `package-lock.json` are up to date.
- Delete `node_modules` and reinstall dependencies.

### 2. Lint or Test Failures
- Run `npm run lint` and `npm test` locally to reproduce errors.
- Fix code style or test issues before pushing.

### 3. Build Step Not Found
- If you see `No build script defined`, add a `build` script to your `package.json` if needed.

### 4. Environment Variables
- Use `.env` files for local development, but set secrets in CI/CD platform settings.

### 5. Permissions Issues
- Ensure your CI/CD runner has access to required resources (e.g., repo, secrets).

## Debugging Tips
- Use `echo` or `printenv` to debug environment variables in workflows.
- Check logs for failed steps in GitHub Actions or GitLab CI.
- Use `actions/upload-artifact` or GitLab artifacts to collect logs or coverage reports.

---

_Expand this guide as you encounter new issues._
