# Tutorial Map

## Introduction (10-20 mins)

* What is operability - take this from Matthew Skelton book and recommend it.
* Ask for stories of operability testing.
* Why is it important for testers
  * Improving observability, control and understanding
  * Better test environments
  * A way of improving your testing, providing better information to stakeholders.

## Run the App, Describe the Architecture (20-40 mins)

* Get everyone up and running, however we should try and get everyone to this point before we start the day. Download little on the day.
* Describe the layers with an image, plus add a slide for the business flows, as per the previous tutorial
* Get everyone to test for a few minutes with a high level charter.
* Allow time for questions and reflection.

## Runbooks as Test Strategy (20-30 mins)

* Slides to introduce what a run book is.
* Tell the story of the coop, where we tested VPN, Jenkins instance network connectivity.
* Give a section to each table, ask them to generate test ideas by section for the app described.

## Simple Logging Exercise (60 mins)

* Slides to describe what logging is and why better logging increases operability.
* Talk about verbosity and controlling it for testing, increasing feedback.
* Lets add morgan to the front end app, just access type logs, coding along style. Go through the different levels of detail of logs.
* Get them to test again, similar charter.
* Provide observability for testers, ability to debug.
* If there is time, add a log rotation policy. Ask how they would test it.

## Advanced Logging Exercise (60 mins)

* Slides to introduce ELK as a concept
* Why log aggregation
  * Better operability through observability, able to diagnose quickly.
  * Better testing through observability, best for investigating problems.
* Build the container.
* Add the web app logs
* Add the mongo db logs from /var/logs/mongodb
* Get them to test again and reflect on the patterns.

## Simple Monitoring and Alerting (60 mins)

* Discuss the difference between monitoring and observability
* Discuss why its important to have alerts for operability - as in looking for the known, thinking about the obvious.
* Think of it like a listener for your testing, can alert you to side effects.
* Install prometheus
* Configure to listen to API and Web
* Install AlertManager
* Add some simple alerts such as for status codes over time.
* Discuss which alerts you might add to your own application.

## Simple Health Checks and Control Mechanisms (60 mins)

* Add a health check URL for our mongo instance.
* Something simple on collection sizes.
* Maybe number of connections too if we can do it.
* Get them to test again.
* Discuss what they might add.
* If we get time, do a clear collection endpoint with a POST

## Conclusion (30 mins)

* Slide for each exercise
* Key threads
* Thank you and goodnight