dalek-reporter-mongodb
===================

> DalekJS reporter plugin for MongoDB

## Ressources

## Docs

The reporter can be installed with the following command:
```
$ npm install dalek-reporter-mongodb --save-dev
```
The result that will be saved.

```javascript
{
    "_id" : ObjectId("568bf62889f8e4790fcb8613"),
    "tests" : [
        {
            "id" : "test2",
            "name" : "test",
            "browser" : "PhantomJS",
            "status" : true,
            "passedAssertions" : 1,
            "failedAssertions" : 0,
            "actions" : [
                {
                    "value" : "http://google.com",
                    "type" : "open",
                    "uuid" : "uuid-3",
                    "kind" : "action"
                },
                {
                    "success" : true,
                    "expected" : "Google",
                    "value" : "Google",
                    "message" : "It has title",
                    "type" : "title",
                    "kind" : "assertion"
                }
            ]
        }
    ],
    "elapsedTime" : {
        "hours" : null,
        "minutes" : null,
        "seconds" : 1.1741814639999999
    },
    "status" : true,
    "assertions" : 1,
    "assertionsFailed" : 0,
    "assertionsPassed" : 1
}
```
You can change this by adding a config option to the your Dalekfile

```javascript
{
  "reporter": ["mongodb"],
  "mongodb-reporter": {
    "authenticate": true,
    "host":"localhost",
    "user":"",
    "pass":"",
    "db":"report",
    "colletion":"tests",
    "port":27017
  }
}
```
## Legal FooBar (MIT License)

Copyright (c) 2016 Cristiano Boell

Distributed under [MIT license](https://github.com/dalekjs/dalek/blob/master/LICENSE-MIT)
