# Instalace Git + GitHub CLI na Macu

## 1. Homebrew (správce balíčků)

Pokud ještě nemáš, nainstaluj Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Po instalaci přidej do PATH (jen Apple Silicon Macy):

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

---

## 2. Git

```bash
brew install git
```

Ověření:

```bash
git --version
# git version 2.x.x
```

Základní konfigurace (jednou po instalaci):

```bash
git config --global user.name "Tvoje Jméno"
git config --global user.email "tvuj@email.cz"
```

---

## 3. GitHub CLI (gh)

```bash
brew install gh
```

Ověření:

```bash
gh --version
```

Přihlášení k GitHubu:

```bash
gh auth login
```

→ vyber **GitHub.com** → **HTTPS** → **Login with a web browser**

---

## Rychlá kontrola že vše funguje

```bash
git --version && gh auth status
```

Mělo by vypsat verzi gitu a `✓ Logged in to github.com`.
