# Review
## Query Suggestion for Mobile Search: Understanding Usage Patterns

### INTRODUCTION
Typing text on a standard 9-key cell phone is difficult and time consuming.
To address these inefficiencies, a variety of text prediction techniques have been proposed.
In this paper, we study usage patterns of a query suggestion system.
Our primary goal is to build a usage model of query suggestion in order to provide UI guidlines for mobile text prediction interfaces.
- We show that users accept the correct suggestion by the third time it is shown.
- Surprisingly, users will often accept suggestions even if the process of doing so results in an increase in the number of total key presses.

### EXPERIMENTS
- entering 23 queries on a mobile phone
- asked a series of questions (NASA-Task Load Index)

#### Interface Variants Tested
The six interfaces differed only in the number of suggestions displayed as the user was typing the query.
The number of suggestions ranged from zero to a maximum of five suggestions (the maximum number of suggestions that fit on the screen without requrining the user to scroll).

#### Users & Datasets
- Users : 30
- partial completions : where the suggestion completes part of the desired query
- super completions : where the suggestion is a superset of the desired query
- full completions :  where the suggestion is the desired query

### FINDINGS
Users who were asked to enter queries on a search interface with query suggestions rated their workload lower, their enjoyment higher and saved nearly half of the key pressed than the users who were not shown suggestions.
Surprisingly, time to enter a query was not reduced with the decreased number of key presses.
- this trend indicates that the presence of query suggestions may slow the number of key presses/second.

#### Users rely heavily on query suggestions
100% of the users who were shown suggestions accepted at least one suggestion; the average number of accepted suggestion per query was 0.9.
The number of suggestions shown to the user did not impact the high acceptance rate.

#### Users often ignore the cost of accepting a suggestion
users did not make that cost-benifit analysis when considering whether to accept a listed suggestion.
Of suggestions that were presented to the user when the number of key press left to type was less than the number of down and enter key presses required to select the suggestion, 50% were accepted.

#### Users will accept a correct suggestion quickly
If a user has not accepted a suggestion after it is shown three items it can be taken as a strong signal that the suggestion is not the user's intended query.
Showing more suggestions may hinder the efficient usage of suggestion.
Users who are shown fewer suggestions are likely to accept a suggestion earlier, perhaps because with fewer suggestions it is easier to identify a correct suggestion.
Anoterh factor which impacts how quickly a user will accept the suggestions is the movement of the suggestions in the list.

### CONCLUSION AND FUTURE WORK
- It will be interesting to determine the effects of different search mediums: do users with miniature QWERTY keyboards rely on suggestions less frequently, and how does it compare to conventional computers? 
