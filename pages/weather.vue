<template>
    <div>
      <input type="text" v-model="city" placeholder="Enter a city">
      <button @click="searchWeather">Search</button>
      <div v-if="weatherData">
        <h2>{{ weatherData.name }}</h2>
        <p>Temperature: {{ weatherData.main.temp }}°C</p>
        <p>Weather: {{ weatherData.weather[0].description }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        city: '',
        weatherData: null
      };
    },
    methods: {
      async searchWeather() {
        if (this.city.trim() !== '') {
          const apiKey = '48f1792ed1b8cfa3672b4a11f752ab2e';
          const url = `https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=${apiKey}&units=metric`;
  
          try {
            const response = await fetch(url);
            if (response.ok) {
              this.weatherData = await response.json();
            } else {
              console.error('Failed to fetch weather data:', response.statusText);
            }
          } catch (error) {
            console.error('Error fetching weather data:', error);
          }
        }
      }
    }
  };
  </script>
  