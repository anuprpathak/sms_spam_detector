# sms_spam_detector

## Overview
Refactor code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, create a Gradio app to host the application, enabling users to test text messages. The application will provide feedback to users, indicating whether the text is classified as spam or not, based on the model's performance.

### Details
1. Create the SMS Classification Function
   - Set the features variable to the text message column of the DataFrame.
   - Set the target variable to the "label" column of the DataFrame.
   - Split data into training and testing and set the test_size to 33%.
   - Build a pipeline to transform the test set to compare to the training set.
   - Fit the model to the transformed training data and return model.

2. Create the SMS Prediction Function
   - Create a variable that will hold the prediction of a new text.
   - Use a conditional statement that determines if the text message is "ham" or “spam”.
     -  If the message is “ham”, the function should return the following message: f'The text message: "{text}", is not spam.'
     -  If the message is spam, the function should return the following message: f'The text message: "{text}", is spam.'
    
3. Create the Gradio Interface Application
   - Create a Gradio Interface application that takes a textbox for the inputs and has a textbox for the output. The textboxes should have labels that describe what each textbox contains.
   - Launch the application and provide the URL to share the application.
