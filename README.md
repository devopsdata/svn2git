# svn2git
The code to convert SVN into GIT repository

Here are the steps for converting SVN repository into GIT repository.

1. Create a list of Subversion repositories to convert.

2. Create a list of transformations for Subversion usernames to Git committers.
   Run:
   ./fetch-svn-authors.sh  --url-file=[filename] > [output file for raw authors]

   Then edit the raw list of Subversion usernames to provide full names and
   emails suitable for Git committers.

3. Convert the Subversion repositories into bare Git repositories with:
   ./git-svn-migrate.sh --url-file=[filename] --authors-file=[filename] [destination folder]


