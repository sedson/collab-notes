# collab-notes

A plain text notetaking app that allows realtime collaboration


## User story

Users can:
- Create an account
- Sign in and sign out
- Create plain text documents
- Add collaborators to documents
- Edit plain text documents collaboratively

## Wireframes

![wireframe 1](/wireframes/wf1.png)

![wireframe 2](/wireframes/wf2.png)

## Models

### Document
```
title: string (or collaboration safe type)
text: string (or collaboration safe type)
authorizedEditors: [user_id]
createdAt: timestamp
editedAt: timestamp
```

### User
```
name: string
password: hashed string
ownedDocs: [document_id]
collabDocs: [document_id
```

## Things to look into

- [Slate – rich text editor](https://gutenberg-yjs.vercel.app/)
- [Yjs – collaborative data JS tool](https://yjs.dev/#intro)
- [Prosemirror – has a collab demo running with source code](https://prosemirror.net/examples/collab/#edit-Example)
- [Conclave text writeup](https://conclave-team.github.io/conclave-site/)
