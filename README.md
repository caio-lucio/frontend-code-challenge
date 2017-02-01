Front End Engineer Code/Design Challenge
=======================

Hello!

We've come up with this relatively open-ended programming/design
challenge that will allow you to demonstrate your skills from the comfort
of your own workspace.  In addition, we know your time is valuable, so please
feel free to use your completed work as a portfolio piece.

We wish you the best of luck and can't wait to see what you create!

## Overview

We have provided you with a simple [NodeJS](https://nodejs.org)
application server for user registration and administration.
This app does two things:
* Hosts static content from the 'public' directory
* Serves a JSON REST API for [CRUD](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete) operations on users stored in memory

We would like for you to build a user interface for user registration and one for administration of existing users.  To get you started, we have created placeholder pages (signup.html and admin.html) that you can build on.

You may use **any front-end technologies** you would like to create these user interfaces. This nodejs application is currently geared towards client-side rendering for systems like AngularJS, BackboneJS, EmberJS, VueJS, jQuery, etc.

In terms of design & layout, we leave that **entirely up to you**.  We are familiar with [Bootstrap](http://getbootstrap.com) but have also heard great things about [Foundation](http://foundation.zurb.com).  We recommend using whatever you're most comfortable with.


## Getting Started

To use this application, you will need to download and install [NodeJS](http://nodejs.org/download/).

Once you have NodeJS installed, you have two choices for downloading this source code:

1. Download & extract a [zip file](https://github.com/RakutenBrasil/frontend-code-challenge/archive/master.zip) of the source  
2. Fork this repository and git clone your fork

Next, you need to install the package dependencies by running the following command in the top-level directory of this source tree:
```
npm install
```

Once the dependancies are installed, you can start the application server by running
```
npm start
```

Once the server is running, you can access the start page (index.html) by opening your browser to [http://localhost:3000](http://localhost:3000).

To stop the server, press CTRL-C.

## REST API

The Users JSON REST API is exposed at [http://localhost:3000/users](http://localhost:3000).

On server start, user data is read into memory from init_data.json. All subsequent actions are done against this memory store.  Stopping and starting the server will re-initialize data from init_data.json.  

#### API Endpoints

* **/users**
HTTP GET: returns array of all users
HTTP POST: creates a new user, returns the created user data
* **/users/:id**
HTTP GET: returns the user with given id (numeric, auto-incrementing).  HTTP 404 if user not found
HTTP PUT: updates the user with given id and returns updated record. HTTP 404 if user not fund.
HTTP DELETE: removes the users with given id, returns nothing (HTTP 204)

Here is an example of results returned from HTTP GET on /users:
```
[{"id":1,"email":"kyle@server.com","firstName":"Kyle","lastName":"White","state":"active"},
{"id":2,"email":"jane@server.com","firstName":"Jane","lastName":"Stone","state":"active"},
{"id":3,"email":"lilly@server.com","firstName":"Lilly","lastName":"Smith","state":"pending"},
{"id":4,"email":"fred@server.com","firstName":"Fred","lastName":"Miles","state":"pending"},
{"id":5,"email":"alex@server.com","firstName":"Alexandra","lastName":"Betts","state":"pending"}]
```

## Requirements

**We kindly ask that you spend no more than 6-8 hours on this challenge.**

At a minimum, there are three things we would like to see:
* Users should be able to register
* Admin page should list all users
* Design/layout of content

We will of course **examine your code for readability, architectural decisions, and modularity**.  If/when you meet with us, be prepared to talk about why and how you built your interfaces.

## Idea inspiration

If you have additional time after completing the requirements (we _think_ you should), then we'd love to see what else you can do.  Here are some ideas to get you started (but please don't limit yourself to these!).

* Signup form validation
* Automated testing
* Dynamic data on Admin page (no need to refresh to status changes)
* Sorting/Searching of users
* Admin button to activate accounts (set user status to 'active')
* Admin creation of new accounts
* Optimize assets (minimize and/or bundle css/js)

To be perfectly clear, we don't expect that anyone could complete _all_ of these in 6-8 hours.  This is simply a list of ideas to inspire you.

## Submission

You can follow the GitHub Fork/Pull Request workflow by [forking this repository](https://github.com/RakutenBrasil/frontend-code-challenge/fork), commiting your changes, and submiting a pull request to us, explaning all the features and modification that you made.  For more information about that, you can see this [GitHub article](https://help.github.com/articles/fork-a-repo/#propose-changes-to-someone-elses-project)

## License

We have licensed this project under the MIT license so that you may use this for a portfolio piece (or anything else!).

## Credits

This project/idea is based on [https://github.com/yodlr/frontend-code-challenge](https://github.com/yodlr/frontend-code-challenge).