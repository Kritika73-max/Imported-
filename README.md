# ⚡ GITFOLIO

A beginner-friendly developer portfolio template with a retro-futuristic cyberpunk aesthetic. Fork it, customize it, and deploy it — no design skills required. (Promise!)

## 🚀 Quick Start

### Prerequisites

Before getting started, make sure you have:

* [Node.js](https://nodejs.org/) installed
* npm installed (included with Node.js)
* A GitHub account if you plan to deploy your portfolio using GitHub Pages

### Option 1: Use This Template (Recommended)

1. Click the **"Use this template"** button at the top of this repository.
2. Select **"Create a new repository"**.
3. Give your repository a name, such as `my-portfolio`.
4. Clone your new repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

5. Install the dependencies:

```bash
npm install
```

6. Start the development server:

```bash
npm run dev
```

7. Open http://localhost:3000 in your browser.

### Option 2: Fork & Clone

If you want to contribute to GITFOLIO or create your own fork:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
npm install
npm run dev
```

Open http://localhost:3000 to view the portfolio locally.

---

## ✏️ Customize Your Portfolio

All of your portfolio content lives in **`app/page.tsx`**, making it easy to personalize the template.

### 1. Update Your Name or Brand

Find the navigation section and replace `GITFOLIO` with your name or brand:

```tsx
<Link href="/">
  YOUR_NAME
</Link>
```

### 2. Add Your Projects

Find the `ProjectCard` components and replace the example projects with your own:

```tsx
<ProjectCard
  title="MY_PROJECT"
  description="What this project does and why it's awesome."
  tags={["REACT", "TYPESCRIPT", "API"]}
  color="cyan"
  href="https://github.com/you/project"
/>
```

Available colors include:

```text
cyan
fuchsia
purple
yellow
```

### 3. Write Your Bio

Find the `// ABOUT_ME` section and add your developer story:

```tsx
<p>
  Your developer journey goes here. What drives you?
  What are you passionate about building?
</p>
```

### 4. Update Your Skills

Customize the `STACK_TRACE` and `PROTOCOLS` lists with your actual technologies, skills, and interests.

### 5. Add Your Photo

Place your profile photo in the `/public` folder as `me.png`.

Alternatively, update the filename in `app/page.tsx` if you want to use a different filename.

### 6. Update Your Social Links

Find the footer section and replace the example links with your own:

```tsx
<SocialLink
  href="https://github.com/YOUR_USERNAME"
  label="GITHUB"
/>

<SocialLink
  href="https://linkedin.com/in/YOUR_USERNAME"
  label="LINKEDIN"
/>

<SocialLink
  href="https://twitter.com/YOUR_USERNAME"
  label="TWITTER"
/>
```

---

## 🌐 Deploy to GitHub Pages

GITFOLIO includes a GitHub Actions workflow for deploying your portfolio to GitHub Pages.

### Step 1: Update the Base Path

In `app/page.tsx`, update the `basePath` value with your repository name:

```tsx
const basePath =
  process.env.NODE_ENV === "production"
    ? "/YOUR_REPO_NAME"
    : "";
```

### Step 2: Enable GitHub Pages

1. Open your repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **GitHub Actions**.
4. Push your changes to the `main` branch.
5. GitHub Actions will build and deploy your portfolio automatically.

Your portfolio will be available at:

```text
https://YOUR_USERNAME.github.io/YOUR_REPO_NAME
```

---

## 🧪 Test Your Changes Locally

Before deploying your portfolio, you can check that the project builds successfully:

```bash
npm run lint
npm run build
```

To start the production server locally after building:

```bash
npm run start
```

---

## 📁 Project Structure

```text
├── app/
│   ├── page.tsx        # Main portfolio content
│   ├── layout.tsx      # Root layout and metadata
│   └── globals.css     # Global styles
├── public/
│   └── me.png          # Profile photo
├── .github/
│   └── workflows/      # GitHub Pages deployment
└── next.config.ts      # Next.js configuration
```

---

## 🎨 Design Features

* **Cyberpunk Aesthetic** — Neon cyan, fuchsia, and yellow accents on a deep-space background
* **Terminal Typography** — Monospaced fonts for a developer-focused look
* **Interactive Elements** — Glowing hover effects, pulsing status indicators, and smooth animations
* **Responsive Design** — Optimized for mobile, tablet, and desktop
* **Accessible** — Uses semantic HTML and accessible color contrast

---

## 🛠️ Tech Stack

| Technology                                    | Version | Purpose                         |
| --------------------------------------------- | ------: | ------------------------------- |
| [Next.js](https://nextjs.org/)                |      16 | React framework with App Router |
| [React](https://react.dev/)                   |      19 | UI library                      |
| [Tailwind CSS](https://tailwindcss.com/)      |       4 | Utility-first styling           |
| [TypeScript](https://www.typescriptlang.org/) |       5 | Type safety                     |

---

## 📝 Available Scripts

| Command         | Description                      |
| --------------- | -------------------------------- |
| `npm run dev`   | Start the development server     |
| `npm run build` | Build the project for production |
| `npm run start` | Start the production server      |
| `npm run lint`  | Run ESLint                       |

---

## 🤝 Contributing

Contributions are welcome! If you find a bug, spot an issue in the documentation, or have an idea for improving GITFOLIO, feel free to contribute.

### Contribution Workflow

1. Fork the repository.
2. Clone your fork locally.
3. Create a new branch:

```bash
git checkout -b feature/your-feature
```

4. Make your changes.
5. Test your changes locally.
6. Commit your changes:

```bash
git commit -m "Improve README documentation"
```

7. Push your branch:

```bash
git push origin feature/your-feature
```

8. Open a Pull Request and describe what you changed.

For additional contribution guidelines, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 🐛 Troubleshooting

### The development server will not start

Make sure Node.js and npm are installed:

```bash
node --version
npm --version
```

Then reinstall the project dependencies:

```bash
rm -rf node_modules
npm install
npm run dev
```

On Windows, you can delete the `node_modules` folder manually and then run:

```bash
npm install
npm run dev
```

### The portfolio looks different after deployment

If assets or links are not loading correctly on GitHub Pages, verify that the `basePath` matches your repository name.

---

## 📄 License

This project is open source under the [MIT License](LICENSE). Feel free to use it for your own portfolio.

---

## 💜 Credits

Made with ❤️ by [GitHub for Beginners](https://gh.io/gfb) and [GitHub Copilot](https://gh.io/gfb-copilot).
