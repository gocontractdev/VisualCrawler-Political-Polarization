# Forschungspraktikum/Projektpraktikum "Online political polarization" > Visual Crawler Group

# Summary

Our task is to create an expert Twitter Crawler that monitors tweets to find posts that have images with matching faces of certain predefined politicians and then to grab replies to that tweet in order to find out how much hate that politician reveive within the Twitter. These results can then result in an index to show how popular or infamous a politician is on socail media.


Our base data set consists of 4 World Powers ( Mr Donald Trump, Mr Valdimir Putin, Mrs. Angela Merkel and Mr Bouris Johnson). We have 3 images of each and each tweet that includes images will be checked against all the photos.

We use a mixture of different techniques to take advantage of Tweeter API. On average, 10 percent of the collected tweets have images. Out of these, usually 2.1 percent are original tweets (from the news channels amd not re-tweets) and have detectable images of our politicians dataset. For these tweets we use a second api called TWARC to just grab related replies. This process is very slow and requires more access keys and process power to work for larger scales. Last but not least, all the replies will be checked to see any cases hate speech is occuring. We have found out that there is at least 5.3 percent of hate speech involved in the politicians' tweets which we call observable hate since it is the amount a machine learning algorithm can detect.

-----------------------------------------------------------------------------------------------------------------------------

# How To

In order to be able to use the Visual Crawler one has to first apply for at least 1 Twitter Stream API key pair. After this, through the following steps Visual Crawler can be deployed and used:


- ## Step 0:  Configurations:
Parameters in parameter.yml file have to be proberly set. Here is the description for each value:

```json

# parameters
consumer_key: 'Twitter consumer key'
consumer_secret_key: 'Twitter secrert'
access_token: 'Access token provided by Twitter'
access_token_key: 'Access key provided by Twitter'
pin_code: 'Twarc pin code'
crawl_directory: './data/crawl' 
process_directory: './data/processed'
dataset_directory: './dataset'
image_directory: './data/images'
log_directory: './data/log'
class_directory: './data/classes'
memory_file: 'history' 
lock_file: 'locker'
face_file: 'facer'
label_file: 'labeler'
parsed_file: 'dataset.csv'
reply_file: 'replies.csv'
class_name: 'Proper class name that represents class directory '
dataset_file: 'labeled_tweets.csv'
max_power: 'Max number of wighted tokens for labeling'
refresh_lock: 'Distance between lock update default is 3'
t_handles: 'array [] of all news handels'
```


-----------------------------------------------------------------------------------------------------------------------------
# More Info

More information about implementation, achievable results and challenges are avaible on our report document sheet via the link below, however due to data protection rules we are not allowed to share and distrubte our datasets.

> Report Doc: https://drive.google.com/file/d/1Fmvtc28Yz5C5yAevarQ9CpJqWgFjs2KM/view?usp=sharing

-----------------------------------------------------------------------------------------------------------------------------

# Contributers

- Amir Reza Javaher Dashti, javaher@uni-koblenz.de

- Marina Rukavitsyna, mrukavitsyna@uni-koblenz.de

- Rahini Chandrasekaran, rahinic@uni-koblenz.de

- Marina Ernst, ernstmargo@uni-koblenz.de

-----------------------------------------------------------------------------------------------------------------------------

# Contacts
This is the Visual Crawler Research Lab Project held by University of Koblenz-Landau in Summer Semester of 2019. The is held by Dr. Oul Han and Frau Ipek Baris as supervisors. In case, you have questions you can stay in touch with the team directly via email:

* Dr. Oul Han, han@uni-koblenz.de

* Ipek Baris, ibaris@uni-koblenz.de

* [Institute for Web Science and Technoloogies (WEST)](https://west.uni-koblenz.de), University of Koblenz-Landau


-----------------------------------------------------------------------------------------------------------------------------

# License
All code is licensed under [MIT License](https://opensource.org/licenses/MIT) .





