# AI Startup Website – Git Collaboration Project

## 📘 Overview

This project demonstrates a complete Git & GitHub team collaboration workflow. It simulates a real-world environment where two contributors, **Tom** and **Jerry**, independently contribute features using branches and pull requests. The workflow includes:

- Branch creation
- Commit tracking
- Pull requests
- Pulling updates
- Merge conflict resolution
- Final merge into `main`

The project is hosted at:  
🔗 [https://github.com/onisj/ai-startup-website](https://github.com/onisj/ai-startup-website)



## 🧩 Contributors & Branches

| Contributor | Branch Name               | Contribution Description                       |
|-------------|---------------------------|------------------------------------------------|
| Tom         | `update-navigation`       | Adds a basic navigation bar                    |
| Jerry       | `jerry-navigation-boldened` | Boldens nav links and adds a "Blog" section   |
| Jerry       | `add-contact-info`        | Adds contact information in the footer         |



## 🛠️ Tools Used

- Git (CLI)
- GitHub
- Visual Studio Code
- Terminal (macOS)



## ✅ Git & GitHub Workflow Steps

### 1. Git Installed

```bash
git --version
```

📸 *Screenshot: Git version output*

---

### 2. Clone the Repository

```bash
git clone https://github.com/onisj/ai-startup-website
cd ai-startup-website
```

📸 *Screenshot:* ![Cloning the repo](./assets/git_clone.png)

---

### 3. Create and Commit `index.html`

```bash
touch index.html
# Add HTML content using VS Code
git add index.html
git commit -m "Initial commit with base index.html"
git push origin main
```

📸 *Screenshot:* ![Cloning the repo](./assets/initial_git_push.png)



### 4. Tom's Branch – `update-navigation`

```bash
git checkout -b update-navigation
# Tom edits index.html to add a nav bar
git add index.html
git commit -m "Tom: Add basic navigation bar"
git push origin update-navigation
```

📸 *Screenshot:* ![Cloning the repo](./assets/tom_push.png)




### 5. Tom Creates a Pull Request

📸 *Screenshot:* ![Cloning the repo](./assets/pull_request.png)

* GitHub → Create PR for `update-navigation`
* Title: **Tom's Navigation Bar**
* Description: Adds navigation section

📸 *Screenshot: Tom’s pull request page*
![Tom pull request](./assets/tom_pr1.png)
![Tom pull request](./assets/tom_pr2.png)
![Tom pull request](./assets/tom1.png)
![Tom pull request](./assets/tom2.png)
![Tom pull request](./assets/tom3.png)
---

### 6. Jerry's Branch – `jerry-navigation-boldened`

```bash
git checkout main
git pull origin main
git checkout -b jerry-navigation-boldened
# Jerry edits the nav section to bold items and adds Blog
git add index.html
git commit -m "Jerry: Bold nav links and add Blog"
git push origin jerry-navigation-boldened
```

📸 *Screenshot: Jerry’s branch creation and commit*
![Jerry pull request](./assets/jerry1.png)
![Jerry pull request](./assets/jerry2.png)
![Jerry pull request](./assets/jerry3.png)



### 7. Jerry Pulls `main` and Resolves Conflict

```bash
git pull origin main
```

🛠 Conflict occurred in `index.html`. Jerry:

* Opened the file
* Manually resolved using combined content
* Removed conflict markers
* Committed resolution:

```bash
git add index.html
git commit -m "Jerry: Resolve merge conflict with main"
```

📸 *Screenshot: Conflict in terminal + resolved code*

---

### 8. Jerry Creates a Pull Request

* GitHub → Create PR for `jerry-navigation-boldened`
* Title: **Jerry's Navigation Styling**
* Description: Bold text and merged updates from main

📸 *Screenshot: Jerry’s PR and conflict resolution*

![Tom pull request](./assets/last.png)

---

### 9. Merge All PRs

* Merged Tom’s PR first
* Merged Jerry’s PR after conflict resolution
* Then merged `add-contact-info` branch

📸 *Screenshot: PRs showing "Merged" status*
![Jerry pull request](./assets/jerry4.png)
---

### 10. Final Pull and Confirm Merge

```bash
git checkout main
git pull origin main
```

📸 *Screenshot: Final merged `index.html` + `git log --oneline`*

