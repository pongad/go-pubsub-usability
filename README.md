CAUTION
----
Do not use this in production.
This repository is temporary, only used for usability study.

Pub/Sub API Overview
---
Pub/Sub is a Google Cloud Platform real-time messaging service
that allows you to send and receive messages between independent applications.
A publisher application creates and sends messages to a topic.
Subscriber applications create a subscription to a topic to receive messages from it.
Communication can be one-to-many (fan-out), many-to-one (fan-in), and many-to-many.

Background Scenario
---
Imagine that you are in the process of developing a new web application
that could benefit from asynchronous messaging.
For the sake of this scenario, let’s say your application will take user sign-ups,
and you need a way to notify downstream services when such an event occurs.
Before committing to using Google Cloud Pub/Sub,
you want to explore the API to better understand the developer experience.
In particular, what is it like working with the API, the documentation, and the client library.

To assess the developer experience, you decide to build a Hello World style application
designed to test out some of the core Pub/Sub functionality.

Your application will be run locally on your machine, via the command line.
E.g. `$ go run app.go`

Account Details
---
In order to complete these tasks, you will require Google account credentials.
The following account has been set up for your use during this study.

TODO: Add account details.

Prerequisites
---
Before consuming any Google API, there are two important prerequisite steps:
- Creating a Developers Console project.
- Enabling the API on your project.

We have already completed the above two steps for you.
The project we have created has the Project ID:

TODO: Add project ID

To authenticate your API calls,
- install and set up [Google Cloud SDK](https://cloud.google.com/sdk/)
- `$ gcloud auth login`

- Install [Go](https://golang.org/doc/install) and Git
  - Git is used by the Go toolchain to fetch dependencies
- `$ go get github.com/pongad/go-pubsub-usability`
