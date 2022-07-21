# Email-SMS-Spam-Classifier-Detection-System-

Bulk mails that	are	unnecessary	and	undesirable	can	be classified	as	Spam	Mails.The Email/SMS Spam Classifier uses Multinomial Naive Bayes Algorithm to predict whether a mail is a Spam or Not.The model is build in python 3.9 and gives 97.96% accuracy and 97.56% precision.

The link of the porject website:- https://email-sms-spam-classifier-ml-p.herokuapp.com/

The link of the dataset:- https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset

The Preview of the Webiste:-

1. Spam 
![project1](https://user-images.githubusercontent.com/61287615/179959689-002da783-90f6-4831-a2c3-59a241f189bd.PNG)

2. Not Spam
![project2](https://user-images.githubusercontent.com/61287615/179961042-7c1996a7-7ab2-4510-8b1f-61dd1630ee84.PNG)

The Project involves mainly 4 steps:-

1. Model Building
2. Exploratory Data Analysis(EDA)
3. Data/text Preprocessing:-
   i)convert into Lower Case
   
   ii)Tokenization
   
   iii)Removing special characters
   
   iv)Removing stop words and punctuation
   
    v)Stemming

4.Model Building :- In model building we check for all the Machiene Learning Algorithm and becuase it is an imbalance dataset we will choose the one which gives highest precision and comparable acuuracy. Here Multinomial Naive bayes gives the highest precision 1.0.The model is build in python 3.9 and gives 97.96% accuracy and 97.56% precision. 

The Model is finally deployed on Heroku.com
# Deployment
Some additional files neede to be created for deployment

setup.sh
          
          mkdir -p ~/.streamlit/

          echo "\
          [server]\n\
          port = $PORT\n\
          enableCORS = false\n\
          headless = true\n\
          \n\
          " > ~/.streamlit/config.toml
          
requirements.txt

          streamlit
          nltk
          sklearn     
          
nltk.txt

         stopwords
         punkt
         
.gitignore

          venv
          
Procfile

         web: sh setup.sh && streamlit run app.py
