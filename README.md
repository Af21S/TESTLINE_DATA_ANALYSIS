Personalized Student Recommendations

Project Overview

The goal of this project is to analyze quiz performance data and provide personalized recommendations to students preparing for exams. By leveraging historical and current quiz data, the system will generate insights into student performance, identify weak areas, and suggest targeted improvement strategies. This solution will enhance student learning by delivering data-driven guidance tailored to their unique needs.

Key Features

Data Analysis: Extract patterns in student performance based on topics, difficulty levels, and accuracy.

Insights Generation: Identify weak areas, improvement trends, and performance gaps.

Personalized Recommendations: Suggest specific topics, question types, or difficulty levels for improvement.

Student Persona Definition: Categorize students based on their learning patterns and performance.

Setup Instructions

Prerequisites

Python 3.8+

Required Libraries:

pip install pandas numpy requests scikit-learn flask

API Endpoints (Provided by NEET Testline app):

Current Quiz Data API: Provides details of a user’s latest quiz submission.

Historical Quiz Data API: Provides performance data from the last 5 quizzes.

Project Installation and Execution

GET APP : https://play.google.com/store/apps/details?id=practice.test.neet.testline&hl=en_IN

EXTRACT INFO : https://jsonkeeper.com/b/LLQT
HISTORICAL DATA: https://api.jsonserve.com/XgAgFJ

Test API Endpoints

curl http://127.0.0.1:5000/recommendations?user_id=123

Approach Description

Step 1: Data Acquisition & Preprocessing

Fetch data from the provided API endpoints.

Convert JSON responses into structured Pandas DataFrames.

Normalize response maps (key: question ID, value: selected option ID) for analysis.

Step 2: Data Analysis & Pattern Identification

Topic Performance Analysis: Evaluate accuracy trends across different topics.

Difficulty Level Insights: Analyze performance on easy, medium, and hard questions.

Response Accuracy Mapping: Identify frequent mistakes and incorrect responses.

Performance Trends: Track score progression over the last 5 quizzes.

Step 3: Generating Personalized Recommendations

Weak Area Identification: Highlight topics with low accuracy.

Targeted Practice Suggestions: Recommend specific difficulty levels and question types.

Time Management Insights: Advise on pacing strategies based on quiz completion speed.

Step 4: Student Persona Definition

Using performance patterns, categorize students into:

"The Perfectionist" (High Achiever): Consistently high scores, minimal mistakes.

"The Consistent Climber" (Intermediate Performer): Steady improvement, minor inconsistencies.

"The Unstable Explorer" (Struggling Learner): Frequent mistakes, erratic performance.

Step 5: Delivering Insights & Recommendations

Generate a personalized summary for each student.

Provide actionable steps for improvement.

Offer recommendations on study materials and test-taking strategies.
