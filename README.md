# Real-Time Cryptocurrency Price Dashboard

## Live Demo  
https://mafegz0.github.io/Dashboard-criptomonedas/

[![View Project](https://img.shields.io/badge/View-Project-blue)](https://mafegz0.github.io/Dashboard-criptomonedas/)

This project is an **interactive dashboard** that visualizes real-time cryptocurrency price fluctuations using Binance data through WebSockets. It is developed with **HTML, CSS, JavaScript, and D3.js**, and aims to provide a clear and accessible narrative for a general audience on how prices change minute by minute.

**View deployed dashboard on Replit:**  
https://criptomonedas-precios--mafegz0.replit.app

---

## What does this dashboard do?

The dashboard allows users to:

- Connect to a real-time data source (Binance WebSocket)
- Visualize the **trend chart** of a selected cryptocurrency
- Display the **current price**, **minimum and maximum range** since the dashboard opened, and **cumulative variation**
- Dynamically update data without refreshing the page
- Select different cryptocurrencies using a dropdown menu

---

## Technologies Used

- **HTML & CSS** — Dashboard structure and styling  
- **JavaScript** — Data connection logic, modeling, and UI dynamics  
- **D3.js** — Data visualization  
- **Binance WebSocket API** — Real-time data source  

---

## Project Structure

```
├── index.html # Main dashboard interface
├── style.css # Visual styles
├── script.js # Logic and visualization
└── README.md # Project documentation
```

---

## How It Works

1. The application connects to the Binance API using WebSockets to receive real-time cryptocurrency prices.
2. Incoming data is modeled into a structure that accumulates information for each cryptocurrency.
3. D3.js is used to draw a **line chart** showing the price evolution of the selected cryptocurrency.
4. Descriptive and contextual text accompanies the visualization to facilitate interpretation for a general audience.

---

## Notes

This project was developed as part of an academic exercise to practice real-time connectivity and data visualization without prior knowledge of future values, emphasizing visual storytelling for a non-technical audience.

---

## Links

- **Live Dashboard (Replit):**  
https://criptomonedas-precios--mafegz0.replit.app

- **GitHub Repository:**  
https://github.com/Mafegz0/Dashboard-criptomonedas/tree/main
