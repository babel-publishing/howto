# babel

```
babel (n).

1. a non-ivory tower.

2. somewhere everyone is welcome.

3. science minus academia.
```

# howto

### 1. make a repo on github

  * Click New Repo.
  * We'll call it `babel-publishing/howto` but you can call yours anything.
  * Then click "Initialize this repository with a README". We'll set ours to use The Unlicense.

### 2. clone it locally

```bash
git clone https://github.com/babel-publishing/howto
cd howto
```

### 3. maybe there's some code

```bash
mkdir code

echo "print('Hello, world.')" > code/__main__.py

echo '__pycache__' > .gitignore

cat > code/README.md << EOF
# babel

This is the code.
EOF

chmod +x code/__main__.py

## run the code, for fun
python code/

git add .
git commit -m "Add code."
```

### 4. maybe there's a paper

```bash
mkdir paper

cat > paper/main.tex << "EOF"
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{Paper}
\author{Babel Publishing}
\date{Hindsight, 2020}

\begin{document}

\maketitle

\section{Introduction}

\end{document}
EOF

git add paper
git commit -m "Add paper."
```

### 5. suppose both of those are happily on github
```bash
git push
```

### 6. overleaf (optional)

Now, if you want to work on the paper somewhere else, like overleaf.

> Overleaf -> New Project -> Import from Github

Now make some changes in overleaf.

Suppose we change the title from "Paper" to "Papyrus",
because our mind still hasn't fully left academia and
we have a deep need to sound fancy. Then click

> Menu -> GitHub

It should say

> "This project is synced with the GitHub repository at babel-publishing/howto"
> No new commits in GitHub since last merge.

and then there should be a button that says

> Push Overleaf changes to GitHub

Click that. It'll ask you for a commit message.

Write "Change paper title from overleaf" and click ok.

If you then `git pull` from your local copy of the project
and run `git log`, you should see the new commit.

Now let's make a change from git and see how to pull it into overleaf.

Let's change the section header and add some content.

```latex
\section{$\Phi$ \textrm{@} \texttt{lux}}

In the beginning, Euler said

\begin{equation}
e^{i \pi} + 1 = 0
\end{equation}

\noindent
and it was good.
```

Now add the changes, commit, and push.

```bash
git add .
git commit -m "Fiat lux."
git push
```

Go back to overleaf and click Menu -> GitHub again.

You'll see the new commit from GitHub.

Click "Pull GitHub changes into Overleaf."

Congratulations, you're published.

Let's go do science.
