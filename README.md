# 🚗 Vehicle CO₂ Emissions & Route Calculator

A full-stack JavaScript application that calculates the total carbon footprint of a car journey. By combining the DVLA Vehicle Enquiry API and the Google Maps API, the app provides users with real-time environmental impact data based on their specific vehicle registration and travel route.


## 🎯 Project Overview

This project was built to solve the problem of visualizing environmental impact. While many maps provide distance, this tool adds a layer of personalization by fetching official vehicle emission ratings ($g/km$) to calculate the total $CO_2$ output for a specific trip.


## ✨ Key Features

Real-time Vehicle Lookup: Uses a Node.js backend to securely query the DVLA database for vehicle specifications.Dynamic Route Mapping: Integrates Google Maps to calculate precise driving distances between two locations.Automatic Carbon Calculation: Uses the formula:$$\text{Trip Distance (km)} \times \text{Vehicle Emissions (g/km)} = \text{Total Trip } CO_2$$Technical Security: Implements a proxy server to protect API credentials and handle CORS headers.


## 🛠️ Tech Stack

* Frontend: HTML5, CSS3, JavaScript (ES6+)
* Backend: Node.js, Express.js
* APIs: Google Maps JavaScript API (Maps, Directions, & Distance Matrix)DVLA Vehicle Enquiry Service (Vehicle specs & emissions)


## 🏗️ Architecture & Security

To interact with the DVLA API, this project utilizes a Backend Proxy. This is a critical design choice that:Hides API Keys: Prevents the DVLA x-api-key from being exposed in the browser's "Network" tab.Resolves CORS: Bypasses "Cross-Origin Resource Sharing" restrictions that would otherwise block the browser from contacting the government's API directly.


## 🚀 Setup & Installation

Clone the RepoBashgit clone https://github.com/your-username/your-repo-name.git

cd your-repo-name

Install DependenciesBashnpm install

### Environment Variables

Create a .env file in the root directory and add your DVLA API key:Code snippetDVLA_API_KEY=your_key_here

### Google Maps Key

Add your Google Maps API key to the index.html script tag:HTML<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY_HERE&callback=initMap"></script>

Run the AppBashnode server.js

Open your browser to http://localhost:3000 (or your local frontend server).


## 📈 Future Improvements

Comparison Tool: Compare the trip's $CO_2$ output against public transport or an electric vehicle (EV).History Log: Save previous trips to a local database (MongoDB or PostgreSQL) to track monthly emissions.Frontend Framework: Migrate the UI to React for better state management.
