## Introduction

![> Written with \[StackEdit\](https://stackedit.io/).](https://github.com/a-oh/dreamjobmatch/blob/main/images/Picture1.png?raw=true)

Since Harvard Business Review named data scientist "the sexiest job of the 21st century", job openings under the title 'data scientist' skyrocketed by 650% by the end of 2019. If we include other data related jobs such as data analyst, data engineer, data manager, the graph becomes exponential. By 2025, the annual size of global datasphere is projected to grow to be 4x current size at 175 zettabytes that’s 175 trillion gigabytes. 

The job market looks promising for aspiring data scientists even during the time of pandamic, but at the same time, it makes you wonder which of these positions you should apply for. 

Here, I developed an automated job searcher that delivers curated list of jobs from job aggregator websites that match your skills with a brief summary of the job description.


## Model
### 1. BART-based transformers summarization
![Average Word Count](https://github.com/a-oh/dreamjobmatch/blob/main/images/Picture2.png?raw=true)
- Average word count of job descriptions from Indeed = 650 words
- average word count of job summary = 40 words
- example of the summary

![enter image description here](https://github.com/a-oh/dreamjobmatch/blob/main/images/Screen%20Shot%202021-03-16%20at%206.10.12%20PM.png?raw=true)


### 2. CountVectorizer Cosine Similarity 
![enter image description here](https://github.com/a-oh/dreamjobmatch/blob/main/images/Screen%20Shot%202021-03-16%20at%206.21.40%20PM.png?raw=true)
- although 8/10 job searchers consider salary to be an important factor in deciding the job, the salary estimates vary greatly within the same title and unreliable at predicting the salary
- a better metric for job searchers would be CountVectorizer cosine similarity, which looks at how closely words relate to each other instead of screening for exact keyword match
![enter image description here](https://github.com/a-oh/dreamjobmatch/blob/main/images/Picture5.png?raw=true)

## Output Delivered 

![enter image description here](https://github.com/a-oh/dreamjobmatch/blob/main/images/Picture6.png?raw=true)

