## AiPLA Technical Interview Questions

### Guides

Use your familiar programming language to answer the following questions, e.g. Node.js (TypeScript / JavaScript), JAVA, Python. Do as much as you can.

Time allowed: 30 mins to 45 mins

Allowed submission format: 
1. GitHub link to your source codes
2. Zipped file of your source code, sending to email dev@qdc-aipla.com

Clean codes would be highly appreciated. Suitable level of comments would help demonstrate your capability as a good developer.

—
### Question

This is a simplified format of one of the daily tasks in reality. Students have to answer question paper using the platform. The questions are in MC format.

You are now given a few files of CSV with raw data containing the
- `question_paper.csv`: points out the questions that the students should do, for a given paper
  - `id`: paper ID, unique
  - `Questions`: An array of the (double quoted for parsing in CSV) Question ID, related to `question.csv` - 1st element means the 1st question
  - `UserID`: user's ID
- `submitted_paper.csv`: Shows the submitted answers by the students, corresponding to the question_paper
  - `PaperID`: corresopnding to question_paper.csv 's id
  - `UserID`: user's ID
  - `SubmittedAnswers`: An array of users' selected answer index; -1 means the question is not answered and can be counted as "incorrect"
    - 1st element means the 1st question
- `question.csv`: shows the question ID, question text, topic ID and correct answer index
  - `ID`: the question ID, corresponding to `question_paper`'s Questions column
  - `topicID`: the topic ID of the question
  - `correctAnswer`: the correct answer index of the multiple choice question

CSV files: [data.zip](./data.zip)
Please unzip the data.zip to get the 3 original data set.

Do the following with the data

1. Print the CSV data
2. Calculate the performance of each individual submitted question paper, printing in console or outputting in CSV / JSON format
    - Correctness of each question paper
    - Bonus:
      - Correctness of each question paper, grouped by topic
    - Example, for each question paper, we should know:
      - submitted paper id: e.g. 2
      - paper correctness: e.g. 60%
      - correctness grouped by question's topic ID (bonus)
        - e.g. '4N4': 35%
