# NTU Vote Production Repository

## To clone this repository along with submodules
```
git clone https://github.com/ntu-vote/ntu-vote-production
git submodule init
git submodule update
```
## Prerequisites
+ nodejs ^16.13.0
+ npm ^8.0.0
+ postgresql ^14

## Frontend
1. Go into frontend directory
2. Configure `frontend/.env` to edit the *PORT* and *REACT_APP_PUBLIC_URL* parameters according to your environment (set the latter to localhost if you are running locally)
3. Install node_modules with `npm install`
4. Start frontend server with `npm start`

## Backend
1. Go into backend directory
1. Copy file `backend/ormconfig.json.js-example` to `backend/ormconfig.json` and configure it to connect to an existing clean database which the user has access to.
2. Schema `ntu_vote` should exist in the database specified in `backend/ormconfig.json`
```
\c *db-name*
CREATE SCHEMA IF NOT EXISTS ntu_vote
```
3. Run ORM migrations with `npm run typeorm-run`
4. Transpile typescript to javascript with `npm run build`
5. Start backend server with `npm run start`
