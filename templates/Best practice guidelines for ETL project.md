# Best practice guidelines for ETL project

Some concepts to keep in mind all the time :
* Readability: create code that can be quickly analyzed and understood.
* A concise writing: quickly and well: create quickly, a simple code in a minimum of time.
* Maintainability: reduce complexity to a minimum in order to have an equally minimal impact during changes.
* Accuracy: create a code that precisely meets the need.
* Reusability: create shareable objects and atomic tasks that are reusable.
* Respect for the rules: set up a real discipline between the teams, the projects, the "repositories", and the code. In other words, impose and respect rules of work, naming, and writing.
* Robustness: create code that bends but does not break. In other words, which reacts well when deviating from normal conditions of use.
* Extensibility: create elastic modules that can adapt to demand.
* Consistency: create basic things above all.
* Efficiency: achieve optimal data flows and components.
* Partitioning: create atomic, targeted modules that meet a single need. Avoid Swiss Army Knives!
* Optimization: achieve as many features as possible with as little code as possible.
* Performance: create efficient modules that provide the fastest flow rates.

In all cases, we must have the following elements :
* Have the use case - a well-defined business data/work flow requirement
* Have the technology - the tools with which we craft, deploy, and run the solution
* Have the methodology - a given way to do things that everyone agrees with

## The methods

Must detail HOW you want to build your universe.

### Data modeling

* Holistic / Conceptual / logical / physical
* Database, NoSQL, EDW, Files

### Mastery of the SDLC Process

* V cycle or Agile / Scrum
* Specifications

### Error handling & Supervision

### Governance & Data Architect

## Technologies 

Must list the TOOLS (internal and external) and how they interact.

### OS & Infrastructure topology

### Database Management Systems

### NoSQL systems

### Encryption & Compression

### Integration of third-party software

### Interfaces with Web Services

### Interfaces with external systems

## Good practices 

Should describe WHAT & WHEN certain recommendations should be applied.

### Environments (DEV / QA / ITG / PROD)

### Naming conventions

### Projects, Jobs & Joblets

### Objects in the Repository

### Logging, Monitoring & Notifications

### Job return codes

### Code (Java) Routines

### Context groups & Global variables

### Databases & NoSQL Connections

### Data Sources & Targets & File Schemes

### Entry of Jobs & Exit Points

### Jobs & schemas workflow

### Component use cases

### Parallelization

### Data quality

### Jobs Parents / Son & Joblets

### Data exchange protocols

### Continuous Integration & Deployment

#### Integrated source code management (SVN / GIT)

#### Delivery management & versioning

#### Automated tests

#### Artifact Repository & Promotion

### Administration & Operations

#### Configuration

#### Security & Authorizations

#### Roles & Permissions

#### Project management

#### Batch of jobs, planning, & sequences

### Backups & Disaster Recovery

## Other elements

### Modules libraries

Describing all reusable elements :
* projects
* methods
* objects
* joblets
* context groups

### Data dictionaries

Describing all data schemas & associated stored procedures.

### Data access layers

Describing everything relevant to connecting and manipulating data.

## Some tips

* Define object naming convention (and respect this convention)
* Define organization of Workflow & Disposition
* Use and abuse of context groups, metadata and documentation
* Use atomic jobs ~ Parent / Son jobs
* Choose between tRunJob and Joblets
* Use entry and exit points
* Error handling & Logging
* Choose between the OnSubJobOK / ERROR and OnComponentOK / ERROR (& Run If) links
* Don't forget about memory management
* Dynamic SQL Syntax for complex queries
* Don't forget about parallelization (for huge process)
* Use code routines
* Don't forget about log4j in project settings
* Don't forget about activity monitoring (stats, logs & flow)
* Consider setting up recovery checkpoints in critical treatments

## Some tricks

* Do Use Both The tPreJob & tPostJob Components
* Do Not Clutter Canvas With Tightly Grouped Components; Spread it out a bit
* Do Layout Your Code Nicely; Top-2-Bottom & Left-2-Right
* Do Not Expect To Get It Just Right The 1st Time You Code It
* Do Identify Your Main Job Loop & Control Your Exit
* Do Not Ignore Error Handling Techniques
* Do Use Context Groups Extensively (DEV/QA/UAT/PROD) & Wisely
* Do Not Create Massive Single Job Layouts
* Do Create Atomic Job Modules
* Do Not Force Complexity; Simplify
* Do Use Generic Schemas Everywhere (arguable exception is the single column schema)
* Do Not Forget To Name Your Objects
* Do Use Joblets Where Appropriate (there may only be a few)
* Do Not Over utilize The tJavaFlex Component; tJava or tJavaRow is likely enough
* Do Generate/Publish The Project Documentation When Done
* Do Not Skip Setting The Runtime Memory Heap