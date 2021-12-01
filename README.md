# Video-Streaming

## Table of Contents

-- [Description](#description)

-- [Usage](#usage)

-- [Infra diagram](#diagram)

-- [Deployment](#deployment)

## Description

This application is designed to be a video upload and streaming service specifically for independent film/TV show creators to upload their work and for industry professionals to find new projects to fund. Unaffiliated viewers can view and provide likes/dislikes to videos posted, providing industry professionals with a barometer of public interest in a work as well. The overall goal of the project is to get more industry eyes on up-and-coming independent creators.

It was created using a MERN-stack setup:

- React as the front-end view
  - React-Bootstrap for styling
- GraphQL with Node.js and Express.js servers
- MongoDB and Mongoose ODM for database storage
- Heroku for deployment
- JWT (JSON WebTokens) for user authentication

Here are screenshots of the app's primary pages:

The Main Page:

![Main Page Screenshot](assets/prequelmainpage.PNG)

The Individual Video Page:

![Video Page Screenshot](assets/prequelvideopage.PNG)

Link to the deployment: [ec2 Deployment](http://ec2-35-83-249-21.us-west-2.compute.amazonaws.com:3000)

## Usage

Navigate to the link provided above to get to the deployed app. Once there, an account can be created, videos can be uploaded, and all videos on the site can be seen on the main page with the most recently uploaded video being at the top of the list. The profile page will display all of the videos that the logged-in user, personally, has uploaded. A user can also delete any video they have uploaded from the database at their leisure. Individual videos can be liked or disliked by a user, with a counter incrementing on the video screen.

When visiting the site, you can create your own account or use a dummy account provided here that has a few uploaded videos already, just to demo the functionality of the site:

    Email: test@test.test
    Password: password03

## Diagram

![Infra diagram](assets/infra.PNG)

- Frontend base on react run in 3000 port
- Backend base on express.js runs in 3001 port
- Database runs on Mongo Altas, which is maintained by Mongo AWS account.

## Deployment

`ssh -i ~/.ssh/video-provider-wj8664.pem ec2-user@35.83.249.21`
`cd video-provider-demo && export NODE_OPTIONS=--openssl-legacy-provider`
`npm run develop`
