# Signup-Authentication

# Project Setup
Start by creating a new React app using Vite, which provides a faster development environment:

npx create-vite mern-signup-app --template react
cd mern-signup-app
Now, install the required dependencies:

npm install react-bootstrap react-router-dom axios
Implementing Components
App Component
Integrate React Router to create navigation between different components. Update your App.jsx:

// src/App.jsx
import React from 'react';
import 'bootstrap/dist/css/bootstrap.min.css';
import Signup from './Signup';
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import Login from './Login';
import Home from './Home';

function App() {
    return (
        <BrowserRouter>
            <Routes>
                <Route path="/register" element={<Signup />} />
                <Route path="/login" element={<Login />} />
                <Route path="/home" element={<Home />} />
            </Routes>
        </BrowserRouter>
    );
}

export default App;
