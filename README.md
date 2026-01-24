# Spotify-end-to-end-Data-Engineering

### Introduction
In this project, we will build an ETL(Extract,Transform,Load)pipeline using spotify API on AWS.The pipeline will reterive data from spotify API, Transform it to a desired format, and load it into an AWS Data store.


### Architecture
![Spotify AWS Architecture Diagram](https://github.com/gowthamikinhal146/spotify-end-to-end-data-engineer/blob/main/Spotify_ETL_Architecture.jpg)

 ### Dataset/API
 The Spotify API allows developers to access Spotify data such as playlists, tracks, artists, and audio features, enabling integration of Spotify’s music data into applications and analytics pipelines.[Spotify API](https://developer.spotify.com/documentation/web-api)

### Sevice Used
1. **S3(Simple Storage Services)**:is highly scalable object storage services that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static websites files.

2. **AWS Lambda**: AWS Lambda is a serverless computing services that lets you run your code without managing servers, you can use Lambda to run code in response to events like changes in S3 , DynamoDB,or other AWS Services.

3. **Cloud Watch**:is a monitoring and observability service that collects logs, metrics, and events from AWS resources. It helps track application performance, detect issues, set alarms, and troubleshoot problems in real time.

4. **Glue Crawler**:AWS Glue Crawler automatically scans data stored in S3, identifies the schema, and creates or updates tables in the AWS Glue Data Catalog.

5. **Amazon Athena**: Amazon Athena is a serverless query service that allows you to run SQL queries directly on data stored in Amazon S3 without managing any servers.


 ### Install Pacakages
 ```
 pip install pandas
 pip install numpy
 pip install spotipy
 ```

### Project Execution Flow
Extract Data from API -> Lambda Trigger (every 1 hour) -> Run Extract code -> Store Raw Data -> Trigger Transform Function -> Transform Data and load it -> Query Using Athena.
 
