<img src="https://github.com/njd1228/Tello/blob/master/readme-logo.png" width="240" />
<h3>A simple and delightful way to track and manage TV shows.</h3>

![Product screenshots](https://github.com/njd1228/Tello/blob/master/readme-screenshots.jpg)

**It's live! Check it out: https://tello.tv**

----

### Motivation and Purpose
I created Tello because I was sick of looking for ways to watch and talk about my favorite TV shows. I wanted a tool that would show me which of my favorite shows had new episodes tell you what your friends are watching, or offer social integrations so you can discuss what you're watching.



### Technical Info and Cool React Patterns

Tello uses React/Redux on the front-end, and Node/Express on the back-end, persisting data in MongoDB.

It's a single-page app, and the back-end is really just a thin layer around the database, with authentication. 90% of the logic lives on the client.

I experimented quite a bit with different React patterns in this project, and some of them are pretty neat! Some of the highlights:

##### Dynamic and Responsive Routing
Because of React Router 4's dynamic routes, you can do neat things, like make responsive routes. This means that routes update when the window size changes. See:
  - A [MediaQuery](https://github.com/njd1228/Tello/blob/master/src/components/MediaQuery/MediaQuery.js) helper, using function-as-children, and
  - The [AppRoutes](https://github.com/njd1228/Tello/blob/master/src/components/AppRoutes/AppRoutes.js) that use the prop to render routes accordingly.

Also, dynamic routes allow for this neat abstraction to create an [AuthenticatedRoute](https://github.com/njd1228/Tello/blob/master/src/components/AuthenticatedRoute/AuthenticatedRoute.js) component

##### Particle Animations
The [logged-out homepage](https://tello.tv) has floating, self-drawing particles. This is a combination of:
  - [Particle](https://github.com/njd1228/Tello-Final-Project/blob/master/src/components/Particle/Particle.js) (for the SVG drawing), and
  - [Drift](https://github.com/njd1228/Tello/blob/master/src/components/Drift/Drift.js) (for the floating).

##### Behavior Components
I've been a fan of abstracting behavior into components. Here are a couple examples:
  - Dead-simple [Hover](https://github.com/njd1228/Tello/blob/master/src/components/Hover/Hover.js) component using children-as-function
  - [HideOn](https://github.com/njd1228/Tello/blob/master/src/components/HideOn/HideOn.js) selectively renders based on a device type.

##### Scrolling
React components can manage all kinds of window-level stuff, like scrolling:
  - [ScrollDisabler](https://github.com/njd1228/Tello/blob/master/src/components/ScrollDisabler/ScrollDisabler.js) is a behavioral component which removes the ability to scroll. Useful for when modals are open, to prevent background scrolling.
  - [Scrollbars](https://github.com/njd1228/Tello/blob/master/src/components/Scrollbars/Scrollbars.js) styles the main body scrollbars. This is how Tello has the neon pink scrollbars on Webkit browsers!


#### Interested in hearing more about any of these patterns? I'd love to discuss / write a blog post about them, just [let me know](https://twitter.com/njd1228) :)



----

### Thanks!

If you use Tello, please don't be shy; **[let me know what you think](https://twitter.com/njd1228)**!
