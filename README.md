Bootstrap Single Page UI

A clean, responsive single‑page website built with Bootstrap 5. It includes a sticky navbar with smooth scrolling, a hero section, features, projects/portfolio, about, contact form, and a footer. Great as a starting template for portfolios, product landing pages, or small business sites.

🚀 Demo Preview

Open index.html directly in your browser. No build step required.

Features

Sticky, collapsible Navbar with section links

Smooth scrolling and active link highlight (Scrollspy)

Hero section with CTA button

Features grid using Bootstrap cards

Projects/Portfolio gallery

About section with stats

Contact form (client-side validation ready)

Fully responsive with Bootstrap 5 utilities

Tech Stack
HTML5, CSS3

Bootstrap 5 (via CDN)

Vanilla JS (minimal, included inline)

Getting Started
1) Clone the repo
git clone https://github.com/<your-username>/BootstrapSinglePageUI.git
cd BootstrapSinglePageUI
2) Open locally

Just double‑click index.html (or right‑click → Open With → your browser).

3) Customize

Replace images, text, and links.

Update colors in the <style> block if needed.

Deployment

You can deploy as a static site anywhere:

GitHub Pages (recommended)
git init
# If default branch is master, rename it to main (optional)
git branch -M main


git remote add origin https://github.com/<your-username>/BootstrapSinglePageUI.git
git add .
git commit -m "Initial commit"
# Push depending on your branch name
# If your local branch is 'main':
git push -u origin main
# If your local branch is 'master':
# git push -u origin master

Then go to Settings → Pages in your GitHub repo and set the source to main (or master) branch /root.

Project Structure
BootstrapSinglePageUI/
├── index.html
└── README.md
Contributing

PRs welcome! Please open an issue first to discuss major changes.

License

MIT License – free to use and modify.

index.html
# README.md

## Bootstrap Single Page UI

A clean, responsive single‑page website built with **Bootstrap 5**. It includes a sticky navbar with smooth scrolling, a hero section, features, projects/portfolio, about, contact form, and a footer. Great as a starting template for portfolios, product landing pages, or small business sites.

### 🚀 Demo Preview

Open `index.html` directly in your browser. No build step required.

---

## Features

* Sticky, collapsible **Navbar** with section links
* **Smooth scrolling** and active link highlight (Scrollspy)
* **Hero** section with CTA button
* **Features** grid using Bootstrap cards
* **Projects/Portfolio** gallery
* **About** section with stats
* **Contact** form (client-side validation ready)
* Fully **responsive** with Bootstrap 5 utilities

---

## Tech Stack

