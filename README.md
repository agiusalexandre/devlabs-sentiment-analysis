# devlabs-sentiment-analysis
Analyzing audio files : Use Amazon Transcribe and Amazon Comprehend to analyze customer sentiment

# AWS services leveraged
Amazon Transcribe is an automatic speech recognition (ASR) service that makes it easy for developers to add speech-to-text capability to their applications. Using the Amazon Transcribe API, you can transcribe audio files stored in Amazon S3 into text transcripts.

Amazon Comprehend analyzes text and tells you what it finds, starting with the language, from Afrikaans to Yoruba, with 98 more in between. It can identify different types of entities (people, places, brands, products, and so forth), key phrases, sentiment (positive, negative, mixed, or neutral), and extract key phrases, all from text in English or Spanish. Finally, the Amazon Comprehend topic modeling service extracts topics from large sets of documents for analysis or topic-based grouping.

AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume – there is no charge when your code is not running.

AWS Step Functions makes it easy to coordinate the components of distributed applications and microservices using visual workflows.

Amazon Connect is a self-service, cloud-based contact center service that makes it easy for any business to deliver better customer service at lower cost. Amazon connect produces Call Recordings between caller and Agent interactions.


# Solution overview
The architecture is broadly divided into these components, as the following diagram illustrates:

Audio Transcript Storage → Amazon S3 bucket
Orchestration component and business logic component → AWS Step Functions and AWS Lambda
Transcribing component → Amazon Transcribe
Sentiment analysis component → Amazon Comprehend
Notification component → SNS Topic
Amazon Comprehend → Entity, sentiment, key phrases, and language output into an Amazon S3 bucket
AWS Glue maintains the database catalogue and database table structure. Amazon Athena queries data in Amazon S3 using the AWS Glue database catalogue.
Amazon QuickSight analyzes call recording and performs sentiment, and performs a key phrases analysis of caller-agent interactions.

