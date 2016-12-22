# gitcrypt-test

1. Create git-hub repo for your TF files.
2. Commit the repo and merge to master.
3. Create a branch.
4. Generate cluster.conf
5. Create a /secrets folder in the repo.
6. Put cluster.conf in the /secrets folder.
7. Commit the changes.
8. Install git-crypt.
9. Configure the repo to use git-crypt:

git-crypt init
Generating key...

10. Create the .gitattributes file and specify that files in the `secrets` directory should be encrypted.

secrets/** filter=git-crypt diff=git-crypt

NOTE: Do not put this file in the /secrets folder (you don't want it encrypted).

11. Share the repository with others (or with yourself) using GPG:

git-crypt add-gpg-user USER_ID

12. 
