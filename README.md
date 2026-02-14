# Dashboard de Precios de Criptomonedas en Tiempo Real

Este proyecto es un **dashboard interactivo** que visualiza en tiempo real la fluctuación de los precios de criptomonedas usando datos de Binance a través de WebSockets. Está desarrollado con **HTML, CSS, JavaScript y D3.js**, y tiene como objetivo ofrecer una narrativa clara y accesible para público general sobre cómo varían los precios minuto a minuto.

**Ver tablero publicado en Replit:**  
https://criptomonedas-precios--mafegz0.replit.app

---

## ¿Qué hace este dashboard?

El tablero permite:

- Conectarse a una fuente de datos en tiempo real (Binance WebSocket).
- Visualizar la **gráfica de tendencia** de una criptomoneda seleccionada.
- Mostrar el **precio actual**, el **rango mínimo y máximo** desde la apertura del tablero y la **variación acumulada**.
- Actualizar dinámicamente los datos sin necesidad de recargar la página.
- Permitir al usuario seleccionar diferentes criptomonedas mediante un menú desplegable.

---

## Tecnologías usadas

- **HTML & CSS** — Estructura y estilo del dashboard.
- **JavaScript** — Lógica de conexión, modelado de datos y dinámicas UI.
- **D3.js** — Visualización de datos.
- **Binance WebSocket API** — Fuente de datos en tiempo real.

---

## Estructura del proyecto

├── index.html # Interfaz principal del dashboard
├── style.css # Estilos visuales
├── script.js # Lógica y visualización
├── README.md # Documentación del proyecto

## Cómo funciona

1. La aplicación se conecta a la API de Binance usando WebSockets para recibir precios en tiempo real de varias criptomonedas.
2. Los datos entrantes se modelan en una estructura que acumula información de cada moneda.
3. Se utiliza D3.js para dibujar una **gráfica de línea** que muestra la evolución del precio de la moneda seleccionada.
4. Textos descriptivos y de contexto acompañan la visualización para facilitar la lectura por parte de un público general.

---

## Notas

Este proyecto fue desarrollado como parte de un ejercicio académico para practicar conectividad en tiempo real y visualización de datos sin conocer valores futuros, enfatizando la narrativa visual hacia un público sin experiencia técnica previa.

---

## Enlaces

-  **Tablero publicado (Replit):** https://criptomonedas-precios--mafegz0.replit.app
-  **Repositorio (GitHub):** https://github.com/Mafegz0/Dashboard-criptomonedas/tree/main


