
# PROXESS
##### A process manager for your service pool. The idea is, it should be easy to manage all of the servers running on your local machine. Proxess aims to improve the developer experience by allowing you to store all of your terminal commands in a database and start / stop & monitor proccesses

## Prerequisites
* [Node.js](http://nodejs.org/) (with NPM)

## Installation

* `(sudo) npm install -g proxess`

## Running / Development

*  to manage your running services
 * Start the service manager (in your terminal type..): `proxess`
* Visit your manager at [http://localhost:9011/](http://localhost:9011/).

## THE API
```
GET /process          "Returns A List Of All Processes In The Database"
POST /process         "Creates A New Processes In The Database"
    
GET /process/:id      "Returns A Process Model by it's id"
PUT /process/:id      "Updates A Process Model by it's id"
DELETE /process/:id   "Removes A Process Model by it's id"

GET /stats            "Returns Memory Pressure and CPU Usage For Each Process"
GET /stats/:id        "Returns Memory Pressure and CPU Usage For A Single Process"

GET /alive            "Returns An array of currently running processes managed by this application"

POST /execute/:id     "Starts A Process By It's ID"
DELETE /execute/:id   "Kills A Process By It's ID"

POST /all             "Starts Every Dead Process In Your Process Database"
DELETE /all           "Stops Every Running Process In Your Process Database"
```

## Additions to the API Coming Soon!
```
    // Grouping Processes (To start and stop the group you will still use the /execute/:id route.. We will manage the rest internally.)

    POST /group        "Defines a process group to run together (a named set of processes)"
    GET /group         "Returns A List Of All Process Groups In The Database"
    
    GET /group/:id     "Returns A Process Group By It's ID"
    PUT /group/:id     "Updates A Process Group By It's ID"
    DELETE /group/:id  "Deletes A Process Group By It's ID"
```

# Coming Soon, An Ember Application To Manage The Processes in a GUI! YAY! (currently using curl or porstman :( 

## GITHUB
* [proxess](http://github.com/charliemitchell/proxess) 