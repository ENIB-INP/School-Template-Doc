# README - Using LaTeX, Raleway and git commands on Ubuntu, Windows, and GitHub

## 1️⃣ Installing LaTeX

### On Ubuntu

```bash
sudo apt update
sudo apt install texlive-latex-base texlive-latex-recommended texlive-latex-extra
```

Optional full installation:

```bash
sudo apt install texlive-full
```

Check installation:

```bash
pdflatex --version
```

### On Windows

1. Download and install [MiKTeX](https://miktex.org/download).
2. Choose "Install missing packages on-the-fly".
3. Verify installation:

```cmd
pdflatex --version
```

---

## 2️⃣ Compiling a LaTeX Document

Create `main.tex`:

```latex
\documentclass{article}
\begin{document}
Hello, this is a LaTeX document!
\end{document}
```

Compile:

* Ubuntu: `pdflatex main.tex`
* Windows: `pdflatex main.tex`
* GitHub Actions: automatically via workflow

Output: `main.pdf`

---

## 3️⃣ Installing Raleway

### Ubuntu

```bash
sudo apt install texlive-fonts-extra
```

### Windows (MiKTeX)

1. Open MiKTeX Console.
2. Search for `raleway` and install.

Use Raleway in your document:

```latex
\documentclass{article}
\usepackage{raleway}
\begin{document}
Hello, Raleway!
\end{document}
```

Compile as usual.

✅ **Tip**: Installing Raleway system-wide or in GitHub Actions ensures it is available for all your LaTeX projects.

---

## 4️⃣ Quick Guide for git clone (GitHub Repository)

1. Clone a repository:

```bash
git clone https://github.com/username/repo.git
cd repo
```

2. Install required dependencies if any (for LaTeX projects, ensure TeX Live is installed).

3. Build the LaTeX document locally:

```bash
pdflatex main.tex
```

4. Push changes back to the repository:

```bash
git add .
git commit -m "Update document"
git push
```

✅ **Tip**: You can combine GitHub Actions with pit clone to automatically build and check LaTeX documents on every push.
