# SCD-Project
Simple Chat / Messaging Simulator

PROJECT DESCRIPTION
This project is a proof-of-concept Desktop application built using Java Swing that simulates a basic, asynchronous messaging environment. The core goal is to showcase the effective integration of several Design Patterns to manage the application's functionality. The simulator allows a user (Student_User) to send text and system messages and includes a background thread that simulates messages incoming from a TeacherBot.
The architecture leverages five main design patterns:
Singleton Pattern (Creational): The ChatEngine is implemented as a Singleton to ensure only one, centralized instance exists. This instance is responsible for managing all Chat Logs and handling Message Routing (notifying observers).
Message Factory Pattern (Creational): The MessageFactory is used to create specific message objects (e.g., TextMessage or SystemMessage) based on a string input, abstracting the creation logic away from the main application flow.
ChatSession Builder Pattern (Creational): The ChatSessionBuilder provides a flexible and clear way to construct and configure the user's session parameters, such as the username and theme.
Decorator Pattern (Structural): The TimestampDecorator wraps a base message object to dynamically add features, specifically a timestamp, without altering the core message structure.
Observer Pattern (Behavioral): The ChatEngine acts as the Subject, notifying its Observer, the Chat_Simulator (the main GUI class), every time a new message is sent. This effectively decouples the data/engine logic from the UI rendering, enabling live updates.

HOW TO RUN THE SYSTEM
The application is a standard Java program that can be compiled and executed via the command line.
Save the Code: Save the provided Java code block into a file named Chat_Simulator.java.
Compile the File: Open your terminal or Command Prompt, navigate to the directory where you saved your file, and execute the Java compiler command:
      javac Chat_Simulator.java
Execute the Application: Run the compiled class file using the Java runtime:
      java Chat_Simulator
A desktop GUI window will open, launching the application. The system will automatically start a background thread (the simulated "TeacherBot") to send messages, demonstrating the live update functionality.

DEPENDENCIES
This project is fully self-contained, meaning it needs no external libraries or complex downloads. The application is constructed entirely using the tools found within the Standard Java Development Kit (JDK).
A JDK 8 or a newer version must be available on the system for execution.
The core application logic relies on these built-in Java packages:
javax.swing: The primary package used to build and display the entire Graphical User Interface (GUI). This handles all visible components like the chat window, the input box, and the buttons.
java.awt: Provides fundamental support for the GUI's look and feel, including managing layouts, defining colors (for different message types), and controlling the basic event system.
java.util: Used for all essential backend work, such as managing data structures (like the lists holding messages) and handling concurrency (running the background simulation thread).

FOLDER STRUCTURE
The structure of this project is as simple as possible, as the entire chat application is contained within one single Java source file.
There are no complex directories, subfolders, or external asset folders required to run the application.

Project Layout
The system exists entirely in the project's root directory:
Project Root: This is the top-level folder where the work is stored.
Chat_Simulator.java: This is the single file containing all the code (classes, logic, and GUI) necessary for the entire system to compile and run.
