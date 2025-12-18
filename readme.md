Technical Test: Dog Food Landing Page Build
This project is a high-fidelity implementation of a "Dog Food Landing Page" based on provided Figma designs. It is built using a Flask backend to handle routing and asset management, ensuring a professional folder structure and scalable code.

🚀 Setup & Installation
To run this project locally, follow these steps:

1.Ensure Python is installed.

2.Install Flask (if not already installed):

Bash

 pip install flask

3.Project Structure: Ensure your files are organized as follows:

 app.py (The main entry point)

 templates/index.html (The structure)

 static/style.css (The styling)

 static/images/ (Contains all exported PNGs/JPGs)

4.Run the Application:

Bash

python app.py

5.View in Browser: Navigate to http://127.0.0.1:5000.

📁 Project Directory
Plaintext

NUTRITION-SECTION/
├── static/              # CSS and Image assets
│   ├── css/
│   │   └── style.css
│   └── images/          # All Figma exports
├── templates/           # HTML files
│   └── index.html
└── app.py
               # Flask Backend script
               
🛠️ Technical Explanation
1. Backend: Python (Flask)
The project uses Flask to manage the server-side logic.

Routing: app.py uses the @app.route('/') decorator to serve the index.html file from the templates folder.

Static Assets: The url_for('static', filename='...') function is utilized in the HTML to dynamically link the CSS and images, ensuring the paths never break regardless of where the app is hosted.

2. Frontend Structure: HTML5
The page is broken down into semantic sections that match the Figma hierarchy:

Hero Section ("What makes us different"): Uses a three-column grid layout. The center column contains the "Comparison Bowl" image, while the left and right columns contain feature boxes with icons.

Nutrition Stats Section: Uses a flexbox layout to place the textual data (97%, 84%, 92%) on the left and the hero product image on the right.

Benefits Cards: Implements alternating card layouts. One card uses a traditional layout, while the other uses a reverse class to swap the text and image positions.

3. Styling: CSS3 (Flexbox & Grid)
A modern CSS approach was taken to ensure the design is both pixel-perfect and responsive:

CSS Grid: Used for the "What makes us different" section to maintain perfect alignment of the four feature items around the center bowl.

Flexbox: Used for the benefit cards and stat rows to handle alignment and spacing.

Responsive Design: A media query at 992px converts the multi-column grids and flex rows into single-column stacks, ensuring the mobile experience is optimized for handheld devices.

Typography: The Inter font family was imported via Google Fonts to match the clean, modern aesthetic of the Figma file.

4. Image Management
All images were exported from Figma as high-quality PNGs and placed in the /static/images/ directory.

Bowl Comparison: Exported as a single combined asset (bowlComparision.png) to ensure the "half-and-half" visual remains intact.

Icons: Emojis were used as placeholders, but can be easily swapped for SVG exports from Figma for higher resolution.

📝 Conclusion
This build demonstrates a clean separation of concerns by keeping logic (app.py), structure (index.html), and presentation (style.css) in separate files and folders. The use of Flask ensures the project is ready for further development, such as adding dynamic data or e-commerce functionality.