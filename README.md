# find-it
Online Multiplayer Spot-It Game


# Find It server

### Installation

1. **Clone the repository**

   ```sh
   git clone https://github.com/find-it/server.git

   ```

2. **Install dependencies**

   ```sh
   # For the Backend:

   cd server
   npm install
   ```

3. **Setup Database Postgres**

   ```sh
   npx sequelize-cli db:create
   npx sequelize-cli db:migrate
   ```

## Access the application

- Backend: http://localhost:3000

  ```sh
  npm run dev
  ```


# Find It client

### Installation

1. **Clone the repository**

   ```sh
   git clone https://github.com/find-it/client.git

   ```

2. **Install dependencies**

   ```sh
   # For the Frontend:

   cd client/client
   npm install
   ```

## Access the application

- Frontend: http://localhost:5173

  ```sh
  npm run dev
  ```
