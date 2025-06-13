# Movie-recommendation-system-with-sentimental-analysis


The key focus of the project is sentimental analysis for the reviews of the movie selected. The are 5 different sentiments in the dataset(positive, somewhat positive, neutral, somewhat negative, negative). The novelity of the project is it has a dedicated formula for calculating the ratings for the movie based on the sentiments.

<img width="253" alt="image" src="https://github.com/user-attachments/assets/c93a324b-2560-405e-af22-73a0086aa229">

The model we seleted is SVC which performed with an accuracy of 0.85. The architecure used for the project is 

<img width="261" alt="image" src="https://github.com/user-attachments/assets/caf0463c-394b-4583-83ff-bb680153d063">

For web scraping the reviews we have used beautifulsoup to extract from imdb website.
# How to run project
To run the project install all the required modules from requirements.txt file. Get your api key from tmdb api and replace it in the main.py file. The nlp_model.pkl and transform.pkl file is already loaded with the model. If you want to make any changes to them delete the pkl files and do relevant changes in Movie_Reviews_Classification.ipynb file and run it. To run the project go to the terminal and give the command 
python3/python main.py. Then we have used flask for developing the webapplication. Go to the url http://127.0.0.1:5000.


