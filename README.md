# Kutko - Angle Learning Web Application

A self-contained, interactive web application designed for elementary school children to explore and learn mathematical angles. Written in HTML, CSS, and vanilla JavaScript.

- **Live URL:** [https://dgrbin.github.io/kutovi/](https://dgrbin.github.io/kutovi/)
- **Repository:** [https://github.com/dgrbin/kutovi](https://github.com/dgrbin/kutovi)

---

## File Structure

- `index.html` - The main self-contained application file containing HTML layout, CSS styling, and JavaScript logic (event handling, SVG drawing, Web Audio synth, canvas confetti, and quiz database).
- `favicon.svg` - Source vector image of the smiling protractor icon.
- `favicon-32x32.png` - Standard rasterized favicon image for browsers.
- `apple-touch-icon.png` - Standard rasterized apple-touch-icon image for iOS Safari and bookmarks.

---

## Modifying the Application

### Code Updates
1. Edit `index.html` directly to modify styles, structure, logic, or quiz questions.
2. The quiz questions database is located at the bottom of the script section under `const quizDatabase`. New questions can be appended following the schema.

### Icon Updates (SVG to PNG)
If you update `favicon.svg` and need to regenerate the PNG outputs on macOS, use the native `sips` (Scriptable Image Processing System) command-line utility:

```bash
# Generate apple-touch-icon (180x180 px)
sips -s format png --resampleWidth 180 favicon.svg --out apple-touch-icon.png

# Generate standard favicon (32x32 px)
sips -s format png --resampleWidth 32 favicon.svg --out favicon-32x32.png
```

---

## Local Development & Testing

Since the application is static, you can test it locally by running a simple HTTP server in the repository directory:

```bash
# Start Python local server
python3 -m http.server 8000
```

Then visit [http://localhost:8000/](http://localhost:8000/) in your web browser.

---

## Deployment

Deploying updates to the live site is handled automatically via GitHub Pages when you push to the `main` branch.

1. Stage and commit changes:
   ```bash
   git add .
   git commit -m "Describe your changes"
   ```
2. Push to GitHub:
   ```bash
   git push origin main
   ```
3. Monitor status (optional):
   ```bash
   gh run list
   ```
   *GitHub Actions will build and deploy the update in approximately 30-40 seconds.*
