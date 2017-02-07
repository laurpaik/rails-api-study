# Rails as an API Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

Please note:

-   Many of the readings will mention the "view" layer. We won't be covering the
    view layer in this program.
-   We'll use our [Rails API Template](https://github.com/ga-wdi-boston/rails-api-template)
    repository as the basis for our rails applications.
    This template excludes the "view" layer.

## Required Readings

-   Better Explained
    -   [Starting Ruby on Rails: What I Wish I Knew](http://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/)
        (sections 3 and 4)
    -   [Intermediate Rails: Understanding Models, Views and Controllers](http://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/)
        (up to and including "Quick Controllers")
-   Ruby on Rails Guides
    -   [Rails Routing from the Outside](http://guides.rubyonrails.org/routing.html)
        (up to and including chapter 2.6)
    -   [Action Controller Overview](http://guides.rubyonrails.org/action_controller_overview.html)
        (up to and including chapter 4.5)
    -   [The Rails Command Line](http://guides.rubyonrails.org/command_line.html)
        (up to and including chapter 1.4)

## Additional Resources

-   [Getting Started with Rails — Ruby on Rails Guides](http://guides.rubyonrails.org/getting_started.html)

## Define Model Responsiblities

In your own words, define what the responsibilities of the model layer are in
Rails.

```md
The model gets info from the controller and either spits out a failure if it doesn't get it, or it performs the action and sends some sort of confirmation... So if the controller tells it to GET something, it'll send the controller the data it needs... or if it needs to POST new data, the model will post it and send back the newly made data.
```

## Define Controller Responsiblities

In your own words, define what the responsibilities of the controller layer are
in Rails.

```md
The controller receives a request from the server (via the router) and forwards that request to the model... Once the model responds with success, the controller sends the client a success or fail message, and depending on what the request is, puts it in a form that's easier for the human eye to digest.
```

## Define Router Responsiblities

In your own words, define what the router does in Rails.

```md
The router talks to the controller... it's like the highway between the API and the server, so it breaks strings down and points the request to the appropriate controller action... so if the whole system is a highway and the request is the vehicle and the controller action is an exit, the router is like the road/map that shows the request the correct path to the controller... It's not a perfect example, but yea the router seems like a cool guide that helps the request get to the controller and fulfill its mission.
```

## The Request-Response Cycle in Rails

Starting with a client making a GET request to a particular URL, describe how
the parts of Rails interact to produce and send a response.

```md
So the client makes a GET request to the server, and the server sends the request through the router, which points the request to the controller. The controller then asks the model to fulfill the request, and the model either tells the controller to try again (if it's a failure), or it sends the controller the information/data it wants. If it's a success, the controller turns the data into something the user can actually see/read and sends the final View to the client.
```
