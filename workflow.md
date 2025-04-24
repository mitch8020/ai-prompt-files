## Intro

Start by editing the tech_specs.md file based on your web app high level specifications. Don't get too detailed yet. Just think of high level stuff of what your app needs to do.

Then, copy the tech_specs.md text into a chat as an initial prompt. Don't link the file. Just copy and paste the raw text. (Optional) Attach ONE relevant image of the 'look and feel' that you're trying to go for so that it has a reference image.

## UI Iteration
Once you're satisfied with the first few pages, add some subtle interaction animations (if needed).

You can then proceed to creating more pages for your web app.

## UI to Web App

Start by prompting the AI to something along this statement:

"You are a senior product manager working on a saas app."

**FOR UI/FRONTEND

"If I want to turn this into a proper web app in [YOUR TECH STACK], what UI components should I create? (Don't generate any code yet, just think and plan for now, and also just focus on minimal amount of UI components)."

**FOR BACKEND

"Write a detailed plan/spec for a saas app I want to build where I can [APP DESCRIPTION]. Ask me questions to help fill out any gaps in what this app should be."

"Write this in the format of a PRD using .md file format."

Copy the text that it generates over to a prd.md file in the .cursor folder.

## Setup your Project

Create a new boilerplate project in your chosen tech stack. Add all the dependencies that you need and install them (At least the ones that you know you'll need).

Next prompt:

"Come up with a step by step to-do list to build this out in .md format (todo.md)."

"I've setup a new project in the @[YOUR FOLDER] folder. Now, let's build the first component of AppLayout & screenLayout in layout folder first (But make sure you read the [YOUR TECH STACK] project structure to make sure things are in the right place). After implementing each component, add a ✅ in @prd.md file so we can track what's left to do."

## Working through the To Do list

Once you've reached this point, just prompt the AI to read the prd.md and the todo.md files and complete each task ONE AT A TIME! (VERY IMPORTANT)

Ask the AI to create tests for each section of code or feature that it creates. Do this for every single step. Run the tests incrementally until all of the tests have been successfully passed.

"Write tests to make sure this app work as expected." Fix the tests or fix the code.

## Best Practices

1. Rate Limit all API Endpoints
2. use row level security always (RLS)
3. captcha on all auth routes/signup pages
4. if using hosting solution like vercel, enable attack challenge on their WAF
- check your code before deploying (i figured this was implied but i guess vibes are a bit wild nowadays??)

- ask your AI helper to look for each of the above and help you implement

+ ask it if it can see any possible other attack vectors and how you can mitigate