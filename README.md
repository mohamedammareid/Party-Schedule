# 🎉 Yearly Party Schedule Generator

A fair and random event schedule generator that distributes participants into monthly events, complete with host locations and PDF export! 📅🏠

---

## 🚀 Features

- **Custom Categories:** Define 2–5 categories (e.g. A, B, C) for your participants.  
- **Flexible Counts:** Set total people (6–500) and per‐event counts per category (1–50).  
- **Randomized Hosts:** Assign 1–20 host locations in a rotating, random fashion.  
- **Fair Distribution:** Ensures everyone meets new people each month, minimizing repeats.  
- **Two Views:** Switch between **Card View** and **Table View** for easy browsing.  
- **PDF Export:** Download your full yearly schedule as a neatly formatted PDF. 📄✨  

---

## ⚙️ Usage

1. **Open** `(https://mohamedammareid.github.io/Party-Schedule/)`.
2. **Enter**:
   - **Number of Categories** (2–5)  
   - **Category Names** (up to 10 characters, A–Z & 0–9)  
   - **Total People** (6–500)  
   - **Host Locations** (1–20)  
   - **Per‐Event Counts** for each category (1–50)  
3. **Click** **Generate Schedule**.  
4. **View** your results in Cards or Table mode.  
5. **Download PDF** to save or share.  

---

## 🎨 Customization

- **Styling:** Modify the TailwindCSS classes in `<style>` to adjust colors, spacing, or fonts.  
- **Fonts:** Change the Google Font in the `<head>` (default: _Inter_).  
- **Logic:** Tweak the scheduling logic in `generateYearlySchedule()` for your own fairness rules.  

---

## 👩‍💻 How It Works

1. **People & Houses Creation**  
   - Splits total people evenly into categories, assigns unique IDs (e.g. `A-001`, `B-012`).  
   - Generates host locations (`Location-1`, `Location-2`, …).  
2. **Shuffle & Assign**  
   - Randomly shuffles people and houses.  
   - For each month, picks participants by lowest participation and lowest prior meetings.  
3. **Track & Render**  
   - Tracks who’s met whom to minimize repeats.  
   - Renders as responsive cards or accessible tables.  

---
