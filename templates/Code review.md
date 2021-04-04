# Code Review Check-list

## Scope 

* [ ] Story is high priority
* [ ] Story is small
* [ ] Story minimize creep
* [ ] No stray changes
* [ ] Off-task changes added to backlog

## Works correctly

* [ ] Specification is correct and complete
* [ ] Implementation follows specification
* [ ] Testing plan created
* [ ] Unit tests created and/or updated
* [ ] Master merged into branch
* [ ] All changes tested
* [ ] Edge cases covered
* [ ] Cannot find a way to break code
* [ ] Cannot find any ways these changes break some other part of the system
* [ ] All tasks 'done'
* [ ] ZERO KNOWN DEFECTS

## Defensiveness

* [ ] All inputs to public methods validated
* [ ] Fails loudly if used incorrectly
* [ ] All return codes checked
* [ ] Security
* [ ] We cleaned up all the temporary resources created
* [ ] Input files are archived

## Easy to read and understand

* [ ] Appropriate abstraction and problem decomposition
* [ ] Minimum interface exposed
* [ ] Information hiding
* [ ] Command-query principle
* [ ] Good naming
* [ ] Meaningful documentation and comments
* [ ] Fully refactored (use judgement with existing code)

## Style and layout

* [ ] All inspections pass
* [ ] Code formatter run
* [ ] No smelly code styling
* [ ] Line length, styling consistent with project guidelines

## Final considerations

* [ ] YOU FULLY UNDERSTAND THE CODE AND THE IMPACT OF THE CHANGES YOU HAVE MADE AND IT... is unbreakable, is actually done, will pass code review, would make you proud to present your changes to other programmers in public, is easy to review, correct branch, no stray code, schema changes documented, master merged into branch, unit tests pass, manual testing plan complete and executed, all changes committed and pushed, pull request created and reviewed, Jira updated