## Getting Started

Follow this guide to get setup for development on this app. DM Sunny if you have any questions.

### Prerequisites

Before getting started, ensure you have the following installed on your system:

1. **Git** – Install it from [git-scm.com](https://git-scm.com/).
2. **Visual Studio Code (VSCode)** – The required IDE for this project. Install it from [code.visualstudio.com](https://code.visualstudio.com/).
3. **Docker Desktop** – Required for running the development container. Install it from [docker.com](https://www.docker.com/products/docker-desktop/).

If you need help with the above steps, each link includes better instructions than I could ever write on how to install those programs. 

### Installation

#### 1. Install the Dev Containers Extension in VSCode

VSCode uses an extension called **Dev Containers** to work inside a Docker container. To install it:

- Open VSCode.
- Go to the **Extensions Marketplace** (`Ctrl+Shift+X` or `Cmd+Shift+X` on macOS).
- Search for **Dev Containers** and install it.

#### 2. Clone the Repository

Open a terminal and run:

```bash
git clone https://github.com/aparm539/MRU_CHEM_Inventory_Management.git
```

Once complete, navigate into the project directory:

```bash
cd MRU_CHEM_Inventory_Management
```

#### 3. Open Docker Desktop

Docker is required to run the development environment. Start Docker by:

- Opening the **Docker Desktop** application.
- Ensuring it is running without errors.

#### 4. Open the Project in VSCode

- Open **VSCode**.
- Click **File > Open Folder** and select the cloned project directory.
- If prompted, click **Reopen in Container**. If not prompted, open the Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P` on macOS) and select **Dev Containers: Reopen in Container**.
- Wait for the container to build and set up the environment. This may take a few minutes.

#### 5. Move into the Frontend Directory

Once the container is running, navigate to the frontend folder inside the terminal:

```bash
cd client
```

#### 6. Install Dependencies

The frontend project uses npm to manage dependencies. To install them, run:

```bash
npm install
```

This command downloads and installs all necessary libraries for the project.

### Development

#### 1. Start the Development Server

To start the application in development mode with Hot Module Replacement (HMR), run:

```bash
npm run dev
```

#### 2. Access the Application

Once the server is running, open your browser and go to:

```
http://localhost:5173
```

This URL will load the application, and any code changes you make will be reflected in real time.

### Troubleshooting

- If you don't see the **Reopen in Container** prompt, ensure the **Dev Containers** extension is installed and Docker is running.
- If `npm install` fails, check if Node.js is installed correctly by running `node -v` and `npm -v`.
- If the application doesn’t start, verify that you are in the `client` directory before running `npm run dev`.

### Working with Git and GitHub

**Setting Up Git Credentials**

To authenticate Git with GitHub using the GitHub CLI, run the following command:
```bash
gh auth login
```
Follow the prompts to select GitHub as your host, choose HTTPS authentication, and authenticate using your browser.

**Creating a New Branch for Feature Development**

When working on a new feature, always create a new branch from the main branch:
```bash
git checkout main

git pull origin main

git checkout -b feature-branch-name
```
Replace feature-branch-name with a descriptive name for your feature.

**Step-by-Step Guide for Pushing and Creating a Pull Request**

1. Make Your Changes – Implement the feature or fix in your branch.

2. Stage and Commit Changes – Once your changes are ready, run:
```bash
git add .
git commit -m "Brief description of the changes"
```
3. Pull Latest Changes – Ensure your branch is up to date before pushing:

```bash
git pull origin main --rebase
```
4. Push to GitHub – Send your changes to the remote repository:
```bash
git push origin feature-branch-name
```
5. Open a Pull Request (PR) –

  - Go to the GitHub repository.
  - Navigate to the Pull Requests tab.
  - Click New Pull Request.
  - Select your branch and compare it with main.
  - Add a descriptive title and details about your changes.
  - Request reviews from everyone else on the project.
  - Submit the PR.

6. Address Feedback & Merge – If there are review comments, update your branch and push changes again. Once approved, merge the PR into main.

