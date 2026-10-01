function convertTemperature() {

    // Get values from the form

    const input =
        document.getElementById("temperature").value;

    const fromUnit =
        document.getElementById("fromUnit").value;

    const toUnit =
        document.getElementById("toUnit").value;

    const error =
        document.getElementById("error");

    const resultBox =
        document.getElementById("resultBox");

    const result =
        document.getElementById("result");


    // Clear old messages

    error.textContent = "";
    resultBox.style.display = "none";


    // Check if input is empty

    if (input.trim() === "") {

        error.textContent =
            "Please enter a temperature.";

        return;
    }


    // Convert input to number

    const temperature = Number(input);


    // Check for invalid number

    if (isNaN(temperature)) {

        error.textContent =
            "Please enter a valid number.";

        return;
    }


    // Check absolute zero

    if (
        fromUnit === "celsius" &&
        temperature < -273.15
    ) {

        error.textContent =
            "Celsius cannot be below -273.15°C.";

        return;
    }


    if (
        fromUnit === "fahrenheit" &&
        temperature < -459.67
    ) {

        error.textContent =
            "Fahrenheit cannot be below -459.67°F.";

        return;
    }


    if (
        fromUnit === "kelvin" &&
        temperature < 0
    ) {

        error.textContent =
            "Kelvin cannot be below 0 K.";

        return;
    }


    // Convert input to Celsius first

    let celsius;


    if (fromUnit === "celsius") {

        celsius = temperature;

    }
    else if (fromUnit === "fahrenheit") {

        celsius =
            (temperature - 32) * 5 / 9;

    }
    else if (fromUnit === "kelvin") {

        celsius =
            temperature - 273.15;

    }


    // Convert Celsius to selected unit

    let convertedTemperature;


    if (toUnit === "celsius") {

        convertedTemperature =
            celsius;

    }
    else if (toUnit === "fahrenheit") {

        convertedTemperature =
            (celsius * 9 / 5) + 32;

    }
    else if (toUnit === "kelvin") {

        convertedTemperature =
            celsius + 273.15;

    }


    // Choose unit symbol

    let symbol;


    if (toUnit === "celsius") {

        symbol = "°C";

    }
    else if (toUnit === "fahrenheit") {

        symbol = "°F";

    }
    else {

        symbol = "K";

    }


    // Show result

    result.textContent =
        convertedTemperature.toFixed(2) + " " + symbol;

    resultBox.style.display = "block";
}


// Connect button to function

document
    .getElementById("convertButton")
    .addEventListener("click", convertTemperature);
