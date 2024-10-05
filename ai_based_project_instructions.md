# My process of Writing Cursor PRD

## Step 1 Draft PRD
Fill this [instructions.md](./instructions.md) file:
[instructions.md](./instructions.md)

## Step 2 Research for packages
1. Research and identify optimal tools and packages:
   a. Utilize Claude or ChatGPT (GPT-4) to inquire about the most suitable tools and packages for the project's core use case.
   b. Analyze the AI's recommendations and select the most appropriate options for the project's requirements.
2. Research and Add Package Documentation:
   a. Add documentation of core framework (React, NextJS, Supabase, Tailwind, Stripe etc.) which you will be using in project.
   b. Identify the suggested tool/package for the project's core functionality.
   c. Locate the official documentation for the chosen package.
   d. Add the documentation to Cursor:
      - Open Cursor Composer
      - Select @docs
      - Click "Add New Doc"
      - Paste the package documentation URL
   e. Use the following prompt in Cursor to generate example code:
      @<package_doc> help me build a simple typescript file for <custom functionality>
   f. Copy the generated example code and paste it into the PRD documentation.

## Step 3 Initialize Project Repository and Install Dependencies
1. Create a new Next.js project:
   ```
   npx create-next-app@latest my-app --typescript --tailwind --eslint
   ```
2. Navigate to the project directory:
   ```
   cd my-project
   ```
3. Install shadcn/ui:
   ```
   npx shadcn@latest init
   ```
4. Add necessary components:
   ```
   npx shadcn@latest add button alert-dialog
   ```
   (Repeat this step for other required components)

## Step 4 Design Project Structure

1. Install tree utility:
   ```
   brew install tree
   ```

2. Generate project structure:
   ```
   tree -L 2 -I 'node_modules|.git'
   ```

3. Use ChatGPT (GPT-4) to optimize file structure:
   - Copy entire PRD
   - Prompt: "Based on this project, suggest a minimal file structure."

4. Refine structure with Claude:
   - Paste ChatGPT's response
   - Ask Claude to convert it to Markdown format

## Step 5: Finalize PRD and Start Development

1. Copy paste Claude's markdown output to `instructions.md`

2. Initialize project by giving this prompt to Cursor Composer:
   ```
   # Create <usecase> platform as per instructions.md
   ```

3. Implement first feature, by giving this prompt to Cursor Composer:
   ```
   # Build "1.1 <Feature functionality 1>"
   ```

4. Troubleshoot:
   ```
   # If error occurs, paste in Composer:
   "Error: <paste error log>"
   ```


## Step 6: Enhance UI with v0

Leverage v0 for superior frontend development compared to Cursor.

Enhance UI with v0:
1. Copy Cursor-generated frontend code to v0
2. Prompt: <em>*"Improve UI for <usecase> platform's <home> page showing <content>. Maintain all functionalities and variables. (Remember ONLY change UI, do not change functionalities or variables)"*</em>
3. Paste v0's enhanced frontend code back into Cursor

## Step 7: Deploy on Vercel
<Will add more specific instructions later, work in progress>
1. Create a Vercel account if you don't have one
2. Connect your GitHub repository to Vercel
3. Configure your project settings in Vercel dashboard
4. Trigger a deployment by pushing changes to your main branch
5. Monitor the deployment process in Vercel's dashboard
6. Once deployed, test your live application
7. Set up custom domain (optional)

Note: Detailed steps may vary based on your specific project configuration.