labview-goblin-library
=========================

LabView Goblin library helps to organise experimental parameters for each experiment. It reads and writes parameters into a human readable file (JSON) that can be copied between experiments.

Trivia: goblins are good at keeping books. HP. 

## Format

Use JSON format as it is widely available. There is a [library for LabView](https://code.google.com/p/i3-labview/downloads/list)

## Functions

### Initialisations 

    GoblinInitialise (in: experiment folder): Goblin object
      	
      	look for "experiment.json": if not there create
      	load all values to the object
      	create local variables with all the names

### Get

    GoblinGet (in: Goblin object, property name): int, float or a string

### Add

Adds a variable to the Goblin books. 

    GoblinAdd (in: Goblin object,  name, value): Goblin object

### Remove 

    GoblinRemove (in: Goblin object,  name): Goblin object

### Save

    GoblinSave (in: Goblin object)

    	Save values into file. Keep values that were not in this Goblin.

### Load

    GoblinLoad (in: Goblin object)
