any file or directory within the 'files' portion of the json file will not be allowed to be committed by any user unless they are within an authorized team within an organization
that is mentioned within the cooresponding list. Please make sure you have your 'git_token' set within the hooks/config file of the git-hooks reposistory. This must have read:org 
permissions in order to find every member in a certain team within an organization. This is how we determine authorization.

To restrict a directory, you must simply write the directory name, and nothing else. e.g. 'restricted_dir/*' or 'restricted_dir/' will NOT work. 'restricted_dir' will work.
This will block the directory itself from being committed, meaning all files within the directory as well.

To restrict a file, you must write the exact file name and its proper extension. (e.g file.txt or main.py)

Please note that everything is case sensitive.

You do not want to touch the 'disallowed issue states.'
