# Action Repository

This repository is used to test GitHub webhooks with our Flask webhook receiver.

## Purpose
- Trigger push events when commits are made
- Trigger pull request events when PRs are created
- Trigger merge events when PRs are merged

## Webhook Events Monitored
- **Push**: When code is pushed to any branch
- **Pull Request**: When a new PR is opened
- **Merge**: When a PR is merged

## Test Instructions

### Testing Push Events
```bash
# Make changes to files
echo "New feature" >> features.txt
git add .
git commit -m "Add new feature"
git push origin main
```

### Testing Pull Request Events
```bash
# Create a new branch
git checkout -b feature-branch

# Make changes
echo "Feature implementation" >> features.txt
git add .
git commit -m "Implement new feature"
git push origin feature-branch

# Create PR on GitHub UI
```

### Testing Merge Events
- Create a pull request
- Review and merge it through GitHub UI

## Webhook Dashboard
Check the webhook dashboard at your Flask application URL to see real-time events.

---
Last updated: $(date)