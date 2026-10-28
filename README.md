🍽️ Recipe Recommendation Project 🍽️

This is a simple recipe recommendation project using KNN and cosine similarity, developed in Python with the help of the scikit-learn and numpy libraries. Additionally, it includes recommendation scripts based on RandomForestClassifier and NaiveBayesClassifier models.

The project analyzes the ingredients the user likes and recommends similar recipes, as well as attempts to classify the user’s preferred type of recipe.

📋 Technologies Used...
Python 3.8 or higher
Libraries: scikit-learn, numpy, Flask, Flasgger
⚙️ How to Run the Project Locally
1. Clone the repository

Open your terminal and run;

git clone https:""
cd recomendation_project
2. Create a virtual environment (VENV)

Windows:

python -m venv venv

Mac/Linux:

python3 -m venv venv
3. Activate the virtual environment

(Run this every time you want to activate the VENV)

Windows:

venv\Scripts\activate

Mac/Linux:

source venv/bin/activate
4. Install dependencies

With the VENV activated:

pip install -r requirements.txt
5. Run the project
KNN for Recipe Recommendation:
python service/knn_service.py
Decision Tree for Recipe Recommendation:
python service/decision_tree_service.py
Naive Bayes for Recipe Recommendation:
python service/naiveBayesClassifier.py
Script to generate fake users (toy dataset):
python service/generate_users.py

For better project organization, when running the generate_users script, a /data directory will be automatically created, where the generated JSON file will be stored. If the directory already exists, the JSON file will simply be overwritten.

Each time the script is executed, a new JSON file is generated, always replacing the previous one.

6. Deactivate the virtual environment

Windows:

venv\Scripts\deactivate.bat

Mac/Linux:

deactivate
7. Run the Flask API

Execute:

python app.py

The API will be available at:
👉 http://0.0.0.0:8080

Swagger documentation:
👉 http://0.0.0.0:8080/docs/

🧪 How to Test the Swagger Endpoint
Click on the [POST] /recommendation endpoint
Click on "Try it out"
In the "ingredients" field, send a list like:
{
  "ingredients": ["lemon", "jalapeno pepper", "beef"]
}
Click "Execute"

👉 You will receive a response with the Top 5 recipes that best match your preferences.
