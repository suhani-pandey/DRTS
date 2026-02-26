# README

## Folder Contents
This folder contains the following background materials for the "02225 DRTS Mini-project 1 description".

mini-project-1-description.tex is the description of the project; read it first.

Buttazzo--Chapter 4.pdf has the background on the theoretical concepts needed for the mini-project and the schedulability algorithms that have to be implemented.

w2d-simulation.pdf has some suggestions on how to get started with the simulation.

The students have to generate test cases with tasks for their mini project, and the suggestion is to use the one described in task-set-generator-README.md and available at https://github.com/porya-gohary/real-time-task-generators?tab=readme-ov-file. The students may create their own test cases. 

An example task set with its format in CSV is available in task-set-example.csv. PE stands for Processing Element and can be ignored (we consider uni-processor systems, so there's always a single PE). For RM/DM task sets, there will be a priority column (called "Priority") with the task priority.

The students can decide themselves what to aspects to compare for RM and EDF and how. A lot of comparison ideas are available in RM-vs-EDF.pdf. 

## Guidelines

These are the guidelines that the students receive about the mini-projects.

### What is a good project that will get a top grade?

    •    Simulator Tool Development: Build a simulator that can simulate RM and EDF scheduling algorithms and record the response times (e.g., average, worst-case).
    •    Analytical Tool Development: Build a software tool to calculate worst-case response times, WCRTs, for the periodic tasks.
    •    Schedulability Analysis Validation: Compare your analysis results with alternative methods (e.g., manual calculations, other tools, or simulation); identify and explain any discrepancies.
    •    Thorough Results Analysis: Document simulation and analytical findings; interpret them and discuss, highlighting any performance trade-offs.
    •    Comparative Performance Evaluation: Analyze relevant metrics (e.g., WCRTs, missed deadlines); show the impact of chosen scheduling techniques on different types of tasks.
    •    Good Test Cases: Develop multiple realistic system scenarios with varied traffic, workload, or configuration parameters; avoid trivial or overly small examples.
    •    Critical Evaluation: Discuss the strengths and limitations of your chosen scheduling approach in these scenarios; suggest improvements or further research directions.
    •    Effective Teamwork: Show clear division of tasks and cohesive collaboration within your group; integrate individual contributions seamlessly in the final deliverables.
    •    Well-Written Report: Organize the report with clear sections; use concise, precise technical language; properly cite all references.

### Note on the use of Generative AI (GenAI)

Students are encouraged to use GenAI models like ChatGPT, Gemini or Claude for brainstorming, code generation, and problem-solving. Always follow DTU’s academic integrity guidelines and verify AI-generated information for accuracy. 

### Project report: structure, format, hand-in

You can adapt the suggested structure below as you see fit, but please be concise.

◦    Introduction & Theory: Clearly state project goals and the scheduling model. Provide only essential theoretical notations. Mention simplifications or assumptions you made.
◦    Implementation:
    ▪    Tool Development: Summarize the software tool’s purpose.
    ▪    Pseudocode: Include key steps of your algorithm.
    ▪    Technical Details: Note libraries and configurations.
◦    Testing & Validation:
    ▪    Describe test cases and validation process (e.g., comparing analysis results with simulation outputs).
◦    Evaluation & Discussion:
    ▪    Present results, analyze scheduling performance, discuss any trade-offs and limitations.

Submission Details:
    ▪    Hand in a PDF report along with a compressed archive (ZIP) containing:
    ▪    Code: All source files and scripts.
    ▪    Results: Relevant output data or logs.
    ▪    README: Instructions for running your tool and explaining the contents of the archive.