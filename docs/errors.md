### **`docs/errors.md`**
```markdown
# Errors

## Error Response Format

When a request fails, the OpenWeather API returns an error object in the following format:

```json
{
  "status_code": 401,
  "status_message": "Invalid API key. Please see https://openweathermap.org/faq#error401 for more info.",
  "success": false
}
````

---

### **Fields**

| Field            | Type    | Description                                              |
| ---------------- | ------- | -------------------------------------------------------- |
| `status_code`    | integer | HTTP status code of the error.                           |
| `status_message` | string  | A descriptive message explaining the cause of the error. |
| `success`        | boolean | Will always be `false` in an error response.             |

---

### **Common Errors**

| Status Code | Meaning               | Cause                                      |
| ----------- | --------------------- | ------------------------------------------ |
| `401`       | Unauthorized          | Missing or invalid API key.                |
| `404`       | Not Found             | The requested resource could not be found. |
| `429`       | Too Many Requests     | Rate limit exceeded.                       |
| `500`       | Internal Server Error | Unexpected server-side issue.              |

---

### **Best Practices**

* Always validate your API key before making requests.
* Implement retry logic with exponential backoff for `500` errors.
* Monitor your usage in the OpenWeather dashboard to avoid rate limits.

```