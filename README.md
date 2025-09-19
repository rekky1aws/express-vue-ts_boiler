# TS + Express + Vue
This repo is a boiler for NodeJS projects using Express for the backend and VueJS for the frontend, with TypeScript Support for both sides.

It uses an architecture where the backend is a separated entity with an API providing all the data to the frontend.

## First installation steps
Server side :
```bash
cd server
npm install
cd ..
```

Client side :
```bash
cd client
npm install
cd ..
```

## Developpement
Open two terminals and in both `client/` & `server/` directories run :
```bash
npm run dev
```

In `client/` there is the most basic example on how to fetch data from the backend with a button.