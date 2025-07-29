# Todo CLI Application

A simple command-line todo application built with Python, Typer, and SQLite. This tool helps you manage your tasks with categories, track completion status, and persists data in a local SQLite database.

## Features

- Add new tasks with a category
    
- List all tasks in a formatted table
    
- Update task descriptions and categories
    
- Mark tasks as completed
    
- Delete tasks
    
- Tasks are stored in a SQLite database (`todos.db`)
    

## Prerequisites

- Python 3.7 or newer
    
- Git (for version control and repository hosting)
    

## Installation

1. **Clone the repository**
    
    ```bash
    git clone https://github.com/<your-username>/todo-cli-app.git
    cd todo-cli-app
    ```
    
2. **Create and activate a virtual environment**
    
    ```bash
    python -m venv venv
    source venv/bin/activate   # On Windows: venv\\Scripts\\activate
    ```
    
3. **Install dependencies**
    
    ```bash
    pip install -r requirements.txt
    ```
    

## Project Structure

```
├── database.py       # SQLite database operations
├── model.py          # Todo model definition
├── todocli.py        # Typer-based CLI entry point
├── requirements.txt  # Python dependencies
└── README.md         # Project documentation
```

## Usage

Activate the virtual environment (if not already active):

```bash
source venv/bin/activate
```

Run the CLI tool:

```bash
python todocli.py [COMMAND] [OPTIONS]
```

### Commands

- `add [TASK] [CATEGORY]`
    
    - Adds a new todo item
        
    - Example: `python todocli.py add "Write blog post" "Learn"`
        
- `show`
    
    - Displays all todo items in a table
        
    - Example: `python todocli.py show`
        
- `update [POSITION] [--task TEXT] [--category TEXT]`
    
    - Updates the task or category of an existing item
        
    - Example: `python todocli.py update 2 --task "Read documentation"`
        
- `complete [POSITION]`
    
    - Marks a todo item as completed
        
    - Example: `python todocli.py complete 3`
        
- `delete [POSITION]`
    
    - Deletes a todo item
        
    - Example: `python todocli.py delete 1`
        

> Positions start at 1 when shown in the `show` command.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

1. Fork the repository
    
2. Create a feature branch (`git checkout -b feature/YourFeature`)
    
3. Commit your changes (`git commit -m 'Add some feature'`)
    
4. Push to the branch (`git push origin feature/YourFeature`)
    
5. Open a pull request
    

## License

This project is licensed under the MIT License. See the LICENSE file for details.

