# Capture audience feedback with a serverless app

You are giving this presentation and as attendees leave the room you'd like to get a quick feel about how you did. *Emoting* mimics the smiley terminals you may see at the airport security or whenever you are queuing somewhere.

<img src="xdocs/emoting-question.png" height="200"/>
<img src="xdocs/emoting-answer.png" height="200"/>
<img src="xdocs/emoting-admin.png" height="200"/>

## Overview

Built using the IBM Bluemix, the application uses:
* IBM Bluemix OpenWhisk to host the backend
* Cloudant to persist the data
* GitHub Pages to host the frontend

No runtime to deploy, no server to manage :)

![Architecture](http://g.gravizo.com/g?
  digraph G {
    node [fontname = "helvetica"]
    rankdir=LR
    user -> github
    github -> openwhisk [label="API Calls"]
    openwhisk -> cloudant
    github [shape=circle style=filled color="%234E96DB" fontcolor=white label="GitHub Pages"]
    openwhisk [shape=circle style=filled color="%2324B643" fontcolor=white label="OpenWhisk"]
    cloudant [shape=circle style=filled color="%234E96DB" fontcolor=white label="Cloudant"]
  }
)

## Application Requirements

* IBM Bluemix account. [Sign up][bluemix_signup_url] for Bluemix, or use an existing account.

## License

See [LICENSE](LICENSE) for license information.

---

This project is a sample application created for the purpose of demonstrating a serverless app with OpenWhisk. The program is provided as-is with no warranties of any kind, express or implied.

[bluemix_signup_url]: https://console.ng.bluemix.net/?cm_mmc=GitHubReadMe
