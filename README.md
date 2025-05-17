```markdown
# English Level Assessment and Personalized Study Plan Creator

## Project Description

This project is designed to help students assess their English language proficiency and create a personalized study plan. It uses a virtual English teacher to evaluate the student's level (beginner, intermediate, or advanced) based on their responses to multiple-choice questions. The study plan is tailored to the student's level, learning goals (e.g., for work, travel, understanding music/movies, gaming), age, and available study time per week.

## Features

*   **English Level Assessment:** Evaluates the student's English level through a series of multiple-choice questions of increasing difficulty.
*   **Personalized Study Plan:** Generates a study plan based on the student's English level, learning goals, age, and available study time.
*   **Two Communication Modes:**
    *   **Full English:** All communication with the student is in English.
    *   **Half English:** The initial assessment and exercises are in English, while explanations and instructions are in Portuguese.
*   **Virtual Teacher Persona:** Interacts with the student as "Professor Eve," an engaging and supportive virtual English teacher.
*   **Text-to-Speech:** Uses gTTS to provide audio instructions and questions, enhancing the learning experience.
*   **Integration with Gemini AI:** Leverages Google's Gemini AI model for generating responses and personalized study plans.
*   **Adjustable difficulty:** Tests the student with questions from basic to advanced, adjusting the level depending on the student´s answers
*  **Google Userdata Authentication:** Uses Google userdata to store your private API_KEY

## Technologies Used

*   Python
*   Google Colab
*   `google-genai` (for interacting with Google's Gemini AI model)
*   `gTTS` (for text-to-speech)
*   `IPython` (for displaying images and audio in Colab)
*   `colorama` (for colored text output in the console)

## Setup and Installation

1.  **Open in Google Colab:** Open the project notebook in Google Colab.
2.  **Install Dependencies:** Run the following commands in a Colab cell to install the required libraries:

```bash
!pip install google-genai
!pip install gTTS
!pip install IPython
```

3.  **Set up Google API Key:**

    *   Create an API key at the [Google AI Studio](https://makersuite.google.com/app/apikey).
    *   In Google Colab, go to *Tools > Secrets*.
    *   Create a secret with the name `GOOGLE_API_KEY` and paste your API key as the value.
    *   The project code will fetch the API key using the following:

```python
import os
from google.colab import userdata
os.environ['GOOGLE_API_KEY'] = userdata.get('GOOGLE_API_KEY')
```

## Usage

1.  **Run the Notebook:** Execute the cells in the Colab notebook in the order they appear.
2.  **Interact with the Virtual Teacher:** Follow the prompts provided by the virtual English teacher.
3.  **Answer the Questions:** Respond to the multiple-choice questions to assess your English level.
4.  **Receive Personalized Study Plan:** After completing the assessment, you will have the option to receive a personalized study plan based on your level, goals, age, and available study time.

## Project Structure

*   **Code Cells:** The Colab notebook contains code cells with Python code for:
    *   Installing dependencies
    *   Setting up the virtual teacher
    *   Defining functions for text-to-speech, displaying images, and interacting with the Gemini AI model
    *   Implementing the English level assessment
    *   Generating the personalized study plan

*   **Markdown Cells:** The notebook also contains markdown cells with explanations, instructions, and formatting.

## Code Explanation

*   **`mode_identify()`:**  Determines whether to proceed in "full\_english" or "half\_english" mode based on the user's understanding of an initial English prompt.
*   **`texto_para_audio(texto, idioma)`:** Converts text to audio using gTTS.
*   **`print_assistent_response(response)`:** Prints the virtual assistant's responses with a specific color formatting.
*   **`chat_config`:** Defines the system instructions for the Gemini AI model, specifying its role as an English teacher and the evaluation process.
*   The rest of the code handles the interaction with the user, the English level assessment, and the generation of the personalized study plan.

## Contributing

Contributions to this project are welcome! If you find a bug, have a suggestion for improvement, or want to add a new feature, please submit a pull request.


## Credits

*   This project was created by ealbertini66.
*   Special thanks to the developers of `google-genai`, `gTTS`, `IPython`, and `colorama` for providing the tools to make this project possible.

**Disclaimer:**  This project uses AI models for generating responses and study plans. While it strives to provide accurate and helpful information, the results may not always be perfect. Always consult with qualified language instructors for personalized guidance.
```


.
