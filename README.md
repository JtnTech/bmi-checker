# 🧮 BMI Calculator (HTML • CSS • JavaScript)

A responsive **BMI (Body Mass Index) Calculator** built using **pure HTML, CSS, and JavaScript**.  
It includes **Dark Mode**, smooth UI effects, and mobile responsiveness.

---

## 🚀 Features

- ✅ Calculate BMI using height (cm) & weight (kg)
- 🌗 Dark / Light mode toggle
- 📱 Fully responsive (mobile friendly)
- 🎨 Animated UI & smooth transitions
- ⚠️ Input validation with clear messages

---

## 📸 Preview

> Open the file in your browser to see the live calculator.
> 
> <img width="815" height="675" alt="bmi scr" src="https://github.com/user-attachments/assets/2b64376f-134e-4193-a41e-349ad7f15f72" />


---

## 📂 Project Structure

```text
bmi-calculator/
│
├── index.html
└── README.md
```

**🧑‍💻 How to Use**

- **Download** or **clone** the repository

Open **index.html** in any browser

Enter:
Height in CM
Weight in KG

- Click Calculate
- Toggle **Dark Mode** if you like 🌙

# 🧾 Source Code
**index.html**

```html
  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BMI calculator</title>

    <!-- CSS -->
    <style>
        body {
            text-align: center;
            transition: background-color 0.3s ease;
            text-transform: capitalize;
            font-family: "Audiowide", serif;
        }

        *::selection {
            color: chartreuse;
        }

        .container {
            margin: 50px auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 80vh;
        }

        fieldset {
            max-width: 40vw;
            padding: 20px;
            border-radius: 10px;
            border: 1px solid black;
            box-shadow: 0px 0px 10px rgba(0,0,0,0.1);
        }

        input, button {
            margin-top: 10px;
            padding: 8px;
            border-radius: 5px;
        }

        #btn {
            background-color: rgb(104, 172, 255);
            color: white;
            border: none;
            cursor: pointer;
        }

        #btn:hover {
            background-color: transparent;
            border: 1px solid black;
            color: black;
        }

        .dark-mode {
            background-color: #1a1a1a;
            color: white;
        }
    </style>
</head>

<body>

<div class="container">
    <button id="btnbg">Enable Dark Mode</button>

    <fieldset>
        <legend>BMI Calculator</legend>

        <label>Height in CM</label>
        <input type="text" id="height">

        <label>Weight in KG</label>
        <input type="text" id="weight">

        <button id="btn">Calculate</button>

        <div id="results">Your result will appear here</div>
    </fieldset>
</div>

<script>
    const btnbg = document.getElementById("btnbg");
    const body = document.body;

    btnbg.addEventListener("click", () => {
        body.classList.toggle("dark-mode");
        btnbg.innerText = body.classList.contains("dark-mode")
            ? "Disable Dark Mode"
            : "Enable Dark Mode";
    });

    document.getElementById("btn").addEventListener("click", () => {
        const h = parseFloat(height.value);
        const w = parseFloat(weight.value);
        const r = document.getElementById("results");

        if (!h || !w) {
            r.innerHTML = "Please enter valid values!";
            r.style.color = "red";
            return;
        }

        const bmi = (w / (h/100) ** 2).toFixed(2);
        r.innerHTML = `Your BMI is ${bmi}`;
        r.style.color = "green";
    });
</script>

</body>
</html>

```

| Category    | BMI Range   |
| ----------- | ----------- |
| Underweight | < 18.6      |
| Normal      | 18.6 – 24.9 |
| Overweight  | 25 – 29.9   |


 # 🔗 Connect with JtnTech

📺 **YouTube:** https://www.youtube.com/@jatintrails

💻 **GitHub:** https://github.com/JtnTech

- ⭐ If this repo helped you, don’t forget to star it and subscribe!
