<!-- markdownlint-disable MD033 -->
<!-- markdownlint-disable MD041 -->

<p align="center">
  <img style="border-radius: 5px;" src="https://raw.githubusercontent.com/orbitbits/smog/refs/heads/main/.github/logo/compact/smog-git.svg" alt="smog" width="180"/>
</p>

<h1 align="center">Turn data into unreadable noise.</h1>

AUR packaging for **Smog**

---

## 🔧 Maintainer workflow (AUR)

### Build package with script `main.sh`

```sh
./main.sh build
```

### Install package local with script `main.sh` (test)

```sh
./main.sh install
```

> Note: Always test with `./main.sh install` before pushing in AUR.

### Clean all build with script `main.sh`

```sh
./main.sh clean
```

---

## 🚀 Initial publish to AUR

```sh
./main.sh publish
```

---

## 🔁 Updating package when a new GitHub tag is released

Example: new version `0.3.2`

1 - Update version in `main.sh`:

```sh
# edit main.sh
PKGVER=0.3.2
```

2 - Recalculate checksums:

```sh
./main.sh check
```

3 - Rebuild:

```sh
./main.sh build
```

4 - Commit and push:

```sh
./main.sh publish
```

Done.

---

## 📂 Templates in this repository

* `PKGBUILD.template` — AUR build recipe
* `smog.install.template` — post-install message

---

## 🧠 Notes

* This repository does **not** contain the source code.
* The PKGBUILD downloads the source directly from GitHub releases.
* Always test with `./main.sh install` before pushing.

---

## ✅ Maintainer best practices

Never edit `.SRCINFO` manually.
Never update `sha256sums` by hand.
Always use:

```sh
./main.sh check
```

## Official page

[https://orbitbits.com/smog/](https://orbitbits.com/smog/)

---

© [OrbitBits](https://orbitbits.com) - All rights reserved.
