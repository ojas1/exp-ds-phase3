# exp-ds-phase3
Converting data structure experiments to phase 3 structure.  This is a sample repository.

## Experiment Descriptor
The Experiment Descriptor contains information about the structure of the repository and how to build the experiment.  The descriptor (if present) lists all the learning units and tasks included in the experiment along with their placement in the experiment, sources used to build the units and pages to be generated for the same.

### Structure of the Experiment Descriptor
The experiment descriptor is a json document that contains a list of **units**.  Each unit describes a part of the experiment and depending on the unit type, it may contains other units.

## Unit

A Experiment is divided into several **units**.  Each unit is defined by record in the experiment descriptor that contains the following information:

1. Unit Type
2. Label
3. Content Type
4. Source
5. Target
6. Basedir
7. Units

### Unit Type

Types of Units: *Learning Unit*, *Task*
Record in Experiment Descriptor: "unit-type"
Values: "lu", "task"

### Label

The label field is used for the navigation menu.

### Content Type

| Content Type | Descriptor Value | Criteria                                        | Appilcable to |
|--------------|------------------|-------------------------------------------------|---------------|
| Text         | text             | only text                                       | lu, task      |
| Video        | video            | Text (optinal) and Video                        | lu, task      |
| Simulation   | simulation       | Text (optional), Simulation and Video (optinal) | task          |
| Assesment    | assesment        | Quiz.                                           | task          |

### Basedir

The directory that contains all the content for the learning unit.

### Source

Path of the source file (md, js or html), relative to the basedir.

### Target

Path of the target html file, relative to the basedir.

### Units

List of tasks within the learning unit.