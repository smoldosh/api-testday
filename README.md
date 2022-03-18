# API testday assignment

Your objective is to create a web service, which provides an REST API to perform CRUD data operations , i.e. creating, reading, updating and deleting shops stored in an SQL database. The structure of the API is defined in the specification, which you can find **[here](https://app.swaggerhub.com/apis/heu-pilsen/testday-api/1.0.1)**. 

The API has to be accessible on a localhost (i.e. **IP 127.0.0.1**) on a **port 8080**. It has to use MariaDb as a storage. Everything you need to set up the db is prepared, the only thing you need to do is to run **docker-compose up** inside the api-testday folder. After that, your database is accessible on the **IP adress 172.17.0.1** on the **port 3306** with following credentials:
- IP: 172.17.0.1
- root password: root
- database: api_testday
- user: api_testday
- password: test123

The database contains a table *Shop* which contains all instances of shops. To access the database, use command docker exec -ti **testday_db mysql -u root -p**.The table **Shop** has following structure:

| Field | Type | Null | Key | Default | Extra |
| :--- | :--- | :--- | :--- | :--- | :--- |
| id | int\(10\) unsigned | NO | PRI | NULL | auto\_increment |
| ownerId | int\(10\) unsigned | NO |  | NULL |  |
| name | varchar\(255\) | NO |  | NULL |  |
| url | varchar\(255\) | YES | UNI | NULL |  |
| email | varchar\(50\) | NO |  | NULL |  |
| orderPhone | varchar\(20\) | YES |  | NULL |  |
| phone | varchar\(20\) | YES |  | NULL |  |
| importUrl | varchar\(255\) | YES |  | NULL |  |
| status | enum\('new','ppc','free','blocked','to\_delete'\) | NO |  | NULL |  |
| deactivationReason | enum\('admin','bad-delivery','bad-price','bad-url','condition','debtor','not-active','no-credit','not-xml','shop'\) | YES |  | NULL |  |
| termsAccepted | tinyint\(1\) unsigned | NO |  | 0 |  |
| questionnaireRecipient | varchar\(50\) | YES |  | NULL |  |
| questionnaireSender | varchar\(50\) | YES |  | NULL |  |
| certifiedAgreementDate | timestamp | YES |  | NULL |  |
| customerId | char\(36\) | YES |  | NULL |  |
| createdAt | timestamp | YES |  | NULL |  |
| updatedAt | timestamp | YES |  | NULL |  |

It is up to you what language you want to use to complete this assignment. If you are skilled with PHP, do not hesitate to use it. If you prefer Python, it is a viable option as well.

Before submiting, write a **README** file with information about your service(what technologies you use and why, how to run it locally, what improvement you would do etc.), preferably in english.

Once you feel you are done with your work, publish your code on a Github (or any other Git service) and provide us a link.
