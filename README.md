CAUTION
===
Do not use this in production.
This repository is temporary, only used for usability study.

`goimports`
===
This repository is a copy of `cloud.google.com/go/pubsub/apiv1` and `github.com/googleapis/gax-go`
to insulate the usability test from development churn.

This might confuse `goimports` tool since `pubsub/apiv1` exists in more than one place.

Pub/Sub API Overview
===
Pub/Sub is a Google Cloud Platform real-time messaging service
that allows you to send and receive messages between independent applications.
A publisher application creates and sends messages to a topic.
Subscriber applications create a subscription to a topic to receive messages from it.
Communication can be one-to-many (fan-out), many-to-one (fan-in), and many-to-many.

Prerequisites
===
Authentication
---
To authenticate your API calls,
first install and set up [Google Cloud SDK](https://cloud.google.com/sdk/).
After that is installed, run the following command in your terminal:
```
$ gcloud beta auth application-default login
```

At this point, you are now authenticated to make calls to Pub/Sub and other Google Cloud services.

TODO: Which one should they use...?

Installation
---
Please ensure you have [Go](https://golang.org/doc/install) and
[Git](https://git-scm.com/) installed on your machine.
Once you do, please run the following command to install the package
and all its dependencies locally:
```
$ go get github.com/pongad/go-pubsub-usability/pubsub/apiv1
```

Documentation
===
Documentation is available on
 [GoDoc](https://godoc.org/github.com/pongad/go-pubsub-usability/pubsub/apiv1).
It includes simple examples for every API method.

```go
package main

import (
  "fmt"
  "log"

  pubsub "github.com/pongad/go-pubsub-usability/pubsub/apiv1"
  "golang.org/x/net/context"
  pb "google.golang.org/genproto/googleapis/pubsub/v1"
)

func main() {
  ctx := context.Background()
  c, err := pubsub.NewPublisherClient(ctx)
  if err != nil {
    log.Fatal(err)
  }
  defer c.Close()

  t, err := c.CreateTopic(ctx, &pb.Topic{
    Name: pubsub.PublisherTopicPath("{MY-PROJECT}", "{MY-TOPIC}"),
  })
  fmt.Println(t, err)
}
```
