# Ex03 To-Do List using JavaScript
## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .todo-container {
      background: white;
      width: 350px;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px gray;
      text-align: center;
    }
    h2 {
      color: #333;
    }
    input {
      width: 70%;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      padding: 8px 12px;
      background: #28a745;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background: #218838;
    }
    ul {
      list-style: none;
      padding: 0;
      margin-top: 15px;
    }
    li {
      background: #e9ecef;
      margin: 5px 0;
      padding: 8px;
      border-radius: 5px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    li.completed {
      text-decoration: line-through;
      color: gray;
    }
    .delete-btn {
      background: red;
      color: white;
      border: none;
      border-radius: 5px;
      padding: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="todo-container">
    <h2>📝 To-Do List</h2>
    <input type="text" id="taskInput" placeholder="Enter a new task">
    <button onclick="addTask()">Add</button>

    <ul id="taskList"></ul>
  </div>

  <script>
    function addTask() {
      const taskInput = document.getElementById("taskInput");
      const taskList = document.getElementById("taskList");
      const taskText = taskInput.value.trim();

      if (taskText === "") {
        alert("Please enter a task!");
        return;
      }

      const li = document.createElement("li");
      li.textContent = taskText;

      li.addEventListener("click", function () {
        li.classList.toggle("completed");
      });

      const delBtn = document.createElement("button");
      delBtn.textContent = "Delete";
      delBtn.classList.add("delete-btn");
      delBtn.onclick = function () {
        taskList.removeChild(li);
      };

      li.appendChild(delBtn);
      taskList.appendChild(li);
      taskInput.value = "";
    }
  </script>
</body>
</html>

```

## OUTPUT

<img width="1919" height="892" alt="image" src="https://github.com/user-attachments/assets/764046d7-a274-4f64-bb60-9328118d2b94" />

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
