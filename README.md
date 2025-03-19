# LaTeX Resume Builder

This repository contains LaTeX templates for professional resumes in two popular styles:
- Awesome CV
- ModernCV

The repository is configured with GitHub Actions to automatically build PDF versions of the resumes when changes are pushed.

## Prerequisites

To work with these templates locally, you need:

1. A LaTeX distribution installed on your computer:
   - For Windows: [MiKTeX](https://miktex.org/download)
   - For macOS: [MacTeX](https://www.tug.org/mactex/)
   - For Linux: `texlive` (`sudo apt-get install texlive-full` on Debian/Ubuntu)

2. For Awesome CV, you'll need XeLaTeX which is included in most modern LaTeX distributions

3. Font packages:
   - Font Awesome for icons (included in most LaTeX distributions)
   - For Awesome CV: specific fonts (covered in project files)

## Repository Structure

```
├── awesome-cv-resume.tex      # Resume using Awesome CV template
├── moderncv-resume.tex        # Resume using ModernCV template
├── fonts/                     # Custom fonts for Awesome CV
├── .github/
│   └── workflows/
│       └── build-latex.yml    # GitHub Actions workflow
└── README.md                  # This file
```

## Local Building

### Awesome CV

```bash
xelatex awesome-cv-resume.tex
```

### ModernCV

```bash
pdflatex moderncv-resume.tex
```

## GitHub Actions

The repository is configured with a GitHub Actions workflow that automatically:

1. Builds both resume formats when changes are pushed
2. Makes the PDFs available as build artifacts
3. Optionally deploys the PDFs to GitHub Pages

## Customization

### Personal Information

Edit the personal information section in each file:

For Awesome CV:
```latex
\name{Your}{Name}
\position{Your Position}
\address{Your Address}
...
```

For ModernCV:
```latex
\name{Your}{Name}
\title{Your Position}
\address{Your Address}{}{}
...
```

### Styling

#### Awesome CV

Change the primary color:
```latex
\colorlet{awesome}{awesome-red} % Options: awesome-emerald, awesome-skyblue, awesome-red, awesome-pink, awesome-orange, awesome-nephritis, awesome-concrete, awesome-darknight
```

#### ModernCV

Change the style and color:
```latex
\moderncvstyle{classic} % Options: 'casual' (default), 'classic', 'banking', 'oldstyle' and 'fancy'
\moderncvcolor{blue}    % Options: 'black', 'blue' (default), 'burgundy', 'green', 'grey', 'orange', 'purple' and 'red'
```

## License

This project uses template code from:
- [Awesome CV](https://github.com/posquit0/Awesome-CV) (CC BY-SA 4.0)
- [ModernCV](https://github.com/moderncv/moderncv) (The LaTeX Project Public License 1.3c)
