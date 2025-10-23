# ICS-Quadratic-Grader-Kamfwa-Nathan
```markdown
# Quadratic Equation Solver and Grading System

The application is built using HTML, CSS, and JavaScript, with a modern, user-friendly interface styled using CSS custom properties for a consistent color scheme.

## Features
- **Quadratic Solver**:
  - Accepts coefficients \( a \), \( b \), and \( c \) as inputs.
  - Validates inputs to ensure they are valid numbers and that \( a \neq 0 \).
  - Computes the discriminant (\( D = b^2 - 4ac \)) and determines the roots:
    - Two distinct real roots if \( D > 0 \).
    - One repeated real root if \( D = 0 \).
    - Two complex conjugate roots if \( D < 0 \).
  - Displays results with roots rounded to four decimal places.
  - Includes error handling for invalid inputs.
  - Provides a reset button to clear inputs and results.

- **Grading System**:
  - Accepts a student number, student name, and a numeric score (0–100).
  - Validates the score to ensure it is an integer between 0 and 100.
  - Assigns a letter grade based on the following scale:
    - 85–100: A+
    - 75–84: A
    - 65–74: B+
    - 60–64: B
    - 55–59: C+
    - 50–54: C
    - 0–49: D
  - Displays the score and corresponding grade.
  - Includes error handling for invalid scores.
  - Provides a reset button to clear inputs and results.

- **User Interface**:
  - Responsive design with a clean layout optimized for various screen sizes.
  - Styled using a custom color palette defined with CSS variables.
  - Includes input validation with error messages displayed below each input field.
  - Features interactive buttons with hover effects and smooth transitions.
  - Results are displayed in styled result boxes for clarity.

## File Structure
- `index.html`: The main HTML file containing the structure, styling, and JavaScript logic for the application.
- No external dependencies or additional files are required.

## Setup and Usage
1. **Prerequisites**:
   - A modern web browser (e.g., Chrome, Firefox, Edge, Safari).
   - No additional software or libraries are needed.

2. **Running the Application**:
   - Clone or download the repository to your local machine.
   - Open `index.html` in a web browser.
   - Alternatively, host the file on a local or remote server for web access.

3. **Using the Quadratic Solver**:
   - Enter the coefficients \( a \), \( b \), and \( c \) in the provided input fields.
   - Click the "Compute" button to calculate and display the roots.
   - Click the "Reset" button to clear all inputs and results.
   - Error messages will appear if inputs are invalid (e.g., non-numeric values or \( a = 0 \)).

4. **Using the Grading System**:
   - Enter the student number, student name, and a numeric score (0–100).
   - Click the "Compute" button to display the corresponding letter grade.
   - Click the "Reset" button to clear all inputs and results.
   - An error message will appear if the score is invalid (e.g., outside the 0–100 range).

## Code Details
- **HTML**:
  - Structured with semantic elements and organized into two sections: Quadratic Solver and Grading System.
  - Uses input fields with appropriate attributes (e.g., `type="number"`, `step="any"`, `min`, `max`).
  - Includes result boxes and error message spans for user feedback.

- **CSS**:
  - Utilizes CSS custom properties (`--primary-color`, `--secondary-color`, etc.) for a consistent color scheme.
  - Implements a responsive design with flexbox for centering the container.
  - Includes styles for buttons, inputs, and result boxes with hover effects and transitions.
  - Uses a modern font stack (`Segoe UI`, Tahoma, etc.) for readability.

- **JavaScript**:
  - **Quadratic Solver** (`solveQuadratic`):
    - Parses input values and validates them.
    - Calculates the discriminant and determines the type of roots.
    - Formats output using template literals (with fixed decimal places for readability).
    - Handles errors by displaying messages in the UI.
  - **Reset Quadratic** (`resetQuadratic`):
    - Clears all input fields, error messages, and the result box.
  - **Grading System** (`getGrade`):
    - Validates the score and assigns a letter grade based on the defined scale.
    - Displays the result or an error message for invalid inputs.
  - **Reset Grade** (`resetGrade`):
    - Clears the score input, error message, and result box.
  - Note: The student number and name fields are included in the UI but are not currently used in the JavaScript logic.

## Known Issues
- The JavaScript code contains syntax errors in the `solveQuadratic` and `getGrade` functions where template literals are incorrectly used within string concatenation (e.g., `output += <p>...</p>`). These should be fixed by using proper template literals or string concatenation.
- The student number and name fields in the Grading System section are not validated or used in the output, which may be incomplete functionality.
- The error message spans for student number and name (`student_number_error`, `Student_name_error`) lack the `error` class, which may affect styling consistency.

## Future Improvements
- Fix the syntax errors in the JavaScript template literals to ensure proper HTML output.
- Add validation for the student number and name fields (e.g., check for non-empty values or specific formats).
- Include the student number and name in the grading system output for a more complete result.
- Enhance accessibility by adding ARIA attributes and keyboard navigation support.
- Add unit tests for the JavaScript functions to ensure reliability.
- Consider adding a history feature to display previous calculations or grades.

