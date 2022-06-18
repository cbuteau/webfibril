
# States

A state digram for the main page.
This is where experimentaion takes place until plantuml is in github

## Diagram

```plantuml
[*] --> STARTING
STARTING --> STARTED : SCRIPTLOADED
STARTING : Here we instantiate the Worker() object.

STARTED --> INITIALIZED : BASEINIT_COMPLETE
STARTED : We get a message back that the basethread script properly loaded.

INITIALIZED : This is where we load requirejs.
INITIALIZED : TODO Load any loading subsystem.

STARTED --> COMPLETED : BASEINIT_ERROR


INITIALIZED --> DISPATCH : DISPATCH

DISPATCH : This is where the execution
DISPATCH :  of the sided script occurs.

DISPATCH --> COMPLETED : DISPATCH_COMPLETE
DISPATCH --> COMPLETED : DISPATCH_ERROR
COMPLETED --> STARTED

STARTING --> COMPLETED : Exception

```
