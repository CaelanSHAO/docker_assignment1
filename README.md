## Agile Software Practice - Assignment 1.
## Docker Assianment-Agile Software Practice
Name:....JIAYI SHAO .....
Demo:... https://youtu.be/zF5xLbsWSmE...
This repository contains the containerization of themukti-container application ilustrated below.
![](./images/arch.png)
### Database Seeding.
To automate the database initialization, I used a volume in the mongo container (. /seed:/data/db) in the mongo container to mount the prepared seed data files to the MongoDB database folder. This way, when the Mongo container starts, it automatically reads the data in the . /seed directory and writes it to the database.

In addition, depends_on ensures that the movies-api service is started after the mongo and redis services are running to avoid connectivity issues. With this configuration, you don't need to manually add the initial data after deployment.
### M.ulti-Stack
Briefly explain how you support building developmentand production stack options.