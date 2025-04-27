# GitHub Workflows

This directory contains GitHub Actions workflows that automate various tasks for this repository.

## Blog Post Workflow

The `blog-post-workflow.yml` file contains a workflow that automatically updates the README.md file with your latest Medium blog posts.

### How it works

1. The workflow runs automatically every day at midnight (UTC)
2. It fetches the latest posts from your Medium RSS feed
3. It updates the README.md file in the section between the comment tags `<!-- MEDIUM-BLOG-POST-LIST:START -->` and `<!-- MEDIUM-BLOG-POST-LIST:END -->`
4. It commits the changes back to the repository

### Manual Trigger

You can also trigger this workflow manually from the Actions tab in your GitHub repository.

### Setup Requirements

To use this workflow, you need to:

1. Push this repository to GitHub
2. Ensure your Medium profile is correctly set in the workflow file (`@psantana5_`)
3. No additional setup is required as the workflow uses the default `GITHUB_TOKEN`

### Customization

You can customize the workflow by editing the `blog-post-workflow.yml` file:

- Change the schedule by modifying the cron expression
- Adjust the maximum number of posts displayed by changing `max_post_count`
- Modify the post template by editing the `template` parameter
