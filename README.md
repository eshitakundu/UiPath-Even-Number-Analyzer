# UiPath Even Number Analyzer

## Overview
This project demonstrates a simple **UiPath automation** designed to receive a user’s input and determine whether the input is an even or odd number. The automation includes multiple workflows to handle user input, number validation, and interaction using dialog boxes.

The solution showcases how UiPath can handle user interactions, logic conditions, and error handling, providing a flexible framework that can be expanded for more complex processes.

## Features
- Prompts the user to input a number.
- Uses a **Try-Catch block** to handle invalid or non-numeric input.
- **If-Else logic** to check whether the number is even or odd.
- Provides the user with an option to continue or exit the process.
- Exception handling for invalid inputs.

## Workflows
### 1. **Main Workflow**
The central workflow manages the flow of the process, invoking other workflows to handle specific tasks. It uses:
- A **Do While** loop to keep prompting the user for inputs until they choose to exit.
- Variables like `userdecision`, `input_number`, and `number` to manage user input and control the process flow.

### 2. **InputNumber Workflow**
This workflow:
- Takes user input using the **Input Dialog** activity.
- Handles exceptions (non-numeric input) using a **Try-Catch** block.
- Converts the string input into an integer and passes it back to the main workflow through the `out_number` argument.

### 3. **IsEven Workflow**
This workflow:
- Receives the number from the main workflow.
- Uses an **If-Else** condition to check if the number is even (`number mod 2 = 0`).
- Displays the result to the user via a **Message Box**.

## Getting Started
### Prerequisites
- **UiPath Studio**: Make sure you have UiPath Studio installed on your machine.
- Basic knowledge of UiPath and how workflows are designed in the platform.

### Installation Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/eshitakundu/UiPath-Even-Number-Analyzer.git
   ```
2. Open the project in **UiPath Studio**.
3. Run the `Main.xaml` file to start the automation.

## How It Works
1. The user is prompted to enter a number.
2. If the input is invalid (non-numeric), the user is asked to enter a valid number.
3. If the input is valid, the automation checks if the number is even or odd and displays the result.
4. The user is then asked if they want to check another number or exit the process.

## Project Structure
- **Main.xaml**: The main workflow file.
- **InputNumber.xaml**: The workflow handling user input and error handling.
- **IsEven.xaml**: The workflow checking if the input number is even or odd.
- **Flowchart.xaml**: The flowchart showing the working of the project.
- **README.md**: This file.

## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute this project.
