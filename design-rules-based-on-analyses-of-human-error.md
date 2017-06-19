# Review
## Design Rules Based on Analyses of Human Error

### INTRODUCTION
Errors, however, can be serious, both in the sense that they can lead to serious mishap, and in the social sense that they frustrate beginning users.
This paper addresses the developmenet of design rules that can lead to improvements in this situation.

### SYSTEM DESIGN PRINCIPLES CAN BE DERIVED FROM THE CLASSES OF HUMAN ERROR
- Call the highest level specification of a desired action an intention.
- An error in the intention is called a mistake.
- An error in carrying out the intention is called a slip.

### MODE ERRORS SUGGEST THE NEED FOR BETTER FEEDBACK
A large class of errors is the mode error: doing the operation appropriate for one mode when in fact you are in another.
Mode errors occur when the person believes the system is in one state (mode), when it is actually in another.
Many mode errors occur in text editors, with confusions between "insert" mode and "command" mode.
In any event, there are obvious ways to minimize mode errors.
- Do not have modes.
- Make sure that the modes are distinctively marked.
- Make the commands required by different modes different, so that a command in the wrong mode will not lead to difficulty.

* Mode errors : Erroneous classification of the situation
* Description errors : Ambiguous or incomplete specification of the intention

### DESCRIPTION ERRORS SUGGEST THE NEED FOR BETTER SYSTEM CONFIGURATION
A description error occurs when there is insufficient specification of an action and the resultant ambiguity leads to an erroneous act.
One class of description errors occurs in the use of computer text editors which have multiple commands, usually based upon one or two keystrokes.
Solutions to this problem have long been known:
1. Screen displays and menu systems should be organized functionally.
2. Design the command language or menu display headings to be distinct from one another so as not to be easily confused, either in perception or in the action required.
3. Make it difficult to do actions that can lead to operations with serious implications and that are not reversible.

### LACK OF CONSISTENCY LEADS TO ERRORS
The appropriate sturcture for one command is not the same for another, even though the commands appear to be related and share a common description of purpose, action, and even part of the command format.
The basic concept involved here is that when people lack knowledge about the proper operation of some aspect of a machine, they are apt to derive the operation by analogy with other, simliar ascpects of the device
It can lead to error if the mapping from one domain onto the other is not consistent.
- One solution is to make command structure and instrument format consistent, even at the cost of som inefficiency of usage.
- A better solution would be to redesign the entire system to yield both consistency and ease of operation.

### CAPTURE ERRORS IMPLY THE NEED TO AVOID OVERLAPPING COMMAND SEQUENCES
A capture error occurs when there is overlap in the sequence requried for the performance of two different actions, especially when one is done considerably more frequently than the other.
- One possible way of avoiding this class of error is to minimize overlapping sequences, but this may not be possible, especially when the infrequent action sequence is simply a modification of the frequent one.
- A second way of avoiding the error is to try to catch it where it occurs. The error occurs at the critical place where the sequences deviate, so it is here that the problem must be faced.

### ACTIVATION ISSUES SUGGEST THE IMPORTANCE OF MEMORY REMINDERS
Activation errors are of two classes: inappropriate actions get performed and appropriate actions fail to get done.
In many ways the old saying, out of sight, out of mind is apt;

### PEOPLE WILL MAKE ERRORS, SO MAKE THE SYSTEM INSENSITIVE TO THEM
People will make errors even in the best designed systems, even with the best of training and motiviations.
So, a corollary of the attempt to minimize errors is that one should try to minimize the effect of an error.
It is not sufficient to ask the user to confirm that a particular action sequence is wanted, because if confirmation is routinely asked for, the confirmation itself becomes an automatically invoked component of the command sequence.

### LESSONS
- Feedback
    - The state of the system should be clearly available to the user, ideally in a form that is unambiguous and that makes the set of options readily available so as to avoid mode errors.
- Similarity of response sequences
    - Different classes of actions should have quite dissimilar command sequences so as to avoid capture and descrpition errors.
- Actions should be reversible
    - and where both irreversible and of relatively high consequence, they should be difficult to do, thereby preventing unintentional performance.
- Consistency of the system
    - The system should be consistent in its structure and design of command so as to minimize memory problems in retrieving the operations.
