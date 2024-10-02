# B2B Project Freelance (E-Commerce)

## Team Composition

- Our team consists of 4 developers, including myself. We were tasked by the client with developing and deploying an e-commerce website, primarily focused on selling bottles.
- We chose the MERN stack for the project, as it is a technology according to the budget and client usage.

## Challenges Faced

### 1. Skill Set Mismatch:

- Not all team members had the same skill set, particularly when it came to styling. Some of us were comfortable with Tailwind CSS, while others preferred Styled Components.
- **Solution**: To avoid inconsistencies and time delays, we opted to use Tailwind CSS across the project to ensure responsiveness within the given timeframe.

### 2. Design Oversight:

- We created a mobile design in Figma but skipped the desktop version, assuming we could easily adapt it during development.
- **Result**: This proved to be a mistake, as adjusting the design for desktop consumed more time than expected.

## Debugging Issues

- One notable issue occurred when serving static files with Express. We realized that we needed to map a wildcard `*` route to serve the `index.html` file to handle direct URL access correctly.
- **Without this**, typing a URL manually would result in a "Cannot GET [request_url] error.

## AWS Deployment Challenges

### 1. Server Selection:

- During deployment, we initially selected an AWS server located far from us, which led to slow response times and wasted hours troubleshooting.
- **Solution**: I took the initiative to research AWS documentation and learned about Elastic IPs, EC2 instances, and free-tier servers.
  As a Linux user i am familiar about ssh (secure shell) and linux commands, Using this knowledge, I managed the setup more efficiently, configuring domain linking through Nginx, and setting up SSL certificates using Certbot.

### 2. Process Management:

- To keep the server running in the background, we used the PM2 process manager, which streamlined the deployment process.

## Key Takeaways from AWS Deployment

- **Server Performance**: If you have a powerful EC2 instance, there's no need to build and push the frontend separately. However, for lighter instances, it's better to push the bundled frontend (e.g., Vite’s `dist` folder) to GitHub and serve it statically via Express.

- **Security Rules**: Ensure you configure the correct inbound security rules for:

  - HTTPS
  - HTTP
  - SSH
  - Custom-TCP for backend ports

- **Heap Memory Issues**: While building the frontend with Vite, we encountered a "JavaScript heap out of memory" error.
- **Solution**: We attempted to increase Node's memory limit but ultimately solved the issue by building the frontend locally, pushing it to GitHub, and pulling it on AWS.

## My Setup for the Project

- **Tools used**: Neovim, Git, Tmux (for session management), Hyprland (window manager), and Lazygit (a Neovim plugin for easier Git management).

## What I Learned

### 1. AWS Deployment:

- Linking a domain to an EC2 instance.
- Securing the domain with HTTPS.

### 2. Version Control:

- Managing and resolving Git conflicts when working in a team, especially when other's code conflicts with your own.

### 3. Bug Fixing & Collaboration:

- Reading and understanding others' code logic, while also helping guide my teammates on the application workflow.

### 4. CORS & Proxy Usage:

- Gaining a better understanding of when and how to use CORS and proxy setups in a web application.

- when you serve you static folder using express then you need to attach additional get request map to "\*" and return the static index.html on
  response so when ever you hit the url by typing then server we return you the static file otherwise it will give you the cannot get <request_url>
