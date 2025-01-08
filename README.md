# Weather App 🌦️

A simple weather application that allows users to fetch and display real-time weather information for any city using the OpenWeather API.

---

## 🚀 Features

- **Search by City**: Enter a city name to retrieve weather details.  
- **Real-Time Data**: Fetches current temperature, humidity, wind speed, and weather conditions.  
- **Dynamic Icons**: Displays weather-specific icons (e.g., rain, clouds, clear sky).  
- **Error Handling**: Notifies users for invalid city names or network errors.  
- **Responsive Design**: Optimized for both desktop and mobile devices.  

---

## 🛠️ Technologies Used

- **HTML5**: For structuring the app layout.  
- **CSS3**: For styling and responsive design.  
- **JavaScript**: For dynamic functionality and API integration.  
- **OpenWeather API**: For real-time weather data.  

---

## 🖼️ Preview

![image](https://github.com/user-attachments/assets/13273634-e0c1-426d-8361-499130395ab3)


---

## ⚙️ Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Prathmesh-1570/weather-app.git
   cd weather-app
   ```

2. **Set Up API Key**:
   - Sign up at [OpenWeather](https://openweathermap.org/) to get your API key.
   - Replace the placeholder in the `script.js` file:
     ```javascript
     const apikey = "YOUR_API_KEY_HERE";
     ```

3. **Run the Application**:
   - Open `index.html` in your browser to use the app.

---

## 📂 File Structure

```
weather-app/
├── index.html       # Main HTML file
├── style.css        # Styling for the app
├── script.js        # JavaScript for functionality
├── images/          # Weather icons and assets
│   ├── clouds.png
│   ├── rain.png
│   ├── clear.png
│   ├── ...
└── README.md        # Project documentation
```

---

## 📖 Usage

1. Enter a city name in the input field.  
2. Click the **Search** button.  
3. View the weather details, including:
   - Temperature  
   - Humidity  
   - Wind speed  
   - Weather condition  
4. If the city name is invalid or there's an error, an appropriate message will be displayed.

---

## 🧩 Functionality

### Key Functions in `script.js`:

1. **Fetching Weather Data**:
   - Connects to the OpenWeather API to retrieve weather information.
     ```javascript
     async function checkWeather(city) {
         const response = await fetch(apiUrl + city + `&appid=${apikey}`);
         // Parse response and update UI
     }
     ```

2. **Dynamic Icon Updates**:
   - Displays appropriate weather icons based on conditions:
     ```javascript
     if (data.weather[0].main == "Clouds") {
         weatherIcon.src = "images/clouds.png";
     }
     ```

3. **Error Handling**:
   - Handles invalid city names or network errors:
     ```javascript
     if (response.status == 404) {
         document.querySelector(".error").style.display = "block";
     }
     ```

4. **Responsive Design**:
   - Ensures the app works well on both desktops and mobile devices.

---

## 🌐 Demo

https://weather-prathmesh.netlify.app

---

## 📜 License

This project is licensed under the MIT License. Feel free to use, modify, and share!

---

## 🤝 Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue to suggest improvements.

---

## 💡 Future Enhancements

- Add a 5-day weather forecast.  
- Implement geolocation to fetch weather for the user's current location.  
- Add support for multiple units (e.g., Celsius, Fahrenheit).  

--- 

Let me know if you'd like further refinements! 🚀
