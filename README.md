# Twitter-Sentiment-Analysis
This project performs sentiment analysis on tweets using the Sentiment140 dataset. The project includes data preprocessing, feature extraction using TF-IDF, and classification using Logistic Regression.

## Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/your-repository-name.git
    ```

2. **Navigate to the project directory:**
    ```sh
    cd your-repository-name
    ```

3. **Install the required libraries:**
    ```sh
    pip install -r requirements.txt
    ```

4. **Set up Kaggle API key:**
    - Go to [Kaggle](https://www.kaggle.com) and log in.
    - Go to `My Account` and find the `API` section.
    - Click `Create New API Token` to download the `kaggle.json` file.
    - Place the `kaggle.json` file in the appropriate directory.

    ```sh
    mkdir -p ~/.kaggle
    cp /path/to/kaggle.json ~/.kaggle/
    chmod 600 ~/.kaggle/kaggle.json
    ```

## Usage

1. **Download the Sentiment140 dataset using Kaggle:**
    ```sh
    kaggle datasets download -d kazanova/sentiment140
    ```

2. **Extract the dataset:**
    ```python
    from zipfile import ZipFile

    dataset = 'sentiment140.zip'
    with ZipFile(dataset, 'r') as zip_ref:
        zip_ref.extractall('sentiment140_extracted')
    ```

3. **Run the Jupyter Notebook:**
    - Open Jupyter Notebook.
    - Navigate to the project directory and open `Twitter Sentiment Analysis.ipynb`.

4. **Follow the steps in the notebook:**
    - Load the dataset.
    - Preprocess the text data (cleaning, stemming, removing stopwords).
    - Perform TF-IDF vectorization.
    - Split the data into training and testing sets.
    - Train the Logistic Regression model.
    - Predict the sentiment of tweets and evaluate the model.

## Project Structure

- `Twitter Sentiment Analysis.ipynb`: Jupyter Notebook containing the complete analysis and code.
- `README.md`: Project description and usage instructions.
- `requirements.txt`: List of required libraries for the project.
