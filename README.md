CAUTION
----
Do not use this in production.
This repository is temporary, only used for usability study.

`goimports`
---
This repository is a copy of `cloud.google.com/go/pubsub/apiv1` and `github.com/googleapis/gax-go`
to insulate the usability test from development churn.

This might confuse `goimports` tool since `pubsub/apiv1` exists in more than one place.

Pub/Sub API Overview
---
Pub/Sub is a Google Cloud Platform real-time messaging service
that allows you to send and receive messages between independent applications.
A publisher application creates and sends messages to a topic.
Subscriber applications create a subscription to a topic to receive messages from it.
Communication can be one-to-many (fan-out), many-to-one (fan-in), and many-to-many.

Prerequisites
---
To authenticate your API calls,
- install and set up [Google Cloud SDK](https://cloud.google.com/sdk/)
- `$ gcloud auth login` or `$ gcloud beta auth application-default login`

TODO: Which one should they use...?

- Install [Go](https://golang.org/doc/install) and Git
  - Git is used by the Go toolchain to fetch dependencies
- `$ go get github.com/pongad/go-pubsub-usability/pubsub/apiv1`

Documentation
---
Documentation is available on [GoDoc](https://godoc.org/github.com/pongad/go-pubsub-usability/pubsub/apiv1).
