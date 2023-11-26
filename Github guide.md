# Git guide

Using YT video https://www.youtube.com/watch?v=tRZGeaHPoaw&ab_channel=KevinStratvert

## Background

Git is open source and free SCM (source control management).

Once Git is installed, any terminal program can be used such as GitBash (recommended).

## Configuration

Initial configuration screen. The last line is a help request that will list all commands.

![](./images/gitbash_config_screen.jpg)

Useful GitBash commands –

- Help, followed by command name will show help on that command.
- Clear, will clear the screen.

## Example procedure

NOTE: Gitbash used as terminal.

### Finding the files locally and setting a repository

This shows the local location of the files in the worked youtube example.

![](./images/location_of_local_git_files.jpg)

This is how to set that folder as a repository.

![](./images/setting_repository_location.jpg)

### Hidden files

![](./images/showing_hidden_items_in_the_folder.jpg)

Showing hidden files (above) reveals that Git has placed additional hidden files in the repository folder (below).

![](./images/hidden_git_folder.jpg)

### Git status and tracking

Git status shows the status of the repository, currently on the main branch. All files are currently untracked so show in red.

The Git folder tree is highlighted.

![](./images/git_status.jpg)

The git add command for index.htm will set git to track index.htm.

![](./images/tracking_a_file.jpg)

Git status now shows that the index.htm file is tracked (in green).

![](./images/one_file_tracked.jpg)

The rm command will remove (untrack) a file that is tracked. In this case index.htm.

![](./images/untracking_a_file.jpg)

### Ignoring a file

To set a file to be completely ignored by Git (it may for example be confidential), create a new .TXT file in the folder.

![](./images/creating_git_ignore_file.jpg)

Re-title the file to .gitignore

![](./images/re_title_git_ignore.jpg)

Open the file in Notepad etc.

![](./images/open_ignore_file.jpg)

Complete the ignore list using this syntax and save the file.

![](./images/ignore_file.jpg)

Checking status reveals the ignore file, but not the file that is ignored.

![](./images/ignore_status.jpg)


### Tracking all files

Now that the salary file in the example is ignored, set all remaining files to be tracked and show status. Commands git add --all, git add -A or git add . (for the whole folder) will work.

![](./images/tracking_a_file.jpg)

## Committing

### Committing files

This command will commit all files to the repository.

![](./images/commit_files.jpg)

This is the result of that commit.

![](./images/commit_result.jpg)

### Updating one of the files (index.htm)

Open index.htm, make a change and save it.

![](./images/update_file.jpg)

Checking status after the change.

![](./images/file_changed.jpg)

The git diff command will show the differences between the file that was changed.

![](./images/git_diff.jpg)

### Staging status

The git add command will now move the changed file to staging status from working. Staging is a holding place.

![](./images/change_to_staging.jpg)

Files within git will exist in one three status options. working files, staging, or committed.

![](./images/file_status_options.jpg)

Use the command git restore --staged index.htm to return this file to working status.

![](./images/staged_to_working.jpg)

### Committing all files

This command will commit all files, bypassing staging.

![](./images/commit_all.jpg)

### Renaming files

Command git mv "old name" "new name" will rename a file.

![](./images/rename_file.jpg)

### Add a note to a commit

Use commit -m "note" to add a note when committing.

![](./images/add_note_to_commit.jpg)

### Log of all commits

The git log command will list the history of all commits.

![](./images/commit_log.jpg)

Or use git log --oneline to show an abbreviated version.

![](./images/commit_log_brief.jpg)

The command git log -p will display more detail of each previous commit.

![](./images/commit_details.jpg)

NOTE: Git help log will list all log command options. 

### Stepping back through previous commands

Use the up arrow to step back through commands.

![](./images/step_back.jpg)

To exit this view press Q.

![](./images/exit_commit_view.jpg)

### Undo a commit

The command git reset c193894 (this example) will undo a specific commit.

![](./images/undo_commit.jpg)

### Rebasing

It's possible to modify the order in which the commits appear with the rebase command.

![](./images/rebase.jpg)

The result shows the options. Fairly advanced.

![](./images/rebase_options.jpg)

## Branching

### Creating another branch

The command git branch will set up another branch. The branch can be named as shown.

![](./images/new_branch.jpg)

### Viewing active branch status

To view all branches in the repository, just use the git branch command. All branches will be displayed with the active branch asterisked.

![](./images/branch_display.jpg)

### Switching branches
 
To switch to another branch use the git switch command followed by the name of the branch.

