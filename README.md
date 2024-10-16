# TaskTracker

![Annotation 2024-10-10 184628](https://github.com/user-attachments/assets/23f7abf4-ab68-4c37-9f2e-e8e0f25f4912)

# Live Demo
- https://webtasktracker.vercel.app /  https://task-tracker-jyotdhameliagmailcoms-projects.vercel.app

# Overview
- TaskTracker is a simple task management tool with easy to use user interface. just by login with your google account you can store your tasks in this tool.
- Stay on top of your tasks with TaskTracker. Simple, effective task management tool.
- 'Where goals become accomplishments'

# Features
- Secure: TaskTracker Provides you the google authentication to store your information for forever in the google server so that you can easily access your data in any device at any time by just logging in with that same google account.
- Add Task: by just typing your todo in the textbox and pressing enter key will save your task and you can see that immediately below the input box.
- Edit Task: mistakes happens, no need to worry, TaskTracker provides you the functionality of edit button with that you can edit your existing task once you do that old task will be replaced by a new one which you have just added.
- Delete Task: achieved the goal ? or completed the task ? delete that tasks by just clicking on the delete button and it will delete that task from your account for forever.
- Logout: after your work is done with this tool just click on logout.

![Annotation 2024-10-10 184652](https://github.com/user-attachments/assets/a635cf16-6b9f-45f8-a02e-76ee7734e465)

# Get Started
- To get satrted with TaskTracker follow this steps:
 1. Clone the Repository: `https://github.com/JyotDhamelia/TaskTracker.git`
 2. Update .env file: `go to your firebase project find the details and update the values in the .env`
 3. Navigate to the project directory: `cd TaskTracker`
 4. Install Dependencies: `npm install`
 5. Run the website: `npm run dev`
 6. Open the website in a browser: `http://localhost:5173`

 Note: go to firestore database then click on the Rules tab and notice that your rules are same as described below if not then update that rules.

```js
// This is sample firestore database roles 
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId}/tasks/{taskId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}
```


# License
- This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
