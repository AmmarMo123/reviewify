# Inspiration
Google reviews are a very valuable insight for any business, however we felt that given the usual amount of reviews per location, it might be too time consuming and inconvenient for many business owners to take full advantage of and understand their reviews. We decided to solve this issue by displaying information in a simpler and more presentable way that will be more useful for business owners to preview.

# What it does
We decided to solve this issue by categorising reviews into "positive", "negative" and "unrelated" subcategories, and providing informative summaries for the categories based on common patterns in the review. The software requires an input from the user with the name of the business, as well as the postal code. This request will be processed by our backend which will take in the information from the Redis database (or add it to the database if it is the first time the business is being searched), which is then by processed by the cohere natural language processing model (nlp) via their api. The cohere insights are then displayed on the website for the user to see a detailed summary of their positive and negative reviews as well as a percentage of the amount of positive, negative and unrelated reviews that customers have left.

# How we built it
For the frontend, we used React, JavaScript, CSS, HTML, Figma and RadixUI. For the backend we used Python. The Google Geocoding API and Google Places API was used to fetch reviews for the given business, which was the stored in the Redis Databases. The Cohere API (Specifically Cohere Summarise, Cohere Classify) was used to categories these reviews, and provide informative summaries. Flask was used to create an API and relay the information to the frontend.

# Challenges we ran into
Integrating flask with react was a challenge, especially trying to have post requests send information from the front end to the backend. It took multiple approaches and some time for us to overcome the challenge. We all got together, took a break and got back into it for 3 hours, and eventually we were able to find a solution that made everything work. Redis database was also very new to all of us and we had no prior experience with Redis which made it difficult to understand the database and its intricacies. However with persistence, we got the database running and structured it for our needs.

# Accomplishments that we're proud of
We are very proud of figuring out the Redis database as we realized how useful and adaptable it is. We are also very happy with the design we created for the frontend. The cohere API was very easy to use and understand, and we loved working with it and are proud of how we tailored it to meet our needs.

# What we learned
The main things we learned from this hackathon is using Redis, Cohere and learning how to integrate frontend and backend. We were all very impressed with how strong the Cohere API is and loved using it for our project. The API was very interesting to use and fit perfectly for the problem that we were trying to solve. Redis was very useful in managing the data we collected, and we noticed the exceptionally fast read and write operations compared to other databases we have used in the past.

# What's next for Reviewify
We loved working together as a team for the first time, we went from strangers to friends in a matter of 24 hours. We are very happy with the amount and level of work that has been done throughout the hackathon. We want to further improve Reviewify in the future by scraping more reviews and storing them in our databases, to make the positive/negative review ratings ratio more accurate. We want to continue experimenting with the Cohere API, as well as have more visualisations, such as showing the user how their review ratings have changed over time (e.g. a span of 5 years) using graphs, helping business owners keep track of the progress of their reviews overtime and use our product longterm.
