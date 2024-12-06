Problem Statement

The Demo Quiz App is a simple web-based application designed to test and enhance users' knowledge on javascript, html, and CSS. Should the user get every question wrong, out of 5 questions, the demo will present a 0/5 and the user will either get to retry or quit the web app. The result of using this app is hopefully an increase of knowledge in javascript, html, and or CSS.

Functional Features of the App

 - Live hover effects for mouse
 - Rules listed of app:

    "1. You will have only 15 seconds per each question.
    2. Once you select your answer, it can't be undone.
    3. You can't select any option once time goes off.
    4. You can't exit from the Quiz while you're playing.
    5. You'll get points on the basis of your correct answers."

 - If the user gets a question wrong, the wrong selected question turns red with an X and the correct answer is shown.
 - Tracks and displays user score.

 Directory Structure and Setup

 --> index.html # Main html file for hosting the app
 --> css/style.css # Main css file for all web app stlying
 --> js/questions.js #contains questions and answers for webapp
 --> js/quizApp.js # Handles javascript functionality like button handling and user interaction. Points saving

Explanation of the Codebase

index.html:

 <!-- Instruction box wrapper -->
    <div class="info_box">
        <div class="info-title"><span>Some Rules of this Quiz</span></div>
        <div class="info-list">
            <div class="info">1. You will have only <span>15 seconds</span> per each question.</div>
            <div class="info">2. Once you select your answer, it can't be undone.</div>
            <div class="info">3. You can't select any option once time goes off.</div>
            <div class="info">4. You can't exit from the Quiz while you're playing.</div>
            <div class="info">5. You'll get points on the basis of your correct answers.</div>
        </div>
        <div class="buttons">
            <button class="quit">Exit Quiz</button>
            <button class="restart">Continue</button>
        </div>
    </div>

     - info box wrapper which contains basic instructions to the user

questions.js:

    let questions = [
    {
        numb: 1,
        question: "What does HTML stand for?",
        answer: "Hyper Text Markup Language",
        options: [
        "Hyper Text Preprocessor",
        "Hyper Text Markup Language",
        "Hyper Text Multiple Language",
        "Hyper Tool Multi Language",
        ],
    },

    - This is an example of how thwe questuions are stored in the js file

quizApp.js:

    // if startQuiz button clicked
start_btn.addEventListener("click", (e) => {
  info_box.classList.add("activeInfo"); //show info box
});

// if exitQuiz button clicked
exit_btn.addEventListener("click", (e) => {
  info_box.classList.remove("activeInfo"); //hide info box
});

     - Example of how this handles button functionality and user interaction

