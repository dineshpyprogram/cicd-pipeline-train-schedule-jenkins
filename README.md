# cicd-pipeline-train-schedule-jenkins

This is a simple train schedule app written using nodejs. It is intended to be used as a sample application for a series of hands-on learning activities.

## Running the app

You need a Java JDK 7 or later to run the build. You can run the build like this:

    ./gradlew build

You can run the app with:

    ./gradlew npm_start

Once it is running, you can access it in a browser at [http://localhost:3000](http://localhost:3000)
This line is added to test code build trigger in jenkins via webhook setup using the api token key from the github. The repository is forked and from there I am making the changes to trigger the build in jenkins. To enable jenkins to call github repo to build a project we need to give it a token from the github settings of my profile. developerr settings and then create access token. generate the token. save it or copy it and go to jenkins and configure system to configure the github server and give the github webhook credentials as the secret text option in the add credentials dialog box. Then go to new item and create a freestyle project and select the github as general source and git as SCM and give the github link as source. Build trigger as github hook trigger for scm and build step use as gradle or gradle wrapper and then post build archive the zip file.
