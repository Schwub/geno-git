# Git Repository erstellen

### Ein leeres Repository erstellen
```bash
git init
```

### Ein Repository klonen

Über SSH:
```bash
git clone git clone ssh://john@example.com/path/to/my-project.git 
```

Oder über HTTP:
```bash
git clone git clone https://example.com/path/to/my-project.git 
```

# Git Aliase

```bash
$ git config --global alias.co checkout
$ git config --global alias.br branch
$ git config --global alias.ci commit
$ git config --global alias.st status
```

# Stagging Area

Ein neues File erstellen:
```bash
touch some_file.md
```

Status einsehen:
```bash
git status
```

Ein File hinzufügen:
```bash
git add <file>
```

Ein Verzeichnis hinzufügen:
```bash
git add <directory>
```

Alle Änderungen hinzufügen:
```bash
git add -A
```

Interactive Staging Session:
```bash
git add -p
```

Unstagging:
```bash
git reset <file>/<folder>
```

# Commit

Einen Commit erstellen:
```bash
git commit
```

Einen Commit mit Kommentar erstellen:
```bash
git commit -m "Commit Message"
```

Alle Änderungen (bereits getrackte Files) committen:
```bash
git commit -a
```

Änderungen zu dem letzten Commit hinzufügen:
```bash
git commit --amend
```

# Stash
Der Stash ist ein Zwischenspeicher in den Änderungen zurückgestellt und daraus wieder auf das Arbeitsverzeichnis angewandt werden können.

Alle Änderungen bis zu dem letzten Commit stashen:
```bash
git stash
```

Änderungen im Stash auf das Arbeitsverzeichnis anwenden und Stash leeren:
```bash
git stash pop
```

Änderungen im Stash auf das Arbeitsverzeichnis anwenden und im Stash behalten:
```bash
git stash apply
```

# Änderungen rückgängig machen

Ein File hinzufügen und einen commit erstellen
```bash
touch first_file.md
git commit -am "Adds first_file"
```

Log einsehen:
```bash
git log --oneline
```

Ein zweites File hinzufügen und Commit erstellen:
```bash
touch second_file.md
git commit -am "Adds second_file"
```

## Git revert

```bash
git log --oneline
```

```bash
git revert <commithash>
```

```bash
git log --oneline
```

## Git reset 

```bash
git checkout <commithash>
```

![checkout](./02%20git-checkout-transparent-kopiera.png)

```bash
git reset <commithash>
```

![reset](./03%20git-reset-transparent-kopiera.png)

```bash
git log --oneline
```

## Git clean

Nicht getrackte files entfernen: 

```bash
git clean -n
```

```bash
git clean -f 
```
# Remotes

Remotes anzeigen:
```bash
git remote
```

Remote hinzufügen:
```bash
git remote add <name> <url>
```

Remote löschen:
```bash
git remote rm <name>
```

# Branches

Alle Branches anzeigen:
```bash
git branch
```

Einen neuen Branch erstellen:
```bash
git branch <branch>
```

Einen Branch löschen:
```bash
git branch -D <branch>
```

Alle Remote Branches anzeigen:
```bash
git branch -a
```

Online Branch erstellen:
```bash
git push <remote> <branch>
```

Auf einen Branch wechseln:
```bash
git checkout <branch>
```

Einen Branch erstellen und auschecken:
```bash
git checkout -b <branch>
```

# Mergen

```bash
git merge <branch>
```

# Git fetch

Alle Änderungen von einer Remote holen:
```bash
git fetch <remote>
```

Alle Änderungen von allen Remotes holen:
```bash
git fetch --all
```

# Git push

Einen Branch in eine Remote pushen:
```bash
git push <remote> <branch>
```

Den aktuellen Branch posten:
```bash
git push <remote>
```

# Git pull

Änderungen aus dem Repository holen:
```bash
git pull
```

Einen speziellen Branch holen:
```bash
git pull <remote> <branch>
```

# Rebasing

Commits aus einem anderen Branch in den Verlauf einfügen:
```bash
git rebase <branch>
```

# Cherry-Picking

Einzelne Commits in den aktuellen Branch einfügen
```bash
git cherry-pick <commit>
```

# Tags vs. Realise

Tags ansehen:
```bash
git tag
```

Tag erstellen:
```bash
git tag v1.0 
```

Tag mit Message erstellen:
```bash
git tag -a v1.0 -m "<message>"
```

Tag pushen:
```bash
git push origin <tag>
```


