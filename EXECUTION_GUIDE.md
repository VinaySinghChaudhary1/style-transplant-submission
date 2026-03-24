# QUES7: The Style Transplant — Complete Execution Guide

## Concept: Gradient Descent in Bauhaus Style

### What You're Building
A geometric visualization of **gradient descent** (an optimization algorithm) rendered authentically in **Bauhaus graphic design** style (1919–1933).

---

## PART 1: UNDERSTAND BAUHAUS GRAMMAR

### Core Rules (Non-Negotiable)
1. **Colors**: Primary colors ONLY — Bauhaus red (#FF0000), blue (#0000FF), yellow (#FFFF00), plus pure black, white, gray
2. **Shapes**: Geometric only — circles, rectangles, triangles, straight lines
3. **Rendering**: Flat, crisp, NO gradients, NO blur, NO soft edges, NO shadows
4. **Typography**: Bold sans-serif only (Helvetica-style). No serifs. No decoration.
5. **Composition**: Asymmetric but balanced on invisible grid. Active use of white space.
6. **Line Quality**: Uniform stroke weight throughout. Every line visible and deliberate.

### Gradient Descent Concept
- **What it is**: An algorithm that finds the minimum of a function by moving in direction of steepest descent
- **Visual components**:
  - Loss surface (high-dimensional, but show as 2D contours)
  - Starting point (high loss)
  - Descent path (trajectory downhill)
  - Convergence point (minimum)
  - Learning rate (step size along path)

### Why This Works
- Gradient descent is inherently geometric and visual
- Loss surface = contours naturally render as Bauhaus concentric shapes
- Descent path = crisp lines and vectors (pure Bauhaus language)
- Color coding helps show high loss (yellow/red) → low loss (blue) progression

---

## PART 2: GENERATE THE IMAGE

### Using DALL-E 3 (via ChatGPT Plus)

1. **Log in**: https://chat.openai.com (requires ChatGPT Plus subscription)

2. **Paste this prompt exactly**:
```
Create a geometric diagram in the Bauhaus style (1919–1933) depicting the mathematical concept of gradient descent. 

VISUAL RULES:
- Use ONLY primary colors (Bauhaus red #FF0000, Bauhaus blue #0000FF, Bauhaus yellow #FFFF00) plus black lines, white background, and gray accents
- All shapes must be geometric: circles, rectangles, triangles, lines only
- No gradients, no blur, no soft edges, no shadows
- Lines must have uniform, crisp stroke weight
- Use bold, sans-serif typography only (Helvetica or geometric typeface style)
- Composition must be asymmetric but balanced on an invisible grid

SUBJECT: 
Depict gradient descent as a descent path on a simplified loss surface. Show:
1. A 2D coordinate system with axes labeled X and Y in bold sans-serif
2. A contoured loss landscape rendered as concentric circles or angular polygons (NOT smooth)
3. A descent path (red arrow or line) showing vector movement downhill from high loss to minimum
4. The loss minimum marked with a blue circle or square at the convergence point
5. Learning rate indicators: small yellow/red arrows showing step size along the path

COMPOSITION:
- Center the descent path; place the loss minimum off-center to create asymmetric tension
- Use negative space actively (white background)
- Integrate the concept label "GRADIENT DESCENT" as a typographic element, not a caption
- Ensure a viewer trained in machine learning immediately recognizes the descent-to-minimum concept

CONSTRAINTS (critical):
- Single frame, no animation
- Minimum 1024px on short side
- No photorealism, no modern gradients, no soft rendering
- Every line must be deliberate and visible
- Authentically Bauhaus: a 1920s designer should recognize this as their work, not a surface imitation
```

3. **Generate variations**: Generate 4 images using DALL-E 3's multi-generation feature

4. **Evaluate for authenticity**:
   - ✓ Sharpest, crispest lines (look for visible pixels, not soft rendering)
   - ✓ Truest primary color saturation
   - ✓ Clearest descent path visible
   - ✓ No gradients or smooth shading anywhere
   - ✓ Most "1920s poster" feeling (not "retro" or "vintage")

5. **Download**: Right-click best image → "Save image" as `.png`
   - Confirm it's at least 1024px on the short side (DALL-E 3 default is 1024×1024)

---

## PART 3: HOST FILES ON GITHUB

### 3a: Create a GitHub Repository

```bash
# Navigate to a clean directory
cd ~/Desktop
mkdir style-transplant-submission
cd style-transplant-submission

# Initialize git
git init
```

### 3b: Add Your Files

```bash
# Copy your downloaded image
cp ~/Downloads/your_image.png ./gradient-descent-bauhaus.png

# Create submission.json (already provided in ques7/)
cp /mnt/d/Download/Nishi_TDSP1/ques7/submission.json ./submission.json

# Verify files exist
ls -la
```

### 3c: Push to GitHub

```bash
# Stage files
git add gradient-descent-bauhaus.png submission.json

# Commit
git commit -m "Gradient Descent in Bauhaus: data science concept rendered in historical visual tradition"

# Add remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/style-transplant-submission.git

# Create branch & push
git branch -M main
git push -u origin main
```

### 3d: Get Raw URLs

Once pushed, construct your submission URLs:

**Image URL:**
```
https://raw.githubusercontent.com/YOUR_USERNAME/style-transplant-submission/main/gradient-descent-bauhaus.png
```

**JSON URL:**
```
https://raw.githubusercontent.com/YOUR_USERNAME/style-transplant-submission/main/submission.json
```

---

## PART 4: VERIFY CORS ACCESSIBILITY

### Test in Private Window

1. **Open Chrome/Firefox in Incognito/Private mode**
2. **Paste image URL** → should display directly (not show login prompt)
3. **Paste JSON URL** → should show JSON raw text (not hidden behind GitHub UI)
4. **Check both load** → If they do, you're CORS-ready

---

## PART 5: SUBMIT

### Submission Format

```
https://raw.githubusercontent.com/YOUR_USERNAME/style-transplant-submission/main/gradient-descent-bauhaus.png  https://raw.githubusercontent.com/YOUR_USERNAME/style-transplant-submission/main/submission.json
```

**Exactly:**
- Image URL first
- Space (no comma)
- JSON URL second
- Test both URLs before submitting

---

## QUALITY CHECKLIST BEFORE SUBMITTING

- [ ] Image is at least 1024px on short side
- [ ] Image uses only Bauhaus primary colors (red, blue, yellow, black, white, gray)
- [ ] Image has NO gradients, NO blur, NO round corners, NO soft edges
- [ ] Image has crisp lines and geometric shapes only
- [ ] Sans-serif typography only; no serifs
- [ ] Gradient descent visualization is clearly recognizable (descent path visible)
- [ ] JSON file has all required fields populated
- [ ] Both URLs are CORS-accessible (test in private window)
- [ ] Image has authentic Bauhaus feel, not generic "retro"

---

## WHAT THE EVALUATOR WILL CHECK

The AI evaluator will independently identify:
1. What visual tradition is depicted (should identify Bauhaus)
2. What data science concept is shown (should identify gradient descent)
3. Anachronisms (should find none if done correctly)
4. Grammar authenticity (does it feel Bauhaus, or just "old"?)
5. Concept discernibility (is optimization/descent clear?)
6. Integration (is concept genuinely fused with tradition, or pasted in?)

**How to score 9.0+:**
- Knowledgeable viewer recognizes BOTH tradition and concept immediately
- No compromises on Bauhaus visual grammar
- Descent-to-minimum logic unmistakable
- Evaluator identifies it as Bauhaus before reading your submission
- No anachronisms detected

---

## BONUS: Publish Email Attribution

If you want your submission attributed to your email address in the exhibition:

```json
"publish_email": true
```

(Already set to `false` in the default JSON, change if desired)
