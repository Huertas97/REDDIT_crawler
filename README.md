# Reddit Data Extraction Project
 
## Project Description
 
This project is dedicated to extracting and organizing conversation data from Reddit. It utilizes Python and the PRAW (Python Reddit API Wrapper) library to access Reddit data, including posts, comments, and nested replies within specified subreddits. The extracted data is stored in a structured format using JSON files, facilitating further analysis or application development.
 
## Structure of the Data
 
The data is organized into directories named after each subreddit from which data is extracted. Within each subreddit directory, there are JSON files for each post and additional directories for comments and nested replies. Each JSON file contains detailed information about a post or a comment, such as the title, ID, author, content, and metadata regarding scores, timestamps, and more.
 
Below is an example of the folder structure used to store this data:
 
 
- **subreddit_name/**: This directory is named after the subreddit from which the data is extracted (e.g., `python`).
- **post_id_x.json**: Each post from the subreddit is saved as a JSON file named with the post's unique ID.
- **Comments/**: This directory contains JSON files for each comment made on the posts. Each comment file is named using the format `comment_id.json`.
- **Replies/**: Nested within the Comments directory, this folder holds JSON files for replies to comments. Each reply file follows the naming convention `comment_id_reply_id.json`.
 
Each JSON file contains detailed information about its respective post, comment, or reply, including but not limited to the content, author, creation time, and any metadata associated with it.
 
```
Reddit_Data/
└── subreddit_name/
├── post_id_1.json
├── post_id_2.json
├── Comments/
│ ├── post_id_1_comment_id_1.json
│ ├── post_id_1_comment_id_2.json
│ ├── ...
│ └── Replies/
│ ├── comment_id_1_reply_id_1.json
│ ├── comment_id_1_reply_id_2.json
│ └── ...
└── ...
```
 
 
## How to Use
 
### Prerequisites
 
Before running the data extraction script, ensure you have the following installed:
- Python 3.x
- PRAW (Python Reddit API Wrapper)
- tqdm (for progress bars)
 
You can install the necessary Python packages using pip:
 
```bash
pip install praw tqdm
```
 
 
### Authenticating with the Reddit API
You will need to create a Reddit account and obtain the necessary credentials to access the Reddit API. You can do this by following the instructions in the [PRAW documentation](https://praw.readthedocs.io/en/latest/getting_started/authentication.html). The Reddit API requires a client ID, client secret, and user agent to authenticate your requests. This is a really nive video on how to do this: https://www.youtube.com/watch?v=nssOuD9EcVk
 
### Running the Script
Currently the code is in a Jupyter Notebook.
 
## Acknowledgements
 
Special thanks to the Reddit community and the developers of PRAW for making this project possible.