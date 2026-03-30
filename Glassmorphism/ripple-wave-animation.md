Got it — you want that **“phone calling / ripple wave” border animation** 🔔 around your CTA.

This effect is basically:

* multiple **expanding borders (waves)**
* fading out while scaling
* loop animation

---

## 🔥 Final Result (Drop-in Code)

Wrap your `<p>` inside a container:

```html
<div class="call-border">
  <p class="offer-text">
    ⚡ OFFER WILL END SOON — এখনই সুযোগ নিন!
  </p>
</div>
```

---

## 🎯 CSS (Phone Call Wave Border Animation)

```css
.call-border {
  position: relative;
  display: inline-block;
}

/* Your original style (slightly improved) */
.offer-text {
  position: relative;
  z-index: 2;

  text-align: center;
  color: #ffdd00;
  font-weight: bold;
  font-size: 14px;

  background: linear-gradient(135deg,#1a1500,#2a2000);
  border: 1px solid #ffdd00;
  padding: 10px 20px;
  border-radius: 6px;
}

/* 🔔 Wave animation layers */
.call-border::before,
.call-border::after {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: 8px;
  border: 2px solid rgba(255, 221, 0, 0.7);

  animation: waveBorder 2s infinite;
}

/* second wave delay */
.call-border::after {
  animation-delay: 1s;
}

/* 🔁 Animation */
@keyframes waveBorder {
  0% {
    transform: scale(1);
    opacity: 0.8;
  }
  70% {
    transform: scale(1.6);
    opacity: 0;
  }
  100% {
    opacity: 0;
  }
}
```

---

## 💡 What This Does

* Creates **2 expanding borders**
* They scale out like a **phone ringing pulse**
* Opacity fades → gives clean glow effect
* Loops infinitely

---

## 🔥 Pro Upgrade (Looks MUCH Better)

Add glow:

```css
.call-border::before,
.call-border::after {
  box-shadow: 0 0 15px rgba(255, 221, 0, 0.6);
}
```

---

## ⚡ Optional Variations

### Faster pulse

```css
animation: waveBorder 1.5s infinite;
```

### Stronger glow

```css
border: 2px solid rgba(255, 221, 0, 1);
```

### Green version (match your UI)

```css
border: 2px solid rgba(0, 255, 150, 0.7);
box-shadow: 0 0 15px rgba(0,255,150,0.6);
```

---

## 🚀 If you want next level

I can turn this into:

* Button with **hover + click ripple**
* **Tailwind version**
* **React / Inertia component**
* Or sync it with your **scroll animation**

Just say 👍
