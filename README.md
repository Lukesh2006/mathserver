# Ex.05 Design a Website for Server Side Processing
# Date:06.12.24
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Power of Lamp Filament Calculator</title>
  <style>
    /* Global Styles */
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(45deg, #1a1a2e, #16213e, #0f3460);
      color: #fff;
    }

    /* Container */
    .container {
      background-color: rgba(0, 0, 0, 0.7);
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
      width: 350px;
      text-align: center;
    }

    /* Heading */
    h1 {
      color: #fff;
      font-size: 24px;
      margin-bottom: 20px;
      font-weight: 500;
    }

    /* Form Labels */
    label {
      display: block;
      font-size: 16px;
      color: #ccc;
      margin-top: 20px;
      text-align: left;
    }

    /* Input fields */
    input {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      border: 1px solid #555;
      border-radius: 5px;
      background-color: #333;
      color: #fff;
      font-size: 16px;
    }

    input:focus {
      outline: none;
      border-color: #ff6f61;
    }

    /* Button Styles */
    button {
      margin-top: 25px;
      padding: 12px;
      background-color: #ff6f61;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 18px;
      cursor: pointer;
      width: 100%;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #ff4c3b;
    }

    /* Result Box */
    .result {
      margin-top: 25px;
      font-size: 18px;
      color: #d4d4d4;
      display: none;
    }

    .result h3 {
      color: #ff6f61;
      font-size: 22px;
    }

    /* Responsive Styles */
    @media (max-width: 600px) {
      .container {
        width: 90%;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Calculate the Power of Lamp Filament</h1>
    <form id="power-form">
      <label for="intensity">Intensity (I in Amperes):</label>
      <input type="number" id="intensity" step="any" required>

      <label for="resistance">Resistance (R in Ohms):</label>
      <input type="number" id="resistance" step="any" required>

      <button type="submit">Calculate Power</button>
    </form>

    <div id="result" class="result">
      <h3>Power (P) = <span id="power"></span> Watts</h3>
    </div>
  </div>

  <script>
    document.getElementById('power-form').addEventListener('submit', function(event) {
      event.preventDefault();

      const intensity = parseFloat(document.getElementById('intensity').value);
      const resistance = parseFloat(document.getElementById('resistance').value);

      if (isNaN(intensity) || isNaN(resistance) || intensity <= 0 || resistance <= 0) {
        alert("Please enter valid positive numbers for intensity and resistance.");
        return;
      }

      const intensitySquared = intensity * intensity;  
      const power = intensitySquared * resistance;   

      document.getElementById('power').textContent = power.toFixed(2);
      document.getElementById('result').style.display = 'block';
    });
  </script>

</body>
</html>

```

# SERVER SIDE PROCESSING:
![server1](https://github.com/user-attachments/assets/112f2b8b-2275-4c96-8a4a-1ffa775bb410)
![server 2](https://github.com/user-attachments/assets/a8586c07-6ad8-4cef-883e-9dba0ae1a254)


# HOMEPAGE:

![sever 3](https://github.com/user-attachments/assets/2d05d087-d1c0-4d86-9808-603b074b04cc)

# RESULT:
The program for performing server side processing is completed successfully.
