# git-graph

Tool to create a graph from a git history showing tags, branches, stash nodes, cherry-picks.
Forked repository to make small changes for Windows 10. Original was geared to linux. The changes were minor. 

## Requirements

* Python3
* Graphiz

## Create a graph

Run the following inside a git directory to write a graph description to stdout.

    python git-graph.py

On Windows 10 you can use the following command to crate a graph.png file

    python git-graph.py | dot -Tpng -o graph.png

Example with range

    python git-graph.py -r a51eced..HEAD | dot -Tpng -o graph.png

### Parameters
* **-x**: to print debug output to stderr
* **-m**: show commit messages in nodes
* **-r range**: to get a specific range of the repository. See [here](http://git-scm.com/book/en/Git-Tools-Revision-Selection#Commit-Ranges)

# Example Graph
![alt text](images/example.gif)
