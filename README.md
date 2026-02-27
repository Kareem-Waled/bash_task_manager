# 📝 Mini Task Manager

A simple command-line Task Management System built with **Bash scripting**.  
Manage your daily tasks directly from the terminal with full CRUD operations and reports.

---

## 🚀 Getting Started

```bash
# 1. Clone the repo
git clone https://github.com/your-username/task-manager.git
cd task-manager

# 2. Give permission
chmod +x task_manager.sh

# 3. Run
bash task_manager.sh
```

---

## 📋 Features

| Feature | Description |
|---------|-------------|
| ➕ Add Task | Add a new task with title, priority, and due date |
| 📄 List Tasks | Display all tasks in a formatted table |
| ✏️ Update Task | Change the status of a task by ID |
| 🗑️ Delete Task | Delete a task by ID with confirmation |
| 🔍 Search | Search tasks by keyword in the title |
| 📊 Report | Summary of tasks and overdue list |

---

## 🗂️ Data Storage

All tasks are stored in a plain text file `tasks.txt`.  
Each task is saved as one line with fields separated by `|`:

```
ID|Title|Priority|Due Date|Status
1|Buy groceries|low|2025-03-01|pending
2|Fix bug|high|2025-02-20|done
```

---

## 🎮 Usage

```
=== Task Manager ===
1) Add task
2) List tasks
3) Update task
4) Delete task
5) Search
6) Report
7) Exit
Choose:
```

### Add a Task
```
Title: Fix login bug
Priority (high/medium/low): high
Due date (YYYY-MM-DD): 2025-03-10
✓ Task added!
```

### List Tasks
```
ID    Title                Priority   Due Date     Status
------------------------------------------------------------
1     Fix login bug        high       2025-03-10   pending
2     Write report         medium     2025-03-15   in-progress
```

### Update Task
```
Task ID: 1
New status (pending/in-progress/done): done
✓ Task updated!
```

---

## ✅ Input Validation

- Title must not be empty or contain special characters
- Priority must be `high`, `medium`, or `low`
- Date must follow the format `YYYY-MM-DD`
- ID must exist before update or delete

---

## 🎨 Colored Output

| Color | Meaning |
|-------|---------|
| 🔴 Red | High priority / Error messages |
| 🟡 Yellow | Medium priority |
| 🟢 Green | Low priority / Success messages |
| 🔵 Cyan | Headers |

---

## 🛠️ Tools Used

| Tool | Usage |
|------|-------|
| `grep` | Search and filter tasks |
| `sed` | Update and delete lines |
| `awk` | Generate new IDs |
| `read` | Get user input |
| `date` | Compare dates for overdue tasks |

---

## 📁 Project Structure

```
task-manager/
├── task_manager.sh   # Main script
├── tasks.txt         # Data file (auto-created)
└── README.md         # Documentation
```

---

## 📌 Requirements

- Linux / macOS / WSL on Windows
- Bash 4.0+

---

## 👤 Author

Made with ❤️ using Bash
