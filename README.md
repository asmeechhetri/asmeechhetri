# Asmee Gallery ✨

A free-to-host, elegant media gallery with a built-in premium paywall. Built with pure HTML, CSS, and JavaScript. No build steps, no servers, no monthly fees.

## 🚀 Live Website
Your website is hosted for free on GitHub Pages:
**https://asmeechhetri.github.io/asmee/**

---

## 📂 How the Website Works

1. **The Gallery**: The homepage loads images from the `images/` folder. The first 18 images (a.jpg to r.jpg) are free and fully visible. The last 6 images (s.jpg to x.jpg) are blurred and locked.
2. **The Lightbox**: Clicking any free image opens a full-screen "screensaver" view with next/previous arrows and keyboard navigation.
3. **The Paywall**: Clicking "Premium" takes the user to a page with a QR code, payment instructions, and a password box.
4. **The Unlock**: When a customer pays, you manually send them the secret password. Once they type it in, the blurred images permanently unlock in their browser.

---

## 🛠️ How to Manage Your Website (Do it all on GitHub)

You do not need to install any software. You can edit everything directly on GitHub.

### 1. How to Change the Secret Password
The current password is **`asmee2026`**.
1. Click on `index.html` in your repo and click the **pencil icon** (Edit).
2. Scroll down to the bottom, inside the `<script>` tag.
3. Find the line: `if (document.getElementById('passcode').value === "asmee2026")`
4. Change `asmee2026` to your new password.
5. Click **Commit changes**.

### 2. How to Change Your Contact Email
Customers need to email you their transaction ID to get the password.
1. Edit `index.html`.
2. Find the text: `<strong>your-email@example.com</strong>`
3. Replace it with your real email address.
4. Commit changes.

### 3. How to Replace the QR Code
Right now, the website uses a placeholder QR code.
1. Take a screenshot of your real payment QR code and save it to your computer (e.g., `qr-code.png`).
2. Go to your GitHub repo and click **Add file** → **Upload files**. Upload your QR image to the main folder.
3. Edit `index.html`.
4. Find this line: `<img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=PayBridgeNP_Payment" alt="QR Code">`
5. Change it to point to your uploaded image: `<img src="qr-code.png" alt="Payment QR Code">`
6. Commit changes.

### 4. How to Add or Remove Images
The website uses a script to automatically load 24 images from the `images/` folder, named exactly from `a.jpg` to `x.jpg` (alphabetical order).
*   **To add images**: Upload more images to the `images/` folder and name them `y.jpg`, `z.jpg`, etc. Then, edit `index.html`, find the line `const totalImages = 24;`, and change `24` to however many images you now have.
*   **To change which images are locked**: Look at the line `const isPremium = i > 18;`. This means any image number higher than 18 will be locked. Change `18` to whichever image number you want the lock to start at.

---

## ⚠️ Important Notes & Limitations

*   **Caching**: If you make changes to the code or images, GitHub Pages sometimes takes 1-2 minutes to update. If you don't see your changes, press **`Ctrl + F5`** (Windows) or **`Cmd + Shift + R`** (Mac) to force your browser to refresh.
*   **Client-Side Security**: This website uses a front-end JavaScript password. It is perfect for keeping casual visitors out, but a tech-savvy user could inspect the page source to find the password. Do not use this to protect highly sensitive or highly expensive content.
*   **Manual Delivery**: This site does not automatically verify payments. You must manually check your eSewa/Khalti/PayBridge account, confirm the Rs 2999 payment, and email the password to the buyer.
*   **Image Sizes**: GitHub has a repository size limit of 1GB. Try to keep your images compressed (under 500KB each) so the site loads fast and doesn't break GitHub's rules.
