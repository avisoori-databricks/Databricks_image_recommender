Once a similarity model has been deployed for real-time inference using MLflow serving on Databricks, run the following commands at the commandline (Assuming you have Docker installed. If not, install Docker!)
(app.py is implemented such that the Databricks bearer token is saved as an environment variable for the sake of simplicity but if more caution is desired even during testing, such caution is encouraged )

- First run at the terminal: docker build -f Dockerfile -t app:latest .
- Then run: docker run -p 8501:8501 app:latest
- Then test out your app at: http://localhost:8501/

This process is nicely detailed in the blog by Maël Fabien at: https://maelfabien.github.io/project/Streamlit/#dockerfile
