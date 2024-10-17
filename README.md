# Word-Classifier
 This project is based on the extracting specific "Word of Interest" from the sentence provided. The categories are as follows - 
 N/A, Saying Hi and Borrow Money. 

 - **N/A**: This indicates that the sentence is recognized as neither the rest of the three.
 - **Saying Hi**: This indicates that the sentence is approaching with the introductory behaviour.
 - **Borrow Money**: This indicates that the sentence is focused towardds borrowing money.
 - **YouTube Interaction**: This indicates that the sentence is related to Youtube community interaction.

 `Word_Classifier.py` can be used to launch the application. The model will be downloaded upon the initial launch. **IF THE
 MODEL FAILS TO DOWNLOAD, REFER TO [HERE](Model/Model_Data/README.md)**.

 More information on the model can be found [here](Model/README.md).

## Use Case
This model is trained on a very small dataset with only three categories of words to classify with the given sentence. It can be greatly enhanced for larger datasets to perform classfication on multiple sentences. This can work as an extension of sentiment analysis. The sentences can be classified to sentiments, not restricted to only negative or positive. It can be used in many industries like finanace, health and customer service mainly chatbots.

It can majorly help in detecting or classifying user-defined words from long sentences. The main application can be with sentiments and text transcription of the calls made to emergency hotline. It can classify and decide the emergency and can be trained for multiple emergency scenarios aswell. 

# Installation
## Python version
Python 3.x or greater is required.

## Clone the repository
```bash
git clone https://github.com/SAM-DEV007/Word-Classifier.git
cd Word-Classifier
```

## Create a virtual environment
```bash
pip install virtualenv
python -m venv .venv
```

## Activate virtual environment
### Windows
```bash
./venv/Scripts/activate
```
### Linux/Mac
```bash
source venv/bin/activate
```

## Install Dependencies
```bash
pip install -r requirements.txt
```

# Web Integration
Refer to [here](https://github.com/SAM-DEV007/ML-Web-Integration/tree/main/word_classifier) for the file structure and script changes made for Django.

*NOTE: It is strongly recommended to setup bash or python script to download model via Google API from the Google Drive link for the server implementation. **DO NOT RELY ON THE `download_model` FUNCTION GIVEN IN `Word_Classifier.py` AS GOOGLE HAS CHANGED THE METHOD FOR REMOTE DOWNLOAD FROM DRIVE, ESPECIALLY OF LARGE FILES.***

The following steps can be followed **AFTER DOWNLOADING THE MODEL** to integrate the model in a web application:
1. Change `if __name__ == __main__:` to a function, so that the model prediction can be called repeatedly and can be imported to different scritps.
2. `txt = input("Enter your message: ")` can be changed to accept string from the frontend.
3. After modifications, `Word_Classifier.py` can be used as it is for the prediction.

Information on the main functions:

- `txt_arg` is a list of words that can be predicted.
- `model.predict([txt])` returns the array of probabilities of each index to be the predicted result.
- `result` contains the index of the prediction with the highest probability.
- `txt_arg[result]` will generate the predicted result.
