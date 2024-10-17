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
