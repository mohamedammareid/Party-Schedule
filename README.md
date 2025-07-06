**🎉 Party Schedule Generator README 🎉**

Welcome to the **Yearly Party Schedule Generator**, a dynamic, client-side application that randomly and fairly distributes people into monthly parties hosted in different houses. Built with HTML, TailwindCSS, and vanilla JavaScript, you’ll love how easy it is to configure categories, people counts, and houses, then generate and export your schedule!

---

## 📝 Table of Contents

1. [Features](#-features)
2. [Usage](#-usage)
3. [Configuration Options](#-configuration-options)
4. [Validation & Error Handling](#-validation--error-handling)
5. [Export & Reset](#-export--reset)
6. [Customization](#-customization)
7. [Security Considerations](#-security-considerations)
8. [License](#-license)

---

## 🚀 Features

* **Dynamic Form**: Choose 2–5 categories, total people (6–500), and number of houses (1–20).
* **Fair Distribution**: Round-robin algorithm ensures each person attends before repeats.
* **Randomized Shuffle**: Fisher–Yates shuffle for true random order of both people and houses.
* **Toggle Views**: Switch between **Cards** and **Table** displays at any time.
* **PDF Export**: Instantly download your schedule as a printable PDF (`html2pdf.js`).
* **Responsive Design**: TailwindCSS ensures mobile-friendly layout.
* **Live Validation**: Instant input checks with clear error messages.
* **Reset Capability**: Easily start over without reloading the page.

---

## 📋 Usage

1. Open the web page.
2. Fill in the **Number of Categories**, **Category Names**, **Total People**, **Number of Houses**, and **Party Count per Category**.
3. Click **Generate Schedule**.
4. Use **View as Cards** / **View as Table** to switch layouts.
5. Click **Download as PDF** to export.
6. Click **Reset** to start a new configuration.

---

## ⚙️ Configuration Options

| Setting                  | Type   | Range / Default    | Description                                       |
| ------------------------ | ------ | ------------------ | ------------------------------------------------- |
| Number of Categories     | Number | 2–5 (default: 2)   | How many distinct groups of people.               |
| Category Names           | String | A–Z, max 10 ch.    | Alphanumeric labels for each category.            |
| Total Number of People   | Number | 6–500 (default:40) | Total pool of participants.                       |
| Number of Houses         | Number | 1–20 (default:5)   | How many hosting locations.                       |
| Party Count per Category | Number | 1–50 (default:10)  | Number of attendees from each category per month. |

---

## ✔️ Validation & Error Handling

* All inputs are validated on-the-fly.
* Error messages appear under invalid fields.
* Prevents empty names, duplicate categories, out-of-range numbers, and party-size > total people.

---

## 📤 Export & Reset

* **Download as PDF**: Uses **html2pdf.js** with A4 portrait layout. Exports the **Table View** for consistency.
* **Reset**: Clears schedule, hides controls, and returns to the form without page reload.

---

## 🎨 Customization

* **Styling**: Modify TailwindCSS classes directly in the `<style>` block or extend via a custom CSS file.
* **Locale**: Translate month names by updating the `MONTH_NAMES` array.
* **Shuffle Algorithm**: Swap `shuffleArray` with a cryptographic RNG (e.g., `crypto.getRandomValues`).

---

## 🔒 Security Considerations

* **Input Sanitization**: `sanitizeString` removes `<>'"&` to prevent basic XSS.
* **Minimize innerHTML**: Prefer `createElement`/`textContent` for dynamic content to avoid injection.
* **CDN Integrity**: For production, add Subresource Integrity (SRI) attributes or self-host assets.

---
