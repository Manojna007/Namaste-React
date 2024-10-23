Here’s the same information formatted as a **README.md** file:

---

# Namaste React Course by Akshay Saini  
## Chapter 02 - Igniting Our App  

### Q: What is NPM?

**A:** NPM (Node Package Manager) is a tool used for managing packages in Node.js projects. It's installed alongside Node.js and provides a command-line interface (CLI) to interact with the NPM Registry—a repository for public and private packages. NPM allows you to add, update, and manage project dependencies.

**Yarn** is an alternative to NPM for package management.

#### How to initialize NPM?

- `npm init`: Initializes a new project and creates a `package.json` file.
- `npm init -y`: Skips the setup step and creates a `package.json` file with default configurations.

---

### Q: What is Parcel/Webpack? Why do we need it?

**A:** Parcel and Webpack are web application bundlers used for compiling and optimizing code for both development and production. These tools help manage assets, improve performance, and reduce configuration complexity.

#### Parcel Features:
- **HMR (Hot Module Replacement)**: Updates modules in real-time without a full reload.
- **File Watcher Algorithm**: Built with C++, tracks file changes.
- **Minification**: Reduces file size by removing unnecessary code.
- **Development and Production Builds**: Easily switch between development and production.
- **Zero Configuration**: Works out-of-the-box without extensive setup.

#### Installation:
```bash
npm install -D parcel
```
The `-D` flag adds Parcel as a development dependency.

#### Commands:
- For development: `npx parcel <entry_point>`
- For production build: `npx parcel build <entry_point>`

---

### Q: What is .parcel-cache?

**A:** The `.parcel-cache` directory stores project build information. It helps Parcel speed up subsequent builds by avoiding redundant parsing and analysis, making the development process faster.

---

### Q: What is npx?

**A:** **npx** is a tool that executes Node.js packages directly from the NPM registry without needing to install them globally. It's available with NPM (version 5.2.0 and higher).

---

### Q: What is the difference between dependencies and devDependencies?

**A:** 
- **Dependencies** are the essential libraries or frameworks your application needs to run (e.g., React, Angular, Express).
- **DevDependencies** are packages only required during development (e.g., Parcel, Webpack, testing libraries). These are not necessary in a production environment.

To install a devDependency, use:
```bash
npm install --save-dev
```

For normal dependencies, use:
```bash
npm install --save
```

---

### Q: What is Tree Shaking?

**A:** Tree shaking is a process used to eliminate unused code from a project during the build process. By removing "dead" code, it optimizes the size of the final bundle, improving performance.

---

### Q: What is Hot Module Replacement (HMR)?

**A:** **Hot Module Replacement (HMR)** allows updates to be made to specific modules in a running application without requiring a full page reload. This speeds up development and preserves application state.

---

### Q: List 5 superpowers of Parcel and describe 3 of them.

**A:**
1. **Hot Module Replacement (HMR)**: Instantly applies code changes without reloading the page.
2. **File Watcher Algorithm**: Monitors files for changes and updates the project automatically.
3. **Minification**: Automatically reduces file size for better performance.
4. Image Optimization
5. Caching in Development

---

### Q: What is .gitignore? What should be added or excluded?

**A:** The `.gitignore` file tells Git which files or directories to ignore when committing changes to a repository. Sensitive files (like **API keys** or **environment variables**) and automatically generated files (like **node_modules**) should be included in `.gitignore`.

**Example:**
```bash
# Ignore system files
.DS_store

# Ignore node modules
node_modules/

# Ignore environment variables
.env
```

---

### Q: What is the difference between package.json and package-lock.json?

**A:**
- **package.json**: This file contains project metadata (name, version, dependencies, etc.) and is required for every Node.js project.
- **package-lock.json**: Automatically generated after an `npm install`. It locks specific versions of dependencies to ensure consistent builds and prevents breaking changes.

**Version Control Symbols**:
- **~**: Allows patch updates (e.g., `~1.2.3` updates to `1.2.x`).
- **^**: Allows minor updates (e.g., `^1.2.3` updates to `1.x.x`).

---

### Q: Why shouldn't you modify package-lock.json?

**A:** Modifying `package-lock.json` manually can create inconsistencies in dependency management. This file ensures that the same versions of packages are installed across different environments and is handled automatically by NPM.

---

### Q: What is node_modules? Should it be pushed to Git?

**A:** The `node_modules` folder contains all of the external packages your project depends on. Since it is auto-generated by running `npm install`, it should **not** be pushed to Git as it contains a large number of files, taking up unnecessary space in your repository.

---

### Q: What is the dist folder?

**A:** The `/dist` folder contains the final, production-ready code. This is the optimized and minified version of your app that gets deployed to the web.

---

### Q: What is Browserslist?

**A:** **Browserslist** is a configuration tool used to specify which browsers your application should support. It's commonly used with tools like **Babel** and **Autoprefixer** to ensure compatibility with specific browser versions.

---

This README provides a structured explanation of key concepts related to modern web development using Parcel, NPM, and Node.js.