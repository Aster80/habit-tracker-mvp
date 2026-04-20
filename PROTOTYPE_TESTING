Telling AI to Create the RPD ~

I need you to create a single-page web application based on this PRD:

[<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Habit Tracker MVP</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f4f6f8;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
        }

        .container {
            margin-top: 50px;
            background: white;
            padding: 20px 30px;
            border-radius: 10px;
            width: 350px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        h1 {
            text-align: center;
        }

        .input-section {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }

        input {
            flex: 1;
            padding: 8px;
        }

        button {
            padding: 8px 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            background: #4CAF50;
            color: white;
        }

        button:hover {
            background: #45a049;
        }

        ul {
            list-style: none;
            padding: 0;
        }

        li {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #f9f9f9;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
        }

        .completed {
            text-decoration: line-through;
            color: gray;
        }

        .complete-btn {
            background: #2196F3;
        }

        .complete-btn:hover {
            background: #1976D2;
        }

        .delete-btn {
            background: #f44336;
            margin-left: 5px;
        }

        .delete-btn:hover {
            background: #d32f2f;
        }

        .progress {
            text-align: center;
            margin-top: 15px;
            font-weight: bold;
        }

        .error {
            color: red;
            text-align: center;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Habit Tracker</h1>

    <div class="error" id="error"></div>

    <div class="input-section">
        <input type="text" id="habitInput" placeholder="Enter a habit">
        <button onclick="addHabit()">Add</button>
    </div>

    <ul id="habitList"></ul>

    <div class="progress" id="progress">0 / 0 completed</div>
</div>

<script>
    const habitInput = document.getElementById("habitInput");
    const habitList = document.getElementById("habitList");
    const progress = document.getElementById("progress");
    const errorDiv = document.getElementById("error");

    let habits = [];

    // Add Habit
    function addHabit() {
        const habitText = habitInput.value.trim();

        if (habitText === "") {
            errorDiv.textContent = "Please enter a habit!";
            return;
        }

        errorDiv.textContent = "";

        const habit = {
            text: habitText,
            completed: false
        };

        habits.push(habit);
        habitInput.value = "";

        renderHabits();
    }

    // Toggle Complete
    function toggleComplete(index) {
        habits[index].completed = !habits[index].completed;
        renderHabits();
    }

    // Delete Habit
    function deleteHabit(index) {
        habits.splice(index, 1);
        renderHabits();
    }

    // Render UI
    function renderHabits() {
        habitList.innerHTML = "";

        habits.forEach((habit, index) => {
            const li = document.createElement("li");

            const span = document.createElement("span");
            span.textContent = habit.text;

            if (habit.completed) {
                span.classList.add("completed");
            }

            const buttonContainer = document.createElement("div");

            const completeBtn = document.createElement("button");
            completeBtn.textContent = "Complete";
            completeBtn.className = "complete-btn";
            completeBtn.onclick = () => toggleComplete(index);

            const deleteBtn = document.createElement("button");
            deleteBtn.textContent = "Delete";
            deleteBtn.className = "delete-btn";
            deleteBtn.onclick = () => deleteHabit(index);

            buttonContainer.appendChild(completeBtn);
            buttonContainer.appendChild(deleteBtn);

            li.appendChild(span);
            li.appendChild(buttonContainer);

            habitList.appendChild(li);
        });

        updateProgress();
    }

    // Update Progress
    function updateProgress() {
        const completed = habits.filter(h => h.completed).length;
        progress.textContent = `${completed} / ${habits.length} completed`;
    }
</script>

</body>
</html>]


Requirements:
- Single HTML file with embedded CSS and JavaScript
- No external dependencies
- Works in browser
- Include comments

Generate the complete code.
