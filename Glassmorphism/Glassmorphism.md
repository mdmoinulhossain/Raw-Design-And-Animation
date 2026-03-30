Here’s a **complete, ready-to-use layout** that combines:

* ✅ Glassmorphism card
* ✅ Gradient + glowing background
* ✅ Smooth animation
* ✅ Centered layout

You can copy-paste and run directly.

---

## 💎 Full Working Example (HTML + CSS)

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Glass UI</title>

<style>
/* RESET */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

/* 🌌 BACKGROUND */
body {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;

  background: #0b0f1a;
  overflow: hidden;
}

/* Animated gradient blobs */
body::before,
body::after {
  content: "";
  position: absolute;
  width: 500px;
  height: 500px;
  border-radius: 50%;
  filter: blur(120px);
  animation: moveBlob 12s infinite alternate ease-in-out;
}

body::before {
  background: rgba(0, 153, 255, 0.4);
  top: 10%;
  left: 10%;
}

body::after {
  background: rgba(255, 0, 150, 0.35);
  bottom: 10%;
  right: 10%;
}

/* Extra center glow */
.bg-glow {
  position: absolute;
  width: 400px;
  height: 400px;
  background: rgba(0, 255, 200, 0.2);
  border-radius: 50%;
  filter: blur(120px);
  animation: moveBlob 10s infinite alternate-reverse ease-in-out;
}

/* ✨ GLASS CARD */
.glass-card {
  width: 260px;
  padding: 20px;
  text-align: center;

  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(20px) saturate(180%);
  -webkit-backdrop-filter: blur(20px) saturate(180%);

  border-radius: 20px;
  border: 1px solid rgba(255, 255, 255, 0.25);

  box-shadow:
    0 8px 32px rgba(0, 0, 0, 0.2),
    inset 0 1px 0 rgba(255, 255, 255, 0.5);

  position: relative;
  z-index: 2;

  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* Hover effect */
.glass-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow:
    0 15px 40px rgba(0, 0, 0, 0.3),
    inset 0 1px 0 rgba(255, 255, 255, 0.6);
}

/* Shine effect */
.glass-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;

  background: linear-gradient(
    120deg,
    transparent,
    rgba(255,255,255,0.5),
    transparent
  );

  transition: 0.5s;
}

.glass-card:hover::before {
  left: 100%;
}

/* CONTENT */
.glass-card h2 {
  color: #fff;
  margin-bottom: 10px;
}

.glass-card p {
  color: rgba(255,255,255,0.8);
  font-size: 14px;
}

/* 🔄 ANIMATION */
@keyframes moveBlob {
  0% {
    transform: translate(0, 0) scale(1);
  }
  100% {
    transform: translate(50px, -50px) scale(1.2);
  }
}

</style>
</head>

<body>

<div class="bg-glow"></div>

<div class="glass-card">
  <h2>Glass Card</h2>
  <p>Modern glassmorphism UI with animated gradient background.</p>
</div>

</body>
</html>
```

---

## 🔥 What You Get

* Background **moves slowly** → feels alive
* Blur reacts perfectly → **true glass effect**
* Card hover → subtle premium interaction
* Works great for:

  * Portfolio
  * SaaS landing page
  * Consultancy website (your use case 👌)

---

## 🚀 Next Step (if you want)

I can upgrade this into:

* Multiple cards (grid layout)
* Navbar + hero section
* Convert into **React / Inertia component**
* Add scroll animations (AOS / Framer Motion)

Just tell me what direction you want.
