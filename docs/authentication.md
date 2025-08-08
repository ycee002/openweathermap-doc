### **`docs/authentication.md`**

````markdown
# Authentication

## API Key Access

All OpenWeather API requests require authentication using your unique API key (`appid`).  
This key identifies your application and ensures fair usage of our services.

---

### **Authentication Method**
- **Type:** API Key
- **Location:** Query Parameter
- **Parameter Name:** `appid`

---

### **Example Request**
```http
GET https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY
````

---

### **Obtaining an API Key**

1. Sign up for a free OpenWeather account at [openweathermap.org](https://openweathermap.org/).
2. Navigate to **My API Keys** in your dashboard.
3. Copy your key and store it securely.

> **Tip:** Never share your API key publicly. For security, store it in environment variables or secure configuration files.

````