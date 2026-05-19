# Pitch Calendar 2026

A simple HTML calendar view for the 2026 US business trip (May 26 – Jul 21).

## Contents

- `index.src.html` — editable source (plaintext calendar).
- `index.html` — encrypted build output that gets served. Password-gated via [staticrypt](https://github.com/robinmoisson/staticrypt).

## View

Open `index.html` in any modern browser. Password: `fevercoach` (hint shown on page).

## Editing

1. Edit `index.src.html`.
2. Regenerate the encrypted `index.html`:
   ```
   npx staticrypt index.src.html -p fevercoach --short \
     --template-title "Pitch Calendar 2026" \
     --template-instructions "Hint: our app name (all lowercase)" \
     --template-button "Enter" \
     --template-error "Wrong password" \
     -d build && mv build/index.src.html index.html && rmdir build
   ```
3. Commit both files.
