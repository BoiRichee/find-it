# Find-It 🎯

> An exciting real-time multiplayer game inspired by the classic Spot It! (Dobble) card game

## 🎮 Game Description

Find-It is an online multiplayer adaptation of the popular Spot It! card game. Players compete in real-time to quickly find matching symbols between cards, testing their observation skills and reflexes. The game provides an engaging multiplayer experience where speed and accuracy are key to victory.

### ✨ Features

- Real-time multiplayer gameplay
- Multiple game rooms support
- Player ranking system

## 🖼️ Screenshots

### Game 
![Uploading Screen Shot 2025-02-06 at 11.28.13.png…]()

### Gameplay
![Uploading Screen Shot 2025-02-06 at 11.28.37.png…]()

## 🛠️ Tech Stack

### Frontend
- React.js
- Vite
- Socket.IO Client
- Tailwind CSS

### Backend
- Node.js
- Express
- Socket.IO
- PostgreSQL
- Sequelize ORM

## 🚀 Installation and Setup

### Backend Setup

1. **Clone the repository**
```bash
git clone https://github.com/find-it/server.git
cd server
```

2. **Install dependencies**
```bash
npm install
```

3. **Setup PostgreSQL Database**
```bash
npx sequelize-cli db:create
npx sequelize-cli db:migrate
```

4. **Start the server**
```bash
npm run dev
```
The backend will be available at http://localhost:3000

### Frontend Setup

1. **Clone the repository**
```bash
git clone https://github.com/find-it/client.git
cd client/client
```

2. **Install dependencies**
```bash
npm install
```

3. **Start the development server**
```bash
npm run dev
```
The frontend will be available at http://localhost:5173

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

