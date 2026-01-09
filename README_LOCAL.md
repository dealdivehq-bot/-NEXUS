# Run site locally

This repository contains a static site build at the repository root. To serve it locally, use one of the methods below.

1) Python 3 (no install required)
- From the repository root run:
  python3 -m http.server 8000
- Open http://localhost:8000 in your browser.

2) Node (serve)
- Install and run:
  npm install -g serve
  serve -l 5000 .
- Or use npx:
  npx serve -l 5000 .
- Open http://localhost:5000

3) Docker (nginx)
- From repository root run:
  docker run --rm -p 8080:80 -v "$(pwd)":/usr/share/nginx/html:ro nginx
- Open http://localhost:8080

Notes:
- This assumes index.html exists at the repository root and is a complete static build.
- The site uses an inline module script (type="module") and must be served over HTTP (not opened via file://) for modules to load correctly.
