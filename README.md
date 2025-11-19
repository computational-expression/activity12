
# Activity 12: Project UML Diagram

For this activity, you will develop a simple UML diagram in markdown to show how your classes will connect for your final project assignment.

## Instructions

1. Think about the main classes in your project and how they interact.
2. Draw a simple UML diagram in markdown to show:
   - The classes you plan to create
   - How they connect (if at all)
   - How `main.py` orchestrates the application
3. Use the template in `project_diagram/diagram.md` to sketch your project structure.

## Example 1: Two Connected Classes

```markdown
+----------------+        uses        +----------------+
|   Main.py      |------------------>|   ClassA       |
|----------------|                   |----------------|
| run_app()      |                   | do_task_a()    |
+----------------+                   | get_data()     |
      |                           +----------------+
      v                                   v
+----------------+ <--------uses----- +----------------+
|   ClassB       |-------------------|   ClassA       |
|----------------|                   |----------------|
| do_task_b()    |                   | do_task_a()    |
| process_data() |                   | get_data()     |
+----------------+                   +----------------+
```

- `Main.py` creates instances of `ClassA` and `ClassB` and calls `run_app()`.
- `ClassA` has functions like `do_task_a()` and `get_data()`.
- `ClassB` uses or interacts with `ClassA` (e.g., calls its methods or stores a reference) and has functions like `do_task_b()` and `process_data()`.

## Example 2: Two Unconnected Classes

```markdown
+----------------+
|   Main.py      |
|----------------|
| run_app()      |
+----------------+
      |      |
      v      v
+-------------------+   +-------------------+
|  ClassA           |   |  ClassB           |
|-------------------|   |-------------------|
| do_task_a()       |   | do_task_b()       |
| get_data()        |   | process_data()    |
+-------------------+   +-------------------+
```

- `Main.py` creates instances of `ClassA` and `ClassB` and calls `run_app()`.
- `ClassA` and `ClassB` each have their own functions (e.g., `do_task_a()`, `get_data()`, `do_task_b()`, `process_data()`).
- `ClassA` and `ClassB` do not interact with each other; only `main.py` calls their methods.

---

Now, fill out your own diagram in `project_diagram/diagram.md`!
