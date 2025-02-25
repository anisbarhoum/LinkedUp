# LinkedUp - Your Next Co-Founder is One Swipe Away

Finding the right co-founder or job opportunity can be time-consuming and frustrating. Launching your startup ideas is even tougher when you're doing it alone.

That’s where **LinkedUp** comes in.

We built a matchmaking tool that connects LinkedIn users based on their features, interests, and compatibility.

We extracted relevant data from LinkedIn, focusing on education, experience, volunteering, posts, and more to understand users' passions and create vector representations of their profiles and to train the different parts of our scoring function.

Our matching function is a weighted sum of:
- Neural network predictions: Using data scraped from Google News about companies founded by the individuals we identified, we evaluated their success and trained a neural network to predict the potential success of any two individuals.

- Interest similarity: By analyzing user posts, we labeled each post with its primary topic of discussion. For users with multiple posts, we identified their main area of interest by selecting the most frequent topic, helping us understand their passions.

- Education compatibility: To maximize the combined knowledge of each matched pair, we calculated the similarity between their educational backgrounds to ensure complementary expertise.


To learn the weights of our scoring funciton, we performed logistic regression using co-founder data we put aside for testing, we labeled the data with binary labels, indicating success with 1, if their Google News success score was above the median of scores, and 0 otherwise.
