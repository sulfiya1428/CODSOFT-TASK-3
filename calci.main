<script>
    let currentInput = "";
    let resultDisplayed = false;

    const inputField = document.getElementById("answer");
    const numberButtons = document.querySelectorAll(".num");
    const operatorButtons = document.querySelectorAll(".operator");
    const clearButton = document.getElementById("clear");
    const equalsButton = document.getElementById("equals");

    
    numberButtons.forEach(button => {
      button.addEventListener("click", () => {
        if (resultDisplayed) {
          currentInput = button.value;
          resultDisplayed = false;
        } else {
          currentInput += button.value;
        }
        inputField.value = currentInput;
      });
    });

    
    operatorButtons.forEach(button => {
      button.addEventListener("click", () => {
        if (!resultDisplayed) {
          currentInput += " " + button.value + " ";
          inputField.value = currentInput;
        }
      });
    });

    
    clearButton.addEventListener("click", () => {
      currentInput = "";
      inputField.value = "";
    });

    equalsButton.addEventListener("click", () => {
      try {
        currentInput = eval(currentInput);
        inputField.value = currentInput;
        resultDisplayed = true;
      } catch (error) {
        inputField.value = "Error";
      }
    });
  </script>

