# Phase 2

## Question 1: License Plate Coverage

The goal is to create a tool that can automatically detect and blur license plates in images. The image below shows an example of a desirable output.

The tool should meet these quality criteria:

1. **Reliability**: The tool must reliably blur all car license plates in images. A system that only successfully blurs plates 70% of the time is inadequate.

2. **Processing Time**: The tool should not take more than 30 seconds per image, given the potential volume of ads on the site and the need to keep waiting times short for users.

3. **Complete Blurring**: The license plate should be fully blurred without affecting areas outside the plate as much as possible.

### Dataset Description

The data consists of a training and evaluation set with 4,176 and 2,120 images, respectively, captured during the day and night. Since most ad-related images are taken during the day, nighttime images should be excluded from the dataset.

Each image has an accompanying XML file containing the coordinates of the bounding box around the license plate and each character on it. Only one license plate per image is relevant, even if there are multiple plates in the image. 

The test dataset includes 30 images, which will be released 6 hours before the deadline to avoid cheating. the output should include blurred images for each of the 30 test images and performance metrics (IOU Average, MAP, and Recall) on the evaluation dataset.

### Part 1: Data Preparation

Download the images and use libraries such as Keras or PyTorch to read them.

### Part 2: Model Selection

Suggested approaches include classic image processing methods, transfer learning, or object detection models. Choose the model architecture based on data characteristics and task complexity.

Also, fine-tune hyperparameters such as learning rate, network size, and number of epochs to maximize accuracy and efficiency. Remember, inference time is crucial in addition to model accuracy.

Experiment with different models and select the best one for this task. Track both model accuracy and inference time.

### Part 3: Blurring the License Plate

Once the model identifies the license plate, use image processing techniques to blur the specified area.

## Question 2: Amazon Sentiment Analysis

Sentiment Analysis, a subset of Natural Language Processing (NLP), aims to detect the sentiment (positive, negative, neutral) behind a text using machine learning algorithms. This task has broad applications, such as analyzing customer feedback on social media, product reviews, and more.

In this task, we worked with a dataset of Amazon electronic product reviews to extract insights and build a sentiment analysis model.

### Dataset Description

- `overall`: Product rating (1 to 5)
- `vote`: Number of helpful votes
- `verified`: Whether the review is verified
- `reviewTime`: Date of the review
- `reviewerID`: Reviewer ID
- `Asin`: Product ID
- `style`: Dictionary of product details (e.g., color, size)
- `reviewerName`: Reviewer’s name
- `reviewText`: Review text
- `summary`: Review summary
- `unixReviewTime`: Unix timestamp for the review time

### Part 1: Initial Data Analysis

1. Plot the distribution of the `overall` column. Is the dataset balanced? If not, should it be balanced for modeling, and how?
2. Assume ratings of 4-5 are positive, 3 is neutral, and 1-2 are negative. Create word clouds for each category to identify common words. Are there overlapping words in positive and negative categories? Interpret them.
3. Find the top 10 reviewers with the highest total helpful votes. Display each reviewer’s name and total votes.
4. Plot a histogram of the character length of `reviewText`. Do it once with the full dataset and once with filtered data. Decide on a suitable bin size, and comment on whether a character limit should be set for modeling.
5. Identify the top 10 products with the highest count of 5-star reviews. Display them in a table with the brand, product title, and count.
6. Identify the top 10 brands by total reviews. Calculate each brand’s average rating and display in a table.

### Part 2: Satisfaction with Warranty

To assess satisfaction related to warranty:

1. Identify reviews mentioning warranty or similar terms (e.g., “guarantee”) and compute each product’s average rating based on these filtered reviews.
2. Use embeddings (e.g., word2vec or pretrained language model vectors) to find words similar to “warranty” and “guarantee” to capture synonyms and common typos.

### Part 3: Sentiment Analysis Model

Design a model to predict the overall satisfaction (1 to 5) based on `reviewText`. Use additional fields like `summary` or other relevant data if desired, but the review text is essential.
