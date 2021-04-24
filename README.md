# collab-notes

A plain text notetaking app that allows realtime collaboration

[Deployed Front End](http://collab-notes-front-end-herokuapp.com)

[Backend API Repo](https://github.com/sedson/collab-notes-backend)

[Front End Repo](https://github.com/mayer171/collab-notes-frontend)

# Technologies used

The front end application is a React app that uses Material for styles. The backend is a NodeJS app that uses Express for handling http requests and the npm package 'ws' for managing web socket requests. The data handleing is Mongo + Mongoose. Both the front end and backend are deployed on Heroku. 

**NOTE** – for the app to work properly make sure you are conencting via `http` not `https`! Also the credentials are not properly sending from current versions of Chrome! Works best in Firefox.

The text editing component uses Slate.js – a React-based tool for building custom text editors in front end apps. Slate has a lovely datatype that stores each change made to a document as an Operation. These operations are serielazed to JSON and then sent via a live WebSokcet connection to the Express + WS backend. The server then updates the internal representation of the document and broadcasts the operations to all the other editors that have connected 

## User story

Users can:
- Create an account
- Sign in and sign out
- Create plain text documents
- Add collaborators to documents
- Edit plain text documents simultanesouly

## Wireframes

![wireframe 1](/wireframes/wf1.png)

![wireframe 2](/wireframes/wf2.png)

## Models

### Document
```
title: string (or collaboration safe type)
content: string (or collaboration safe type)
authorizedEditors: [users]
createdAt: timestamp
editedAt: timestamp
```

### User
```
name: string
password: hashed string
```

## Things to look into

- [Slate – rich text editor](https://docs.slatejs.org/)
- [Yjs – collaborative data JS tool](https://yjs.dev/#intro)
- [Prosemirror – has a collab demo running with source code](https://prosemirror.net/examples/collab/#edit-Example)
- [Conclave text writeup](https://conclave-team.github.io/conclave-site/)
- [Convergence](https://convergencelabs.com/)
