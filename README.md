
# Activity 12: Project UML Diagram


For this activity, you will develop a simple UML diagram in markdown to show how your classes will connect for your final project assignment.

In Python, a module is a file that contains related classes and functions. Your UML diagram will help you plan which classes go into which modules (files), and how those modules will import and interact with each other in your project.

## Instructions

1. Think about the main classes in your project and how they interact.
2. Draw a simple UML diagram in markdown to show:
   - The classes you plan to create
   - How they connect (if at all)
   - How `main.py` orchestrates the application
3. Use the template in `project_diagram/diagram.md` to sketch your project structure.

## Example 1: Two Connected Classes

```markdown
        +-------------------+
        |     ClassA        |
        |  do_task_a()      |
        |  get_data()       |
        +-------------------+
           ^       
           |       
           |       
   +-------------------+   +-------------------+
   |     main.py       |-->|     ClassB        |
   |     main()        |   |  do_task_b()      |
   +-------------------+   |  process_data()   |
                           +-------------------+
```

- `main.py` is in the center, with arrows pointing to each class.
- `main.py` creates instances of `ClassA` and `ClassB` inside the `main()` function.
- `ClassA` has methods like `do_task_a()` and `get_data()`.
- `ClassB` has methods like `do_task_b()` and `process_data()` and uses or interacts with `ClassA` (e.g., calls its methods or stores a reference).

## Example 2: Two Unconnected Classes

```markdown
        +-------------------+
        |     ClassA        |
        |  do_task_a()      |
        |  get_data()       |
        +-------------------+
           ^       
           |       
           |       
   +-------------------+   +-------------------+
   |     main.py       |-->|     ClassB        |
   |     main()        |   |  do_task_b()      |
   +-------------------+   |  process_data()   |
                           +-------------------+
```

- `main.py` is in the center, with arrows pointing to each class.
- `main.py` creates instances of `ClassA` and `ClassB` inside the `main()` function.
- `ClassA` has methods like `do_task_a()` and `get_data()`.
- `ClassB` has methods like `do_task_b()` and `process_data()`.
- `ClassA` and `ClassB` do not interact with each other; only `main.py` calls their methods.

---

Now, fill out your own diagram in `project_diagram/diagram.md`!
