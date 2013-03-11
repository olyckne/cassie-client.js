cassie-client.js
================

A lovely little JavaScript client for the lovely little chatbot Cassie.

### Install
- Run the [Cassie server](https://github.com/olyckne/cassie)
- Right now it depends on [socket.io](http://socket.io) Cassie server hosts that for you at http://path.to.cassie.server/socket.io/socket.io.js
- Include `cassie-client.js`
- in your main.js (or whatever): 

```javascript
cassie_client = new Cassie_client(options);
cassie_client.init();
```

### Options

| option            | type          | description     | default
| ----------------- | ------------- | --------------- | ------------ |
| url               | string        | url to server   | "ws://localhost:8080"
| outputElem        | jQuery object | html element    | $(".output")
| wrapperElem       | string        | html element    | "\<pre/>"
| form              | string        | id of the form  | "#cassie_form"
| formInput         | string        | id of form input| "#cassie_form_input"
| newMessageClass   | string        | classname       | "cassie_new_message"
| socket            | socket object | Already created socket object            | null (creates a new io.socket)
| scrollIfAtBottom  | boolean       | pins to bottom when new messages arrive  | true
| showTimestamp     | boolean       | show timestamp with message              | true
