# exercice-3
exercice 3 


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>
       <u> EXERCICE 3 : Calculatrice + - / *. </u>
    </h1>
    <div class="calculator">
        <form id="calculator-form">
          <input type="number" id="first-number" placeholder="Premier nombre" required>
          <input type="number" id="second-number" placeholder="Deuxième nombre" required>
          <select id="operation">
            <option value="add">Addition</option>
            <option value="subtract">Soustraction</option>
            <option value="multiply">Multiplication</option>
            <option value="divide">Division</option>
          </select>
          <button type="submit">Calculer</button>
        </form>
        <p id="result"></p>
      </div>


      <script>
document.getElementById('calculator-form').addEventListener('submit', function(event) {
  event.preventDefault();

  #The code retrieves the values of "first-number," "second-number," and "operation" input elements from the HTML document and assigns them to the corresponding variables.

  var firstNumber = document.getElementById('first-number').value;
  var secondNumber = document.getElementById('second-number').value;
  var operation = document.getElementById('operation').value;

  var result;


  # The code performs arithmetic operations based on the value of the "operation" variable and calculates the result using the "firstNumber" and "secondNumber" variables.

  switch (operation) {
    case "add":
      result = Number(firstNumber) + Number(secondNumber);
      break;
    case "subtract":
      result = Number(firstNumber) - Number(secondNumber);
      break;
    case "multiply":
      result = Number(firstNumber) * Number(secondNumber);
      break;
    case "divide":
      if (secondNumber != 0) {
        result = Number(firstNumber) / Number(secondNumber);
      } else {
        result = "Erreur : division par zéro non autorisée.";
      }
      break;
    default:
      result = "Erreur : opération non valide.";
  }

  document.getElementById('result').textContent = 'Résultat : ' + result;
});

      </script>
</body>
</html>

<style>
.calculator {
  width: 500px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 25px;
}

#calculator-form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

#calculator-form input,
#calculator-form select,
#calculator-form button {
  padding: 10px;
  font-size: 16px;
}

#calculator-form button {
  background-color: #121412;
  color: white;
  cursor: pointer;
}




#calculator-form input[type="text"],
#calculator-form select {
  background-color: rgb(10, 90, 229);
  color: white;
  border: 1px solid #ccc;
  border-radius: 5px;
}

#calculator-form button[type="submit"] {
  background-color: rgb(219, 8, 8);
  color: white;
  cursor: pointer;
}

#calculator-form button[type="submit"]:hover {
  background-color: #191919;
}

h1{
    text-align: center;
    margin-top: 20px;
}
#result{
  text-align: center;
  color: green;
}
</style>
