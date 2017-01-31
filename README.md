Customer Service Portal & Help Desk Chat
===============

This repo is a sample for a customer service portal single page app with a live chat.

For the customer service portal, sample pages from [Adidas's Customer Service](http://www.adidas.com/us/customerservice) rebuilded as _single page application_.

For considering reusability of the components, _Live Chat_ modules created separately from single page application. Basically, you can add the _Live Chat_ module easily any other pages or portals.

---

## How To Build

Since _SPA_ and the _Live Chat_ are separate modules, you have to build them separately.

### Live Chat
```
$ cd live-chat
$ npm install
$ npm build:prod
```

### SPA
```
$ cd .. // if you are in live-chat directory
$ npm install
$ npm build:prod
```

---

## How To Run
Use two terminal screens.

In first terminal, in the `live-chat` folder
```
$ npm run server
```

In the second terminal, in the project root
```
$ npm run start
```

Then in your browser navigate to [http://localhost:8080]() for the _SPA_, navigate to [http://localhost:8080/backoffice]() for _Live Chat_'s agent view. 

After page load, the _Live Chat_'s chat screen will appear at the right bottom of the page. 

---

## How To Use
For starting a chat with agent (assuming the agent is already navigated to [backoffice page](http://localhost:8080/backoffice)), just click to "need help?" and start typing.

When a client started a new chat, in the backoffice, a new chat tab will appear. The agent cannot *start* a new chat session.

---

## Frameworks Used
- [React](https://facebook.github.io/react/) is used for _SPA_'s UI components. 
- [Redux](http://redux.js.org/) is used for _SPA_'s state management.
- [Socket.io](http://socket.io/) is used for _Live Chat_ module's Websocket server implementation
- [Webpack](https://webpack.js.org) is used for build tasks

## Notes
For _SPA_'s page data, static Rest API is used in [app/rest-data](). In real life applications, the system can easily change to support a real Rest API server. 