Lesson 3:

Fonts and colors were not showing until I did the following...
(I'm running tailwindcss v3.0.23)

1. Run the following command in the terminal:
   npx tailwindcss init

This creates a file tailwind.config.js in the root directory i.e. same directory as package.json

2. Update the file content as follows:

module.exports = {
content: [
'./public/**/*.{html,js}',
],
theme: {
extend: {},
},
plugins: [],
}

3. Run the following command in the terminal:
   npm run build-css

4. Run the following command in the terminal:
   npx tailwindcss -i ./src/styles.css -o ./public/styles.css --watch

That did it for me!

Further reference: https://tailwindcss.com/docs/installation

====================================

another terminal: 
live-server public/