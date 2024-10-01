# COMP6991 Rust Logo Interpreter Assignment

**Logo Language Overview**
- Logo is a programming language derived from Lisp and others.
- Older programmers often had their first programming experience with Logo.
- Key feature is a "turtle" for drawing by picking up and putting down a pen and moving around.

**Assignment Goals**
- Practice designing and structuring a larger Rust program.
- Focus on modern programming skills and design patterns.
- Have fun creating an aesthetic and interesting application while connecting with programming history.

**Assignment Requirements**
- Build a Logo interpreter that writes to an.svg or.png image using the `unsvg` crate.
- Handle various Logo commands for turtle control, variables, queries, conditionals, and math operations.
- Implement design excellence features for full marks.

## 1. Introduction to the Logo Language
### Tokens
- A token can be a procedure (like a function), a variable (prefixed by `:`), or a value (prefixed by `"`).
- Procedures always take a fixed number of arguments.
- Values in Logo are always strings, but some like `"TRUE"` and `"FALSE"` are interpreted as booleans and some can be parsed as numbers.

### Program Structure
- A logo program consists of lines of text split into tokens by whitespace.
- Lines starting with `//` or empty lines are ignored as comments.

## 2. Introduction to Unsvg
- The assignment uses the `unsvg` crate to generate SVG or PNG images.
- `unsvg::Image` represents an image and has methods like `draw_simple_line`.
- `unsvg::get_end_coordinates` returns where a line drawn from a given point would end.

## 3. How Your Program Will Work
- Produce a program called `rslogo` that takes four arguments: a logo program file (.lg), the output SVG/PNG file path (.svg or.png), image height, and image width.
- Read the logo program, parse and execute it line by line.
- Exit with a non-zero return code and print an error message if there's an issue.
- Write an SVG or PNG using the `unsvg` crate if there are no issues.

## 4. Design Excellence
- Options for design excellence include making beautiful errors, achieving 80% test coverage, using a parser combinator library, creating a facility for language extensions, building a zero-copy program, contributing to the `unsvg` library, or building a transpiler.
- Markers will consider a reasonable attempt at one of these tasks as sufficient.

## 5. The Tasks To Complete
### Part 1: Turtle Control (20%)
- Control the "turtle" which is like an invisible pen that can draw on the image.
- Turtle starts "up" (not drawing) in the center of the screen facing straight up.
- Commands include `PENUP`, `PENDOWN`, `FORWARD`, `BACK`, `LEFT`, `RIGHT`, `SETPENCOLOR`, `TURN`, `SETHEADING`, `SETX`, `SETY`.
- Turtle can go off the image without causing an error.

### Part 2: Variables and Queries (20%)
- Implement the `MAKE` command to create and assign variables.
- Implement the `ADDASSIGN` command for variable increment.
- Support "queries" like `XCOR`, `YCOR`, `HEADING`, `COLOR`.

### Part 3: IFs, WHILE, [ ] (20%)
- Implement `IF EQ` and `WHILE EQ` commands for conditional execution and looping.

### Part 4: Implementing Maths and Comparisons using a Stack (20%)
- Implement operations in Polish Notation like `EQ`, `NE`, `GT`, `LT`, `AND`, `OR`, `+`, `-`, `*`, `/`.
- Implement stack operations for `IF` and `WHILE`.

### Part 5: Logo Defined Procedures (20%)
- Implement procedures analogous to functions in other languages.
- Procedures are defined with a line starting with `TO`, followed by the procedure name and arguments, and ending with `END`.

## 6. Common Questions
### Design Approaches
- Line-by-line approach: Execute each line in turn while storing more data and state.
- Parse then execute approach: Convert the text into an Abstract Syntax Tree and read from it.

### Planning
- A happy middle is suggested: think about the approach and read through the assignment without spending more than 30 minutes planning.

### Using AI
- Permitted uses of AI include seeking help with concepts, pattern matching, generating skeletons, and writing tests.

## 7. Other Information
### Submission
- See instructions at the bottom of the page.

### Using Other Crates
- Can use crates from crates.io under certain conditions.

### Marking Scheme
- Marked on Mechanical Style (10%), Functional Correctness (40%), and Idiomatic Design (50%).

## 8. Formal Stuff
- Assignment is individual.
- No joint work or sharing of code allowed.
- Use of code-synthesis tools is permitted but with caution.
- Submit work by running `6991 give-crate` by Week 7 Wednesday 17:00:00.
# COMP6991 RSLogo 24T3

# CS Tutor | 计算机编程辅导 | Code Help | Programming Help

# WeChat: cstutorcs

# Email: tutorcs@163.com

# QQ: 749389476

# 非中介, 直接联系程序员本人
