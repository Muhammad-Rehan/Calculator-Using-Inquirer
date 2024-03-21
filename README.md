## Mini Calculator using Inquirer

- I have designed this calculator using inquiurer. Once run this program, this will ask the operator for which you would like to perform your calculation. After that, they ask the first number and then second number. You may see below the code as well.

## Code

```typescript
#! /usr/bin/env node

import inquirer from "inquirer";

let calculation = await inquirer.prompt([
  {
    type: "list",
    name: "operators",
    message: "Choose your operator to perform the calculation",
    choices: ["+", "-", "*", "/", "%"],
  },
]);

if (calculation.operators == "+") {
  let inputNumber = await inquirer.prompt([
    {
      type: "number",
      name: "number1",
      message: "Enter your first Number?",
    },
    {
      type: "number",
      name: "number2",
      message: "Enter your second Number?",
    },
  ]);
  console.log(
    `${inputNumber.number1} ${calculation.operators} ${inputNumber.number2} =`,
    inputNumber.number1 + inputNumber.number2
  );
} else if (calculation.operators == "-") {
  let inputNumber = await inquirer.prompt([
    {
      type: "number",
      name: "number1",
      message: "Enter your first Number?",
    },
    {
      type: "number",
      name: "number2",
      message: "Enter your second Number?",
    },
  ]);
  console.log(
    `${inputNumber.number1} ${calculation.operators} ${inputNumber.number2} =`,
    inputNumber.number1 - inputNumber.number2
  );
} else if (calculation.operators == "*") {
  let inputNumber = await inquirer.prompt([
    {
      type: "number",
      name: "number1",
      message: "Enter your first Number?",
    },
    {
      type: "number",
      name: "number2",
      message: "Enter your second Number?",
    },
  ]);
  console.log(
    `${inputNumber.number1} ${calculation.operators} ${inputNumber.number2} =`,
    inputNumber.number1 * inputNumber.number2
  );
} else if (calculation.operators == "/") {
  let inputNumber = await inquirer.prompt([
    {
      type: "number",
      name: "number1",
      message: "Enter your first Number?",
    },
    {
      type: "number",
      name: "number2",
      message: "Enter your second Number?",
    },
  ]);
  console.log(
    `${inputNumber.number1} ${calculation.operators} ${inputNumber.number2} =`,
    inputNumber.number1 / inputNumber.number2
  );
} else if (calculation.operators == "%") {
  let inputNumber = await inquirer.prompt([
    {
      type: "number",
      name: "number1",
      message: "Enter your first Number?",
    },
    {
      type: "number",
      name: "number2",
      message: "Enter your second Number?",
    },
  ]);
  console.log(
    `${inputNumber.number1} ${calculation.operators} ${inputNumber.number2} =`,
    inputNumber.number1 % inputNumber.number2
  );
}

```

### Output Of Above Code

![Program Output](output.png)