* HTML5, CSS3
* [Bootstrap 5](https://getbootstrap.com/) (via CDN)
* Vanilla JS (minimal, included inline)

---

## Getting Started

### 1) Clone the repo

```bash
git clone https://github.com/<your-username>/BootstrapSinglePageUI.git
cd BootstrapSinglePageUI
```

### 2) Open locally

Just double‑click `index.html` (or right‑click → Open With → your browser).

### 3) Customize

* Replace images, text, and links.
* Update colors in the `<style>` block if needed.

---

## Deployment

You can deploy as a static site anywhere:

### GitHub Pages (recommended)

```bash
git init
# If default branch is master, rename it to main (optional)
git branch -M main

git remote add origin https://github.com/<your-username>/BootstrapSinglePageUI.git
git add .
git commit -m "Initial commit"
# Push depending on your branch name
# If your local branch is 'main':
git push -u origin main
# If your local branch is 'master':
# git push -u origin master
```

Then go to **Settings → Pages** in your GitHub repo and set the source to `main` (or `master`) branch `/root`.

---

## Project Structure

```
BootstrapSinglePageUI/
├── index.html
└── README.md
```

---

## Contributing

PRs welcome! Please open an issue first to discuss major changes.

---

## License

MIT License – free to use and modify.

---

# index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Bootstrap Single Page UI</title>
  <meta name="description" content="A clean, responsive Bootstrap 5 single page template" />

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" />

  <!-- Icons (optional) -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css" rel="stylesheet" />

  <style>
    :root {
      --brand: #6c5ce7; /* primary accent */
      --brand-dark: #5a4bd1;
      --text-muted: #6c757d;
    }
    html {
      scroll-behavior: smooth;
    }
    body {
      padding-top: 72px; /* space for fixed navbar */
    }
    .navbar-brand span {
      color: var(--brand);
      font-weight: 700;
    }
    .btn-brand {
      background: var(--brand);
      border: none;
    }
    .btn-brand:hover {
      background: var(--brand-dark);
    }
    .section-title {
      font-weight: 700;
    }
    .hero {
      background: linear-gradient(180deg, rgba(108,92,231,0.08), transparent 60%);
    }
    .feature-icon {
      font-size: 2rem;
    }
    .card-hover:hover {
      transform: translateY(-4px);
      box-shadow: 0 1rem 2rem rgba(0,0,0,.08);
    }
  </style>
</head>
<body data-bs-spy="scroll" data-bs-target="#mainNav" data-bs-offset="80" tabindex="0">
  <!-- Navbar -->
  <nav id="mainNav" class="navbar navbar-expand-lg bg-white shadow-sm fixed-top">
    <div class="container">
      <a class="navbar-brand fw-bold" href="#home">UI<span>One</span></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navMenu" aria-controls="navMenu" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navMenu">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0 gap-lg-3">
          <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="#features">Features</a></li>
          <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
          <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
          <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Hero -->
  <header id="home" class="hero py-5 py-lg-6">
    <div class="container">
      <div class="row align-items-center g-5">
        <div class="col-lg-6">
          <h1 class="display-5 fw-bold mb-3">Build fast with <span class="text-primary">Bootstrap 5</span></h1>
          <p class="lead text-secondary">A minimal, production‑ready single page template with a sticky navbar, smooth scrolling, responsive cards, and a polished contact form.</p>
          <div class="d-flex gap-3 mt-4">
            <a href="#projects" class="btn btn-brand btn-lg text-white">View Projects</a>
            <a href="#contact" class="btn btn-outline-primary btn-lg">Contact</a>
          </div>
        </div>
        <div class="col-lg-6">
          <div class="ratio ratio-16x9 rounded-4 shadow-sm">
            <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Demo" allowfullscreen class="rounded-4"></iframe>
          </div>
        </div>
      </div>
    </div>
  </header>

  <!-- Features -->
  <section id="features" class="py-5">
    <div class="container">
      <h2 class="section-title text-center mb-4">Features</h2>
      <p class="text-center text-muted mb-5">Everything you need to kickstart a beautiful single page.</p>
      <div class="row g-4">
        <div class="col-md-6 col-lg-4">
          <div class="card h-100 border-0 shadow-sm card-hover">
            <div class="card-body">
              <div class="feature-icon text-primary mb-3"><i class="bi bi-lightning-charge-fill"></i></div>
              <h5 class="card-title">Fast & Lightweight</h5>
              <p class="card-text text-muted">No build tools required. Pure HTML + Bootstrap via CDN for instant loads.</p>
            </div>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="card h-100 border-0 shadow-sm card-hover">
            <div class="card-body">
              <div class="feature-icon text-primary mb-3"><i class="bi bi-phone"></i></div>
              <h5 class="card-title">Responsive by Default</h5>
              <p class="card-text text-muted">Looks great on phones, tablets, and desktops with zero extra effort.</p>
            </div>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="card h-100 border-0 shadow-sm card-hover">
            <div class="card-body">
              <div class="feature-icon text-primary mb-3"><i class="bi bi-brush"></i></div>
              <h5 class="card-title">Easy to Customize</h5>
              <p class="card-text text-muted">Tweak colors, content, and layout with utility classes and small CSS.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects / Portfolio -->
  <section id="projects" class="py-5 bg-light">
    <div class="container">
      <div class="d-flex align-items-end justify-content-between mb-4">
        <h2 class="section-title m-0">Projects</h2>
        <a href="#" class="btn btn-sm btn-outline-secondary">See all</a>
      </div>
      <div class="row g-4">
        <div class="col-md-6 col-lg-4">
          <div class="card h-100 border-0 shadow-sm card-hover">
            <img src="https://picsum.photos/seed/p1/600/400" class="card-img-top" alt="Project 1" />
            <div class="card-body">
              <h5 class="card-title">Landing Page</h5>
              <p class="card-text text-muted">A fast marketing page with clear call‑to‑actions and responsive layout.</p>
            </div>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="card h-100 border-0 shadow-sm card-hover">
            <img src="https://picsum.photos/seed/p2/600/400" class="card-img-top" alt="Project 2" />
            <div class="card-body">
              <h5 class="card-title">Portfolio Grid</h5>
              <p class="card-text text-muted">Showcase your work with clean cards and consistent spacing.</p>
            </div>
          </div>
        </div>
        <div class="col-md-6 col-lg-4">
          <div class="card h-100 border-0 shadow-sm card-hover">
            <img src="https://picsum.photos/seed/p3/600/400" class="card-img-top" alt="Project 3" />
            <div class="card-body">
              <h5 class="card-title">Product Section</h5>
              <p class="card-text text-muted">A component‑driven layout you can reuse across pages.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="py-5">
    <div class="container">
      <h2 class="section-title text-center mb-4">About</h2>
      <div class="row g-4 align-items-center">
        <div class="col-lg-6">
          <p class="lead">We build sleek, performant web UIs using modern best practices.</p>
          <p class="text-muted">This template gives you a head start with a thoughtful structure and clean defaults so you can focus on your content, not boilerplate.</p>
          <div class="row text-center mt-4">
            <div class="col-4">
              <h3 class="fw-bold">50+</h3>
              <div class="text-muted small">Projects</div>
            </div>
            <div class="col-4">
              <h3 class="fw-bold">10k+</h3>
              <div class="text-muted small">Users</div>
            </div>
            <div class="col-4">
              <h3 class="fw-bold">5⭐</h3>
              <div class="text-muted small">Ratings</div>
            </div>
          </div>
        </div>
        <div class="col-lg-6">
          <img src="https://picsum.photos/seed/about/800/600" class="img-fluid rounded-4 shadow-sm" alt="About" />
        </div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-5 bg-light">
    <div class="container">
      <h2 class="section-title text-center mb-4">Contact</h2>
      <div class="row justify-content-center">
        <div class="col-md-10 col-lg-8">
          <form class="card border-0 shadow-sm p-4 needs-validation" novalidate>
            <div class="row g-3">
              <div class="col-md-6">
                <label for="name" class="form-label">Name</label>
                <input type="text" id="name" class="form-control" placeholder="Your name" required />
                <div class="invalid-feedback">Please enter your name.</div>
              </div>
              <div class="col-md-6">
                <label for="email" class="form-label">Email</label>
                <input type="email" id="email" class="form-control" placeholder="you@example.com" required />
                <div class="invalid-feedback">Please enter a valid email.</div>
              </div>
              <div class="col-12">
                <label for="subject" class="form-label">Subject</label>
                <input type="text" id="subject" class="form-control" placeholder="How can we help?" />
              </div>
              <div class="col-12">
                <label for="message" class="form-label">Message</label>
                <textarea id="message" class="form-control" rows="5" placeholder="Write your message..." required></textarea>
                <div class="invalid-feedback">Please include a message.</div>
              </div>
            </div>
            <div class="d-flex align-items-center justify-content-between mt-4">
              <small class="text-muted">We'll get back to you within 1–2 business days.</small>
              <button class="btn btn-brand text-white" type="submit">Send Message</button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="py-4 border-top">
    <div class="container d-flex flex-column flex-md-row align-items-center justify-content-between gap-2">
      <div class="text-muted small">© <span id="year"></span> UIOne. All rights reserved.</div>
      <div class="d-flex gap-3">
        <a class="text-muted" href="#"><i class="bi bi-twitter-x"></i></a>
        <a class="text-muted" href="#"><i class="bi bi-github"></i></a>
        <a class="text-muted" href="#"><i class="bi bi-linkedin"></i></a>
      </div>
    </div>
  </footer>

  <!-- Bootstrap JS Bundle (with Popper) -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    // Update year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Bootstrap validation
    (() => {
      const forms = document.querySelectorAll('.needs-validation');
      Array.from(forms).forEach((form) => {
        form.addEventListener('submit', (event) => {
          if (!form.checkValidity()) {
            event.preventDefault();
            event.stopPropagation();
          }
          form.classList.add('was-validated');
        }, false);
      });
    })();
  </script>
</body>
</html>
```
