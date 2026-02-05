
Project: SVM Particle Classification & Data Auditing
Topic: Django Full-Stack Development & ML Integration

📖 Project Overview
BugsOut Systems is a full-stack radiation intelligence platform designed to classify high-energy particles detected by atmospheric Cherenkov telescopes. By bridging the gap between Machine Learning (SVM) and web architecture (Django), the system provides a high-visibility interface for real-time telemetry analysis and data auditing.

The system specifically targets the MAGIC Gamma Ray Telescope Dataset to differentiate between Gamma (Signal) and Hadron (Noise) particles.

🏗️ System Architecture (MVT)
The project follows the Model-View-Template architecture within Django:

Model (The Archive): A database blueprint storing 10 distinct scientific features and the resulting AI prediction.

View (The Logic): The system's "Brain" that handles data cleaning, executes the Support Vector Machine (SVM) algorithm, and classifies the particle.

Template (The Interface): A "Gold & Black" high-visibility terminal designed for laboratory-style interactions.

🧪 Machine Learning Details
The core classifier is built using a Support Vector Machine (SVM) model.

Scientific Features
The model analyzes 11 specific columns from the MAGIC dataset:

fLength: Continuous

fWidth: Continuous

fSize: 10-log of sum of content of all pixels

fConc: Ratio of sum of two highest pixels over fSize

fConc1: Ratio of highest pixel over fSize

fAsym: Distance from highest pixel to center

fM3Long: 3rd root of third moment along major axis

fM3Trans: 3rd root of third moment along minor axis

fAlpha: Angle of major axis with vector to origin

fDist: Distance from origin to center of ellipse

class: g (Gamma / Signal), h (Hadron / Background)

Implementation Steps
Data Cleaning: Handling the Magic04 dataset and encoding classes (Gamma = 1, Hadron = 0).

Scaling: Standardizing features to ensure model accuracy.

Persistence: The trained model and scalar objects are saved as .pkl files for production use.

🚀 Key Features
High-Visibility UI: Uses a "Gold & Glow" theme with CSS variables (--gold-primary) for a modern industrial look.

Radiation Terminal: A customized Django interface for manual telemetry entry.

Official Audit Report: A specialized @media print CSS block that converts the dark web app into a professional white-paper report for printing.

Security: Integrated CSRF protection ensures only authorized BugsOut terminals can communicate with the server.

🛠️ Installation & Setup
Clone the Repository:

Bash
git clone https://github.com/your-username/bugsout-systems.git
cd bugsout-systems
Install Dependencies:

Bash
pip install django pandas scikit-learn joblib matplotlib
Run Migrations:

Bash
python manage.py migrate
Start the Server:

Bash
python manage.py runserver
📊 Testing the System
Use the following telemetry strings in the terminal to verify classification accuracy:

Gamma (Signal): 28.76, 16.03, 2.64, 0.39, 0.20, 23.41, 12.01, 8.12, 2.14, 150.11

Hadron (Noise): 95.82, 25.15, 3.12, ... (Refer to SVMModelBuild.ipynb for more test data)






# ML-and-Django
