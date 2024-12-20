# Disease Prediction System

This project is a Flask-based web application for predicting diseases based on user-inputted symptoms. The system uses a pre-trained Support Vector Classifier (SVC) machine learning model and provides additional details about the predicted disease, including precautions, medications, recommended diets, and workouts.

## Features

- **Disease Prediction**: Predicts diseases based on user symptoms.
- **Detailed Information**: Provides descriptions, precautions, medications, diets, and workout recommendations for the predicted disease.
- **User-Friendly Interface**: Easy-to-use web interface for symptom input and results display.
- **Extendable Dataset**: Supports adding new diseases, symptoms, and related data.

## Dataset

The system uses the following datasets:

- **Symptoms Dataset (`symtoms_df.csv`)**: Contains information about symptoms.
- **Precautions Dataset (`precautions_df.csv`)**: Lists precautions for each disease.
- **Workout Dataset (`workout_df.csv`)**: Provides recommended workouts for diseases.
- **Description Dataset (`description.csv`)**: Contains disease descriptions.
- **Medications Dataset (`medications.csv`)**: Lists medications for diseases.
- **Diets Dataset (`diets.csv`)**: Contains dietary recommendations for diseases.

## Installation

Follow these steps to set up the project:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/disease-prediction-system.git
   cd disease-prediction-system
   ```

2. **Create a virtual environment and install dependencies**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

3. **Prepare datasets**:
   - Place the datasets (`symtoms_df.csv`, `precautions_df.csv`, `workout_df.csv`, `description.csv`, `medications.csv`, `diets.csv`) in the `dataset/` directory.

4. **Load the trained model**:
   - Place the trained SVC model (`svc.pkl`) in the `models/` directory.

5. **Run the application**:
   ```bash
   python app.py
   ```

6. **Access the application**:
   - Open your browser and go to [http://127.0.0.1:5000](http://127.0.0.1:5000).

## Usage

1. Enter symptoms separated by commas in the input box on the home page.
2. Click the "Predict" button to get the disease prediction.
3. View the results, including:
   - Predicted disease
   - Description of the disease
   - Precautions to take
   - Medications
   - Recommended diet
   - Suggested workouts

## File Structure

```
project-directory/
|-- app.py                    # Main Flask application
|-- models/
|   |-- svc.pkl               # Trained Support Vector Classifier model
|-- dataset/
|   |-- symtoms_df.csv        # Symptoms dataset
|   |-- precautions_df.csv    # Precautions dataset
|   |-- workout_df.csv        # Workout dataset
|   |-- description.csv       # Disease descriptions
|   |-- medications.csv       # Medications dataset
|   |-- diets.csv             # Diets dataset
|-- templates/
|   |-- index.html            # Home page
|   |-- about.html            # About page
|   |-- contact.html          # Contact page
|   |-- developer.html        # Developer page
|   |-- blog.html             # Blog page
|-- static/                   # Static assets (CSS, JS, images)
|-- requirements.txt          # Python dependencies
|-- README.md                 # Project documentation
```

## Dependencies

- Flask
- Numpy
- Pandas
- Scikit-learn
- Pickle

Install all dependencies using the `requirements.txt` file:
```bash
pip install -r requirements.txt
```

## Limitations

- Predictions are based on the provided dataset and trained model. Accuracy depends on the quality and comprehensiveness of the dataset.
- The system may not handle misspelled or unknown symptoms effectively.

## Future Improvements

- Add support for more diseases and symptoms.
- Implement a spell checker for symptom inputs.
- Integrate additional datasets for enhanced accuracy.
- Add authentication for secure user access.

## Contributing

Contributions are welcome! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

- Inspired by real-world applications in healthcare technology.
- Special thanks to the creators of the datasets used in this project.

---

Feel free to customize this README file further to reflect any additional details or project-specific information.

