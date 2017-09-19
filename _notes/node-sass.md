## 
  npm i node-sass -D
  
## Script
  scss will compile style.css by default
  "scss": "node-sass --watch scss -o css"
  "scss": "node-sass --watch scss/main.scss -o css"
  
  "build-css": "node-sass --include-path scss scss/main.scss public/css/main.css"

  --include-path : Path to look for imported files
  --watch scss : watch all .scss files in the scss/ folder and recompile them every time there’s a change.
  -o css : The output folder for our compiled CSS.
