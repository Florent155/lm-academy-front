<template>
    <div class="contact-container">
      <h2 class="section-title">Contact</h2>
      <div class="info-grid">
        <!-- Address Section -->
        <div class="info-box">
          <h3>Address</h3>
          <iframe
            class="map"
         src="https://www.google.com/maps?q=Shkolla%20e%20Mesme%20Teknike%20Sh.M.T.%20Lufti%20Musiqi&output=embed"
            width="100%"
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
          <p class="city">Vushtrri<br />42000</p>
        </div>
  
        <!-- Opening Hours -->
        <div class="info-box">
          <h3>Opening Hours</h3>
          <div class="hours-row" v-for="(hour, i) in hours" :key="i">
            <span>{{ hour.day }}</span>
            <span>{{ hour.time }}</span>
          </div>
        </div>
  
        <!-- Contact -->
        <div class="info-box">
          <h3>Contact</h3>
          <p>Tel: +38328009</p>
          <p>e-mail: shmt.lutfi.musiqi@gmail.com</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const hours = [
    { day: 'Monday', time: '07:00 - 18:30' },
    { day: 'Tuesday', time: '07:00 - 18:30' },
    { day: 'Wednesday', time: '07:00 - 18:30' },
    { day: 'Thursday', time: '07:00 - 18:30' },
    { day: 'Friday', time: '07:00 - 18:30' },
  ];
  </script>
  
  <style scoped>
  .contact-container {
    background: linear-gradient(to bottom, #dee3eb, #cfd8e3);
    padding: 3rem;
    font-family: Arial, sans-serif;
    color: #111;
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
  }
  
  .section-title {
    font-size: 2.5rem;
    font-weight: bold;
    margin-bottom: 2.5rem;
  }
  
  .info-grid {
    display: flex;
    justify-content: space-between;
    gap: 2rem;
    width: 100%;
    max-width: 1400px;
    flex-wrap: wrap;
  }
  
  .info-box {
    flex: 1 1 350px;
    display: flex;
    flex-direction: column;
    font-size: 1.2rem;
  }
  
  .info-box h3 {
    margin-bottom: 1.2rem;
    font-size: 1.4rem;
    color: #333;
  }
  
  .map {
    width: 100%;
    height: 400px;
    border: 0;
    border-radius: 8px;
    margin-bottom: 0.8rem;
  }
  
  .city {
    margin-top: 0.8rem;
    font-weight: bold;
  }
  
  .hours-row {
    display: flex;
    justify-content: space-between;
    margin-bottom: 0.5rem;
  }
  
  @media (max-width: 768px) {
    .info-grid {
      flex-direction: column;
      align-items: center;
    }
  
    .info-box {
      width: 100%;
      text-align: center;
    }
  }
  </style>
  