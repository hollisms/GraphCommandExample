# GraphCommandExample

Adds an implementation for a GraphCommand that is stylized after wpilib SequentialCommand, ParallelCommand, etc.

It is intended to be used as a the default command for a subsystem that implemented a state machine.

When the state machines transitions across as link (pathway or connection) between two nodes it executes the Target Command if the node is the final transition or the Waypoint Command if the node is NOT the final transition.  The intention is that some optimizations may be performed in the Waypoint command vs. Target Command.  For example, the "goal tolerance" could be increased on Way Points.  Once the Target Node is reached the Arrived Command is run.

