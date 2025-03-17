# Resume Screening Project

## Overview
This project is designed to classify resumes into different job categories based on their content. Users can upload resumes in PDF, DOCX, or TXT format, and the application will predict the category using a pre-trained machine learning model.

## Directory Structure
```
Resume Screening/
├── .ipynb_checkpoints/       # Jupyter Notebook checkpoints
├── AiModel.ipynb             # Jupyter Notebook for model training
├── Data/                      # Directory containing datasets
│   ├── Resume.csv            # Main dataset of resumes
│   ├── UpdatedResumeDataSet.csv # Updated dataset
│   └── gpt_dataset.csv       # Dataset for GPT models
├── img/                       # Directory for images (currently empty)
├── NetworkSecurityEng_Resume.pdf # Example resume in PDF format
├── app.py                    # Main application file
├── clf.pkl                   # Trained classifier model
├── encoder.pkl               # Label encoder for categories
├── health_fitness_resume.pdf  # Example resume in PDF format
└── requirement.txt           # Required packages for the project
```

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/adarshpheonix2810/Resume-Screening.git
   cd Resume Screening
   ```
2. Install the required packages:
   ```bash
   pip install -r requirement.txt
   ```

## Usage
1. Run the application:
   ```bash
   streamlit run app.py
   ```
2. Open your web browser and navigate to `http://localhost:8501`.
3. Upload a resume in PDF, DOCX, or TXT format.
4. The application will display the predicted job category for the uploaded resume.

## Functions
- `cleanResume(txt)`: Cleans the input resume text by removing unwanted characters and formatting.
- `extract_text_from_pdf(file)`: Extracts text from a PDF file.
- `extract_text_from_docx(file)`: Extracts text from a DOCX file.
- `extract_text_from_txt(file)`: Extracts text from a TXT file with encoding handling.
- `handle_file_upload(uploaded_file)`: Handles the file upload and text extraction based on file type.
- `pred(input_resume)`: Predicts the category of the resume based on the cleaned text.

## Project Goals
This project aims to provide an automated solution for classifying resumes into appropriate job categories, enhancing the job application process for candidates and recruiters alike.

## Technologies Used
- Python
- Streamlit
- Scikit-learn
- Pandas
- NumPy
- PyPDF2
- Python-docx

## Model Training
To train the model:
1. Prepare your dataset in the required format (CSV).
2. Use the Jupyter Notebook `AiModel.ipynb` to train the model. Ensure that the dataset is loaded correctly and the model parameters are set as needed.
3. Save the trained model using `pickle` to generate `clf.pkl`, `tfidf.pkl`, and `encoder.pkl` files.

## Testing
To test the application:
1. Ensure that the application is running by executing `streamlit run app.py`.
2. Upload various resumes in different formats and verify the predicted categories.
3. Check for any errors in the console and ensure the application handles them gracefully.

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with clear messages.
4. Push your branch and create a pull request for review.

## Conclusion
This project provides a simple yet effective way to classify resumes, helping job seekers understand the appropriate job categories for their applications.
