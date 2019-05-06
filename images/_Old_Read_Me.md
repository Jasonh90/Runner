
# iOS Requirements

* We have used SnapKit to contraint each of the elements on the screen
* The API integration allows users to currently post and view jobs. They are also able to reload jobs to be upto date with any new updated jobs
* A TableView was used in two screens. One to actually display all the jobs and the other to create jobs.
* A navigation controller allows users to move between screens. Screens are also presented modally in this app.

_The goal of the app, would be to further implement functionality and allow users to actually accept and do jobs with OAuth!_

# Backend Requirements

## API Design:

**_GET /api/jobs/_** - Get all jobs

> This gets all the jobs that is currently available for anyone to grab.

**_POST /api/job/{user_id}/_** - Create a job for a specific user

> Creates a job for runners to see/accept.

**_GET /api/user/{user_id}/_** - Get a specific user

> Get a user's profile information

**_DELETE /api/job/delete/{job_id}/_** - Delete a job BEFORE it’s completed

> Remove a job from the listing. This can be useful if a job is no longer needed or a job was created by accident.

**_DELETE /api/job/finished/{job_id}/_** - Complete a job

> When a job is completed, the job is moved to the poster's job history of past job creations and each user's infomation is changed accordingly. 

**_POST /api/user/{user_id}/_** - Update a user’s information

> If someone wants to change their profile information, this is the endpoint to do so. If no information is provided, nothing is changed. 

**_POST /api/job/{job_id}/edit/_** - Update Job Information

> If someone posted a job, but information needs to be changed, this is the endpoint to do so. If no information is provided, nothing is changed. 

**_POST /api/user/{user_id}/job/{job_id}/_** - Assign a runner to a job

> When a runner wants to accept a job, this is where you send the information of which user to which job. 

**_POST /api/signup/_** - Create a user (signing up)

> Sign a user up if the user doesn't already exist. Password is encrypted.

**_POST /api/login/_** - Logging in for a user

> Log a user into the app. 

**_POST /api/update/session_** - Update session of a user

> Update the session of a user currently on the app. 


## Deployment to Google Cloud:

Deployed on ip address: _35.227.99.222_

# Additional Comments

The iOS github repo had an issue, so it is uploaded in the form of a zip file. As for the next steps of this project, we'd like to have an in-app messaging system that'll allow users to interact with each other without calling on another external app, via phone call which is currently the only option. Also, we would like multiple sign ups such as google sign up and facebook sign up. We'd like to implement actual paypal or venmo payment system, since it's a large part of this app. Upholding the integrity of each user is one of the hardships, but privacy is an important role to this app. These are only a few of the possible further steps to this app. 