<img src="images/switch_branch.jpg" style= "width: 1000px"/> 

![](./images/switch_branch.jpg)

### Creating another branch and switching to it

It is also possible to create a branch and switch to it using the git switch -c command.

![](./images/create_switch_branch.jpg)

The new branch will be created and switched to. Use the git branch command to check status.

### Editing within a branch

In this example, having switched to the 'FixTemp' branch, all files displayed will now be in that branch. View the files in Explorer and open the file to edit.

![](./images/editing_in_branch.jpg)

Now checking status after editing. The modified file is highlighted red.

<img src="images/check_status_after_branch_edit.jpg" style= "width: 1000px"/>

![](./images/check_status_after_branch_edit.jpg)

### Committing a change within a branch

As before, to commit the change use the command git commit (in this case suffixed -a, -m, then with a note added for this commit).

![](./images/commit_branch_edit.jpg)

### Changing branches

To change branches, in this case switching back to the main branch, use the git switch command followed by the branch name.

![](./images/git_switch.jpg)

Note that the files in the main branch (now displayed) are not changed.

### Merging changes to branches

To merge the changes from the Fixtemp branch in the example back to the main branch, use the git merge command. The command includes a note, then the name of the branch.

![](./images/git_merge.jpg)

### Deleting a branch

Once changes have been merged, in this example to the main branch, the branch can be deleted with git branch -d, then the name of the branch.

![](./images/delete_branch.jpg)

### Check branch status after delete

Can confirm that the branch has been deleted by checking status.

![](./images/delete_branch_status.jpg)

### Merging a changed branch into another changed branch

When attempting to merge a changed branch (in this case 'UpdateText' with the main branch), a conflict message is displayed.

![](./images/change_to_change.jpg)

This conflict needs to be resolved in file explorer.

Opening the conflicted file shows the header HEAD prefixing the current text in the main branch with the conflicting text from the UpdateText branch beneath.

# Github guide

## Background

Reminder that git is a version control system that works through a repository hosted on a local computer.

Github is an extension of that where the hosting takes place in the cloud, enabling collaboration in teams and issue tracking etc.

Start by creating a Github account with login.

### Creating a Github repository

From the Home screen, create a new repository.

![](./images/github_new_repo.jpg)

### Name the repository

Name the new repository, add description if required and make it public or private. Public may be viewed by anyone. Private in this instance means it can be shared with designated members.

NOTE: Repository name must end with file extension .git

![](./images/github_new_repo_2.jpg)

### Choose files to ignore

The ignore file has the same use in Github as it does in Git. An ignore file can be set up on the new repository page.

![](./images/gh_ignore.jpg)

### Choose a license

A license can be set up to tell others what they can and can't do with your code.

#### Create a Github repository from the command line

An alternative to the above is to create a Github repository from the command line.

![](./images/gh_repo_command_line.jpg)

### Push a local repository to Github

This option will push an existing, local Git repository to Github.

Enter the three commands into the command line.

![](./images/push_repo_to_github.jpg)

The result should look like this.

![](./images/push_to_gh_result.jpg)

The complete repository will have been pushed to Github.

### Open the repository

From the Github home screen, click on the repository name.

The repository will be displayed.

![](./images/view_gh_repo.jpg)

### Pushing all branches to Github

The previous actions have pushed only the main branch to Github. To push all branches to Github, use this command.

![](./images/add_branch_to_gh_1.jpg)

In Github there are now two branches shown.

![](./images/add_branch_to_gh_2.jpg)

![](./images/add_branch_to_gh_3.jpg)

## Editing files

### Branch view

The branch view shows the branch contents with notes that were added about the files' history.

Click on a file to preview it.

![](./images/gh_repo_view.jpg)

### Adding files

Files can be dragged into the folder view or added manually with the 'Add File' tab.

![](./images/gh_add_file.jpg)

### Edit history

Click on a file's notes to display its edit history.

![](./images/gh_file_history_1.jpg)

![](./images/gh_file_history_2.jpg)

### Edit a file within Github

Click on any file in the folder view to open it for editing.

A file editor will open within Github.

Click on the edit icon to edit the file.

![](./images/gh_file_editor_1.jpg)

### Commit edits within Github

Scroll down to commit edits to Github.

![](./images/gh_commit_edits.jpg)

## Synchronising Github changes locally

Use the command git fetch to view the changes on Github.

![](./images/git_fetch_1.jpg)

To merge the changes shown, use git merge.

![](./images/git_merge_1.jpg)

To combine both commands, use git pull.

![](./images/git_pull.jpg)

