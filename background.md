What happens in the background
==========================
A Git repository is an on-disk data structure which stores metadata for a set of files and/or directory structure. Explore the .git directory for more insights. 

The trees
---------
The local repository consists of three "trees" maintained by git. 
- Working Directory which holds the actual files 
- Index which acts as a staging area
- HEAD which points to the last commit

The objects
-------------
There are 4 types of objects which are stored in the .git/objects directory. They are stored as a plaintext file, zlib’d and referenced by its SHA1 hash.  
1. Blobs are 'file data'. They are just the contents of the file, referenced by the SHA1 hash of the zlib.  
2. Tree objects are analogous to a directory. It stores a list of blobs (and the names of their files)and other trees (subdirectories).  
3. Commit objects only stores metadata related to the commit. 'tree' points to a tree object which contains the working directory in the state when the commit was made. 'parent' lists one or more parent commits.  
4. Tag objects provides a permanent reference and easy-to-remember name for a commit.  

There are 4 types of meta-objects called references which are stored in the .git/refs directory.. 
Objects never change once they are created; references change constantly.    
1. heads and branches  
    The HEAD reference always points to the current branch. Other build in pointers ORIG_HEAD, FETCH_HEAD, and MERGE_HEAD
    A branch always points to the latest commit in that branch.  
2. remotes  
3. tags  
4. stash  
￼