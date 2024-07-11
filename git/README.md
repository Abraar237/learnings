# Repository Setup and Environment Variable Management

## Steps to Hide `.env` File

To ensure your environment variables are not tracked by Git, follow these steps:

1. **Create a `.env` File**

   Create a `.env` file in the root directory of your project and add your environment variables to it:

   ```sh
   echo "DATABASE_URL=your-database-url" > .env
   echo "SECRET_KEY=your-secret-key" >> .env
   echo "API_KEY=your-api-key" >> .env

   # Repository Setup and Commit History Reset

## Steps to Reset Commit History

To reset the commit history of your Git repository and ensure your environment variables are not tracked, follow these steps:

1. **Create a New Orphan Branch**

   Create a new orphan branch which will not have any commit history:

   ```sh
   git checkout --orphan new-branch

   # Add all files to the new branch
   git add -A

   # Commit the changes
   git commit -m "Initial commit"

   # Delete the old branch
   git branch -D master

   # Rename the new branch to master
   git branch -m master

   # Force push the new branch
   git push -f origin master

   # Remove .env from tracking if it was already added
   git rm --cached .env

   # Commit the changes
   git add .gitignore
   git commit -m "Add .env to .gitignore" prepare me. a readme md file for this content