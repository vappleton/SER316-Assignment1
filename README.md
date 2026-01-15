## Initial  branch structure##

The main branch contains the initial version of the game, while additional functionality is added in feature branches (feature1, feature2, feature3) and integrated through a dev branch. 

## Branch structure##

 - **main**
  Initial implementation of the number guessing game.

 - **feature1**
  Adds the ability to quit the game using a negative number
  Improves user feedback messages and allows replaying the game.

 - **feature2**
 Implements a maximum number of attemps 
 Adds game over logic

 - **feature3** 
 Implemets a hint feature when the player is close to guessing the number.

 - **hotfix**
 Fixes an issue when the random number generator doesnt include the maximum value. 

 ## Differences between merge, rebase, squash, and cherry-pick##
 Merge combines one branch into another by creating a merge commit. It keeps the history of both branches.
 
 Rebasing moves a branch so that its commits are replayed on top of anotehr branch, which creates a linear history and it's easier to read and understand.

 Squash combines multiple commits into a single commit. We use this bfore merging a feature branch so the final history shows one clean commit instead of messy ones. 

 Cherry-pick copies a specific commit from one branch and applies it to another branch. It's useful when we only want one fix  without merging the entire branch. 

 ## What you observed in the git history for feature1 vs feature2 vs feature3 ##
 When reviewing the Git history, I noticed a few differences between feature1, feature2, and feature3. The feature1 branch contained several smaller commits that show the step-by-step development of the quit functionality, replay logic, and improved user feedback. This made the history detailed but a bit cluttered. The feature2 branch included commits related to implementing the maximum attempts limit and game-over behavior, and it required resolving conflicts after syncing with dev, which resulted in a merge commit when it was integrated. In contrast, feature3 originally had multiple development commits, but these were squashed into a single commit titled “Add hint system to show proximity after 3 attempts”, making its history much cleaner and easier to read when added to dev. Overall, feature3 resulted in the most readable history, while feature1 and feature2 preserved more detailed development steps. 

 ## When you would use each strategy in real projects##

 In real projects, I would use merge when I want to preserve the full history of how the branches are combined, espcieally in small projects where it is essential to know where and how the work was integrated. 
 I would use rebase when working on my own feature branch to keep the hisory clean and linear before merging it into a shared branch like dev.
 Squash is useful when a feature branch has many small or messy commits and I want to combine them into one clear and meaningful commit before adding it to the main development branch. 
 Lastly, I would use cherry-pick when I need to apply a specific commit such as a hotfix to another branch without merging all the changes from that branch. 