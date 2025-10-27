# My Git Mastery Challenge Journey

## Student Information
Name: Thoram Toni Lakshmi Prasanna 
Student ID: 23MH1A4955
Repository: https://github.com/Prasannathoram/git-solved-23MH1A4955.git
Date Started: 27/10/25 
Date Completed: 29/10/25



## Task Summary
Cloned the instructor’s repository containing pre-built merge conflicts and resolved them across multiple branches using proper Git workflows such as fetch, merge, stash, cherry-pick, rebase, revert, and tagging.  
This project strengthened my understanding of collaborative Git operations and version control safety mechanisms.



## Commands Used

| Command | Times Used | Purpose |
|----------|-------------|----------|
| git clone | 1 | Clone instructor’s repository |
| git checkout | 20+ | Switch between branches |
| git branch | 10+ | View / manage branches |
| git merge | 2 | Merge dev and conflict-simulator into main |
| git add | 30+ | Stage resolved conflicts |
| git commit | 15+ | Commit resolved or feature changes |
| git push | 10+ | Push commits to remote repository |
| git fetch | 2 | Fetch updates from instructor |
| git stash | 1 | Temporarily save in-progress work |
| git cherry-pick | 1 | Apply a specific commit from another branch |
| git rebase | 1 | Replay commits onto an updated base branch |
| git reset | 3 | Undo commits (soft, mixed, hard) |
| git revert | 1 | Safely undo a commit |
| git tag | 2 | Create release tags |
| git reflog | 1 | Recover lost commits |
| git status | 50+ | Check repository state |
| git log | 30+ | View commit history |
| git diff | 20+ | Compare changes between commits |



##  Conflicts Resolved

###  Merge 1 — main ← dev (6 files)

#### config/app-config.yaml
- Issue: Production used port 8080, development used port 3000.  
- Resolution: Created unified config file with environment-based variables.  
- Strategy: Default to production, allow override for development.  
- Difficulty: Medium  
- Time: 15 minutes  

####  config/database-config.json
- Issue: Different database hosts and SSL configurations.  
- Resolution: Introduced separate connection profiles for prod/dev.  
- Strategy: JSON restructure to support multi-environment configs.  
- Difficulty: Medium  
- Time: 10 minutes  

####  scripts/deploy.sh
- Issue: Different deployment approaches — one for production servers, another for Docker.  
- Resolution: Combined logic with DEPLOY_ENV condition to detect environment.  
- Strategy: Keep both methods but activate based on environment variable.  
- Difficulty: Hard  
- Time: 20 minutes  

####  scripts/monitor.js
- Issue: Conflicting monitoring intervals and logging formats.  
- Resolution: Unified script with configuration options for both environments.  
- Strategy: Used process.env.NODE_ENV to determine settings.  
- Difficulty: Medium  
- Time: 15 minutes  

####  docs/architecture.md
- Issue: Different system architecture explanations.  
- Resolution: Combined both into one detailed architecture overview.  
- Strategy: Added sub-sections for each environment.  
- Difficulty: Easy  
- Time: 10 minutes  

####  README.md
- Issue: Different feature lists and version details.  
- Resolution: Merged all features into one clear, categorized list.  
- Difficulty: Easy  
- Time: 10 minutes  



###  Merge 2 — main ← conflict-simulator (6 files)

####  scripts/test-runner.js
- Issue: One version used Mocha, another used Jest for testing.  
- Resolution: Reconfigured project to support both test frameworks using separate scripts.  
- Strategy: Modularize test configuration; ensure compatibility for both tools.  
- Difficulty: Hard  
- Time: 25 minutes  

#### config/logger.json
- Issue: Different logging levels (info vs debug) and output formats.  
- Resolution: Created a unified logger with toggleable log level.  
- Strategy: Keep debug in development, info in production.  
- Difficulty: Medium  
- Time: 15 minutes  

####  src/utils/apiHandler.js
- Issue: Conflicting error-handling structures.  
- Resolution: Combined both to ensure uniform error reporting with better clarity.  
- Strategy: Used standard error format and fallback handling.  
- Difficulty: Medium  
- Time: 15 minutes  

####  package.json
- Issue: Conflicting dependency versions.  
- Resolution: Updated dependencies to the latest compatible versions.  
- Strategy: Verified compatibility using npm audit and npm install.  
- Difficulty: Easy  
- Time: 10 minutes  

####  docs/contribution.md
- Issue: Different contribution guidelines (one was minimal, one was detailed).  
- Resolution: Merged both documents keeping detailed version and formatting improvements.  
- Strategy: Organized into “Before Commit”, “During Commit”, “After Push” sections.  
- Difficulty: Easy  
- Time: 10 minutes  

####  .gitignore
- Issue: Missing patterns for node_modules and log files in one version.  
- Resolution: Combined both ignore lists.  
- Strategy: Ensure all build and log files are excluded.  
- Difficulty: Easy  
- Time: 5 minutes  



## Most Challenging Parts
1. **Understanding conflict markers (<<<<<<<, =======, >>>>>>>)** during large merge conflicts.  
2. Choosing between two working versions without breaking functionality.  
3. Handling multi-line script conflicts (especially deploy.sh and test-runner.js).  
4. Recovering lost commits using git reflog after a mistaken hard reset.  
5. Testing all resolved branches to ensure stability before merging.  



## Key Learnings

###  Technical Skills
- Mastered conflict resolution techniques and branch workflows.  
- Learned to recover lost commits using git reflog.  
- Understood the difference between merge, rebase, and cherry-pick.  
- Learned safe undoing with git revert and complete reset using git reset.  

###  Best Practices
- Always read both sides before resolving a conflict.  
- Test all merged code before pushing.  
- Write descriptive commit and merge messages.  
- Use git status and git log frequently to stay aware.  
- Never panic — git reflog can always help recover progress.  

###  Git Workflow Insights
- Merge conflicts are normal in collaborative projects.  
- Communication and documentation are as important as the code itself.  
- Rebasing keeps history clean, while merging keeps it contextual.  
- Cherry-picking allows selective integration of fixes.  
- Tagging releases makes version tracking simple and professional.  



##  Reflection
This challenge completely changed my understanding of Git.  
Before, I only used basic commands like add, commit, and push.  
Now, I can confidently handle complex workflows — merging, rebasing, cherry-picking, and recovering from mistakes.

Git is not just a tool, but a *timeline of collaboration*.  
Conflicts are simply Git asking, “Which direction do you want history to go?”  
I now feel fully equipped to manage version control in any real-world team project.



