# Setting Up GitHub Actions for Automatic Blog Post Updates

This guide will help you set up the GitHub Actions workflow that automatically updates your README with the latest Medium blog posts.

## Steps to Push Repository to GitHub

1. **Create a new GitHub repository**

   - Go to [GitHub](https://github.com/) and sign in
   - Click the "+" icon in the top right and select "New repository"
   - Name your repository (e.g., "README" or "profile")
   - Choose whether to make it public or private
   - Click "Create repository"

2. **Initialize Git in your local repository** (if not already done)

   ```bash
   git init
   ```

3. **Add your GitHub repository as a remote**

   ```bash
   git remote add origin https://github.com/yourusername/your-repo-name.git
   ```

4. **Add all files to Git**

   ```bash
   git add .
   ```

5. **Commit your changes**

   ```bash
   git commit -m "Initial commit with README and GitHub Actions workflow"
   ```

6. **Push to GitHub**
   ```bash
   git push -u origin main
   # or if you're using master branch
   git push -u origin master
   ```

## Verifying the Workflow

1. **Check workflow status**

   - Go to your repository on GitHub
   - Click on the "Actions" tab
   - You should see the workflow "Update README with latest blog posts"

2. **Manual trigger**

   - If you want to run the workflow immediately:
     - Go to the "Actions" tab
     - Select "Update README with latest blog posts" workflow
     - Click "Run workflow" button
     - Select the branch and click "Run workflow"

3. **Automatic updates**
   - The workflow is configured to run automatically every day at midnight (UTC)
   - It will fetch your latest Medium posts and update your README

## Troubleshooting

- If the workflow fails, check the workflow logs in the Actions tab
- Ensure your Medium username is correct in the workflow file (`@psantana5_`)
- Verify that the comment tags are correctly placed in your README.md file:
  ```
  <!-- MEDIUM-BLOG-POST-LIST:START -->
  <!-- MEDIUM-BLOG-POST-LIST:END -->
  ```

## Customization

You can customize the workflow by editing the `.github/workflows/blog-post-workflow.yml` file:

- Change how often it runs by modifying the cron schedule
- Adjust the number of posts displayed
- Change the format of how posts are displayed

Refer to the [blog-post-workflow documentation](https://github.com/gautamkrishnar/blog-post-workflow) for more options.
