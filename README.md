# Interactive Sentiment Analysis Web App

An interactive, client-side web application that analyzes the emotional tone of any given text. The entire analysis runs directly in your browser, meaning your text is never sent to a server.

**[View Live Demo](https://shreyas27092004.github.io/sentiment-analysis-app/)**

![App Screenshot](https://github.com/shreyas27092004/sentiment-analysis-app/blob/main/preview.png)

## Project Overview

This application uses a pre-trained AI model to classify text into **Positive**, **Negative**, or **Neutral** categories. It provides a confidence score for the classification and presents the results in a clean, intuitive interface. The project was conceptually inspired by a lab demonstrating the use of transformer models for NLP tasks. It was built to be a fast, private, and easy-to-use tool for text analysis.

## Features

-   **Client-Side AI**: All processing happens in the browser using Transformers.js.
-   **Nuanced Analysis**: Detects Positive, Negative, and Neutral sentiments.
-   **Dynamic Results**: Visual feedback with a confidence score bar.
-   **Interactive Examples**: Pre-written text samples for quick testing.
-   **Multi-Theme Support**: Includes Light, Dark, and Ocean themes.
-   **Responsive Design**: Works smoothly on both desktop and mobile devices.
-   **Serverless**: No backend is required, making it easy to deploy on static hosts like GitHub Pages.

## Technology Stack

-   **Core Logic**: [Transformers.js](https://huggingface.co/docs/transformers.js/index) by Hugging Face
-   **AI Model**: [Xenova/twitter-roberta-base-sentiment-latest](https://huggingface.co/Xenova/twitter-roberta-base-sentiment-latest) (A fine-tuned model for sentiment analysis)
-   **Frontend**: HTML5, CSS3, Modern JavaScript (ESM)
-   **Styling**: [Tailwind CSS](https://tailwindcss.com/)
-   **Icons**: [Font Awesome](https://fontawesome.com/)
-   **Deployment**: [GitHub Pages](https://pages.github.com/)

## How It Works

The application leverages the power of the **Transformers.js** library to run a sophisticated Natural Language Processing (NLP) model directly in the browser.

1.  **Model Loading**: On the first visit, the browser downloads and caches the `twitter-roberta-base-sentiment-latest` model. Subsequent visits are nearly instant as the model is loaded from the cache.
2.  **User Input**: The text entered by the user is tokenized (broken down into pieces the model can understand) by the library.
3.  **Inference**: The tokenized text is fed to the model, which performs a sentiment analysis inference.
4.  **Displaying Results**: The model outputs a label (`positive`, `negative`, or `neutral`) and a confidence score, which are then used to dynamically update the UI.

The entire process is self-contained on the client-side, which ensures user privacy and reduces server costs to zero.

## Getting Started Locally

To run this project on your local machine:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/shreyas27092004/sentiment-analysis-app.git](https://github.com/shreyas27092004/sentiment-analysis-app.git)
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd sentiment-analysis-app
    ```

3.  **Serve the `index.html` file:**
    Because the project uses JavaScript modules, you need to serve it from a local web server. Opening the `index.html` file directly in the browser will likely cause a CORS error.

    A simple way to do this is with the VS Code **Live Server** extension or by using Python's built-in server:
    ```bash
    python -m http.server
    ```
    Then, open your browser and go to `http://localhost:8000`.

## Acknowledgements

-   This project's core functionality is made possible by the incredible **[Hugging Face Transformers.js](https://huggingface.co/docs/transformers.js/index)** library.
-   The initial concept was inspired by the **Generative AI Use Case: Summarize Dialogue** lab, which demonstrated the power of instruction-based prompting and transformer models.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
