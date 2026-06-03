# Cyber Threat Detection Based on ANN Using Event Profiles

## What is this project about?
This was my third year project, and I wanted to work on something in 
cybersecurity since it's a field where AI can make a real difference.

The core problem I was trying to solve: traditional security systems 
generate too many false alarms, which means security analysts waste time 
chasing alerts that aren't real threats. I wanted to see if deep learning 
could do a better job of separating actual threats from noise.

## What I built
An AI-powered SIEM (Security Information and Event Management) system that 
takes raw security event logs, converts them into structured event profiles 
using TF-IDF, and runs them through multiple ML and deep learning models 
to classify whether they're threats or not.

I built a full Django web application on top of this with 5 algorithm 
modules and interactive dashboards showing performance comparisons.

## How the models compared
I benchmarked 7 models against each other and the results were clear:

| Model | Performance |
|-------|-------------|
| LSTM | Best — 94% accuracy from epoch 1 |
| FCNN | Second best |
| Random Forest | Competitive |
| SVM | Moderate |
| KNN | Moderate |
| Naive Bayes | Lower |
| Decision Tree | Lower |

LSTM outperformed everything else across accuracy, precision, recall, 
and F-measure. Starting at 94% from the very first epoch was something 
I didn't fully expect — it showed how well the event profile representation 
worked as input.

## Dataset
- 9,999 security event records
- 80/20 train-test split
- 7,999 records for training, 2,000 for testing

## Tech stack
- **Language:** Python
- **Deep Learning:** LSTM, ANN, MLP, Backpropagation
- **ML Models:** SVM, KNN, Random Forest, Naive Bayes, Decision Tree, FCNN
- **NLP:** TF-IDF for dimensionality reduction
- **Web framework:** Django
- **Libraries:** Scikit-learn, TensorFlow/Keras

## How to run it

```bash
# Clone the repo
git clone https://github.com/vidhisha8/cyber-threat-detection-ann.git
cd cyber-threat-detection-ann

# Install dependencies
pip install -r requirements.txt

# Start the Django server
python manage.py runserver

# Open in browser
# http://127.0.0.1:8000
```

## Challenges I faced
Getting TF-IDF to work well on security log data was tricky — logs have 
a very different structure compared to natural language text. I had to 
experiment quite a bit with preprocessing before the models started 
performing well.

## What I'd improve
Real-time log ingestion would be the obvious next step. I'd also like to 
test this on network intrusion datasets to see how well the approach 

## About me
I'm Vidhisha, a CSE(AIML) graduate from Hyderabad with a focus on AI/ML and NLP.  
Mail: vidhishamantravadi18@gmail.com  
LinkedIn: https://www.linkedin.com/in/mantravadi-vidhisha-a685013a0/

generalizes beyond event logs.

## About me

I'm Vidhisha, a CS graduate from Hyderabad with a focus on AI/ML and NLP.  
📧 vidhishamantravadi18@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/mantravadi-vidhisha)
