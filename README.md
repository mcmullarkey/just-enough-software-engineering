# Just Enough Software Engineering

**Author:** Michael Mullarkey

A practical, concise guide to software engineering principles and practices. This book provides *just enough* knowledge to be effective without overwhelming you with unnecessary detail.

## About the Book

This Quarto book covers essential software engineering concepts including:

- Fundamental software engineering principles
- Best practices for writing maintainable code
- Testing and quality assurance
- Effective collaboration and project management
- Making informed technical decisions

## Live Book

The book is automatically published to GitHub Pages: [View the book](https://[username].github.io/just-enough-software-engineering)

*(Replace `[username]` with your GitHub username once deployed)*

## Local Development

### Prerequisites

- Install [Quarto](https://quarto.org/docs/get-started/) (version 1.3 or higher recommended)

### Rendering the Book Locally

```bash
# Render the entire book
quarto render docs/

# Preview with live reload (recommended for development)
quarto preview docs/

# View the rendered book
open docs/_book/index.html
```

## Making Changes

The workflow for updating the book is simple and pain-free:

1. Edit `.qmd` files in the `docs/` directory
2. Test your changes locally: `quarto preview docs/`
3. Commit your changes: `git add docs/` and `git commit -m "your message"`
4. Push to GitHub: `git push`
5. GitHub Actions automatically builds and deploys the updated book
6. Changes appear on GitHub Pages in ~1-2 minutes

## Project Structure

```
just-enough-software-engineering/
├── .github/
│   └── workflows/
│       └── publish.yml     # Auto-deployment workflow
├── docs/                   # All Quarto source files
│   ├── _quarto.yml        # Project configuration
│   ├── index.qmd          # Book homepage/preface
│   ├── intro.qmd          # Introduction chapter
│   ├── summary.qmd        # Summary chapter
│   ├── references.qmd     # References
│   ├── references.bib     # Bibliography (BibTeX)
│   └── _book/             # Local render output (gitignored)
├── .gitignore             # Git ignore patterns
└── README.md              # This file
```

## Deployment

The book uses GitHub Actions for automatic deployment:

- **Source files** live in the `docs/` directory on the `main` branch
- **GitHub Actions** automatically renders the book on every push
- **Rendered output** is deployed to the `gh-pages` branch
- **GitHub Pages** serves the book from the `gh-pages` branch

### Initial GitHub Pages Setup

After your first push, configure GitHub Pages (one-time setup):

1. Go to your repository **Settings** → **Pages**
2. Under "Source", select "Deploy from a branch"
3. Select branch: **gh-pages**, folder: **/ (root)**
4. Click **Save**
5. Your book will be available at: `https://[username].github.io/just-enough-software-engineering`

## Adding Content

To add new chapters:

1. Create a new `.qmd` file in the `docs/` directory (e.g., `docs/new-chapter.qmd`)
2. Add the file to the chapter list in `docs/_quarto.yml`
3. Commit and push - GitHub Actions will handle the rest

## License

[Add your preferred license here]

## Contributing

Contributions, suggestions, and feedback are welcome! Please feel free to open an issue or submit a pull request.