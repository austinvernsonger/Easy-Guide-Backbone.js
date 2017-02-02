# Application

---

The Backbone.js gives a structure to the web applications that allows to separate business logic and user interface logic. In this chapter, we are going to discuss the architectural style of Backbone.js application, for implementing user interfaces. The following daigram shows architecture of Backbone.js:

**The architecture of Backbone.js contains following modules:  
**

* HTTP Request

* Router

* View

* Events

* Model

* Collection

* Data Source

## HTTP Request

The HTTP client sends a HTTP request to a server in the form of request message where web browsers, search engines etc acts like HTTP clients. User requests for a file such as documents, images etc using HTTP request protocol. In the above daigram, you could see that the HTTP client uses the router to send the client request.

## Router

It is used for routing client side applications and connects them to actions and events using URL's. It is an URL representation of application's objects. The URL is changed manually by the user. The URL is used by the backbone so that it can understand what application state to be sent or present to the user. Router is a mechanism which can copy the URL's to reach the view. Router is required when web applications provide linkable, bookmarkable, and shareable URL's for important locations in the app.

In the above daigram, the router sending HTTP request to the view. It is an useful feature when an application needs routing capability.

## View

Backbone.js views are responsible for how and what to display from our application and they don't contain HTML markup for the application. It specifies an idea behind the presentation of the model's data to the user. Views are used to reflect "how your data model looks like". The view classes do not know anything about the HTML and CSS and each view can be updated independently when the model changes without reloading the whole page. It represents the logical chunk of UI in the DOM.

As shown in the above architecture, views represents the user interface which is responsible for displaying the response for user request done by using the router.

## Events

Events are main parts of an application. It binds user's custom events to an application. They can be mixed into any object and are capable of binding and triggerring custom events. You can bind the custom events by using desired name of your choice. Typically, events are handled synchronously with their program flow. In the above architecture, you could see when an event occurs, it represents the model's data by using the view.

## Model

It is the heart of the JavaScript application that retrieves and populates the data. Models contain data of an application and logic of the data and represents basic data object in the framework. Models represents business entities with some business logic and business validations. It's mainly used for data storage and business logic. It can be retrieved from and saved to data storage. Model takes the HTTP request from the events passed by the view using the router and synchronizes the data from database and send the response back to the client.

## Collection

Collection is a set of models which binds events, when the model has been modified in the collection. Collection contains list of models that can be processed in the loop and supports sorting and filtering. When creating a collection, we can define what type of model that collection is going to have along with the instance of properties. Any event triggered on a model, which will also trigger on the collection in the model.

It also takes the request from the view, bind events and synchronizes the data with requested data and send response back to the HTTP client.

## Data Source

It is the connection set up to a database from a server and contains the information which is requested from the client. The flow of the Backbone.js architecture can be described as shown in the below steps:

* User requests for the data using router, which routes the applications to the events using URL's.

* The view represents model's data to the user.

* The model and collection retrieves and populates the data from the database by binding custom events.



