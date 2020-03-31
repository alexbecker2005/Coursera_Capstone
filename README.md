# Coursera_Capstone - Report
## A new gym for Toronto
#### Project idea and background
My project is based around the question, in which neighbourhood in Toronto one would want to open a new gym. The subject targets individual business people, who would like to own their own company and decided to establish a sports venue and also gym chains, which want to open a new venue in a neighbourhood without a gym.  
#### Data
For this project, I will use, inter alia, data from a Wikipedia page, which presents a list of all postal codes with their boroughs and neighbourhoods. Please find a link here below:
'https://web.archive.org/web/20200303121502/https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M'
Additionally, for the purpose of locating the different postcode areas, I will use the gespatial data of Toronto provided on the Coursera website, which was used in the previous segmentation and clustering assignment. 
Finally, to find out which neighbourhood best fits our purpose, I will use Foursquare data for the different neighbourhoods to see which venues correlate with the existence of a gym in an area. 
#### Methodology
To prepare the data for my use, I took the list of venues from Foursquare, enriched by the names of the neighbourhoods, created dummies for the existence (0 = non existent, 1 = existent) of venues and grouped by the neighbourhoods summing up the dummy variables. Like this, I was able to get the count of each venue category per neighbourhood. Then, I found out the different types of gyms in the Foursquare data ('Gym', 'Gym / Fitness Center', 'Climbing Gym', 'College Gym') and summed them to one column. 
As I wanted to find out the correlation between the existence of gyms and other venues within neighbourhoods, I used polynomial regression to train a model for prediction of number of gyms in an area. For this purpose, I divided the dataframe into neighbourhoods with gyms, to train the model, and neighbourhoods without gyms, to apply the trained model and analyse which neighbourhood should have the most gyms as per prediction. The one with the highest prediction is deemed to be the neighbourhood best fit to open a new gym.
#### Results
The result of above mentioned methodology showed the following:
Kensington Market, Grange Park, Chinatown - 2.009892; St. James Town, Cabbagetown - 1.974261; Oriole, Henry Farm, Fairview - 1.858331;  Trinity, Little Portugal - 1.753322; Harbourfront - 1.586246.
The top 5 neighbourhoods in Toronto where no gym exists, show, that, as per model and correlation to other venues, more than 1.5 gyms would be assumed to be present. 
For the top neighbourhood, Kensington Market, Grange Park, Chinatown, the result even shows more than 2 gyms (2.009892). 
#### Discussion
Even though the model evaluation shows rather a high R-squared score (0.95), the sample size of the neighbourhoods with gyms is small (29 neighbourhoods). Thus, the results should be read with care.
#### Conclusion
Based on the results above, one would want to open a gym in the neighbourhood of Kensington Market, Grange Park, Chinatown in Toronto
