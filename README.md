# **Capital City Quiz**

A fun and educational web application where users can test their knowledge of world capitals. The game challenges players to guess the capital city of a randomly selected country, keeping track of the total correct answers in a single session.

---

## **Features**
- **Dynamic Questions**:
  - Randomly selects a country from the database for each round.
- **Real-Time Feedback**:
  - Indicates whether the submitted answer is correct or incorrect immediately after submission.
- **Scoring System**:
  - Tracks the total number of correct answers during the session.
- **Game Over Prompt**:
  - Ends the game when the user submits an incorrect answer and displays the final score.
- **Restart Mechanism**:
  - Offers a seamless option to restart the quiz after the game ends.

---

## **How to Play**
1. The name of a random country is displayed on the screen.
2. Type the name of its capital city in the input field.
3. Submit your answer:
   - If correct, your score increases, and a new question is displayed.
   - If incorrect, the game ends and displays your final score.
4. Restart the game to try and beat your score.

---

## **Technologies Used**
- **Node.js**: Backend runtime environment for handling server-side logic.
- **Express.js**: Framework for routing and middleware integration.
- **PostgreSQL**: Database for storing country and capital city data.
- **EJS (Embedded JavaScript Templates)**: For rendering dynamic front-end content.
- **CSS**: For styling the interface.
- **JavaScript**:
  - Backend logic for question generation and answer validation.
  - Frontend dynamic features like feedback and restart logic.
- **dotenv**: For managing environment variables securely.
- **body-parser**: Middleware for parsing form data.

---

## **Getting Started**

### **Prerequisites**
- **Node.js**: To run the server-side code.
- **PostgreSQL**: Ensure PostgreSQL is installed and running on your system.

---

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/Ayu1404/Capital-Quiz.git
   cd Capital-Quiz
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up the `.env` file in the root directory with your PostgreSQL credentials:
   ```plaintext
   DB_USER=your_database_user
   DB_HOST=your_database_host
   DB_NAME=your_database_name
   DB_PASSWORD=your_database_password
   DB_PORT=your_database_port
   ```

4. Populate the database:
   - Ensure the `capitals` table contains the necessary data:
     - **country**: The name of the country.
     - **capital**: The capital city of the country.

5. Start the server:
   ```bash
   node app.js
   ```

6. Open your browser and navigate to:
   ```plaintext
   http://localhost:3000
   ```

---

## **Database Schema**
The **capitals** table should have the following structure:

| Column Name | Data Type | Description                 |
|-------------|-----------|-----------------------------|
| **id**      | INTEGER   | Unique identifier for each entry. |
| **country** | TEXT      | The name of the country.    |
| **capital** | TEXT      | The capital city of the country. |

---

## **Project Structure**
### **Server-Side (app.js)**:
- **GET `/`**:
  - Initializes the game and displays the first question.
- **POST `/submit`**:
  - Checks the submitted answer against the current question.
  - Updates the total score if correct and displays the next question.
  - Ends the game if the answer is incorrect.

### **Front-End (index.ejs)**:
- **Dynamic Content**:
  - Displays the country name and input field for the user to type their answer.
  - Provides visual feedback for correct or incorrect answers.
- **Restart Mechanism**:
  - Displays a restart button and a prompt when the game ends.

---

## **Usage**
1. **Start the Quiz**:
   - Open the app in your browser at `http://localhost:3000`.
2. **Submit Answers**:
   - Enter the name of the capital city corresponding to the displayed country.
   - Press the "SUBMIT" button to validate your answer.
3. **Track Your Score**:
   - View your current score in real time at the top of the screen.
4. **Restart the Game**:
   - When the game ends, restart with a fresh set of questions by clicking the restart button.

---

## **Contributing**
Contributions are welcome! To contribute:
1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## **License**
This project is licensed under the MIT License, allowing you to modify and distribute the project with proper attribution.

---

## **Acknowledgments**
- Inspired by a passion for geography and learning about countries and capitals.
- Thanks to the open-source libraries and frameworks that made this project possible.
