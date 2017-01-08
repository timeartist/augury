##Design Guide / Contribution Requirements
- Every branch is a deployable starting point.  It must be runnable and include any prerequisite code from other sections.  
 - This allows participants to work on the parts of the tutorial that they're interested in and skip the ones that they're not.
- Every branch must include a complete set of unit tests that can be run simply with `single command tbd`.  
 - These tests should not work when the branch is first checked out and pass once the participant completes the requirements.
 - This allows participants to check their work, as well as provide a starting point for figuring out the problem being solved in the section
- Each branch should break its tasks into issues in the repo.
 - In the master branch, relevant code should be tagged to the task.
 - This allows participants to simply review how to implement a given idea without needing to actually do so themselves.
 - Each branch should change it's README to explain the task at hand, referencing those tasks.
