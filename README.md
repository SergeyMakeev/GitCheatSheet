# GitCheatSheet

# Configure Fork after Clone (setup upstream)

1. Open Git Console/Bash
2. List the current configured remote repositories for your fork  
`git remote -v`
3. Specify a new remote upstream repository that will be synced with the fork  
`git remote add upstream https://full_path_to_repo/repo.git`
4. Verify the new upstream repository you've specified for your fork  
`git remote -v`
Every url should listed twice (fetch and push)


# Sync your fork with upstream

1. Fetch original master `Upstream/Master`
2. Checkout your fork local master `Local/Master`
3. Merge `Upstream/Master` to `Local/Master` (Fast Forward)
4. Push `Local/Master` to `Origin/Master`  (This will update remote master in your fork)

# Merge

1. Checkout your local Feature branch `Local/Feature`
2. Merge `Local/Master` to your Feature branch
3. Resolve conflicts
4. Build
5. Push `Local/Feature` to `Origin/Feature`


# Diff a feature branch with your form master branch (rebase alternative)
1. Open Git Console/Bash
2. Create patchfile  
`git diff master...Feature-Branch > diff.patch`
3. Create a new branch from master (Feature-Clean) and apply your patch to the new branch  
`git apply diff.patch`

# GitHub UI Hints & Tricks

1. Add .patch postix to PR to get a diff file  
e.g., `https://github.com/repo/pull/123` -> `https://github.com/repo/pull/123.patch`
