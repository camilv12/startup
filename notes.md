# Introduction
## Useful Console Commands
- `echo` - Output the parameters of the command
- `cd` - Change directory
- `mkdir` - Make directory
- `rmdir` - Remove directory
- `rm` - Remove file(s)
- `mv` - Move file(s)
- `cp` - Copy files
- `ls` - List files
- `curl` - Command line client URL browser
- `grep` - Regular expression search
- `find` - Find files
- `top` - View running processes with CPU and memory usage
- `df` - View disk statistics
- `cat` - Output the contents of a file
- `less` - Interactively output the contents of a file
- `wc` - Count the words in a file
- `ps` - View the currently running processes
- `kill` - Kill a currently running process
- `sudo` - Execute a command as a super user (admin)
- `ssh` - Create a secure shell on a remote computer
- `scp` - Securely copy files to a remote computer
- `history` - Show the history of commands
- `ping` - Check if a website is up
- `tracert` - Trace the connections to a website
- `dig` - Show the DNS information for a domain
- `man` - Look up a command in the manual
## Github
### Repositories
You can create a repository on GitHub or by using the `git init` command on Git Bash. You can then clone it to your local environment using the `git clone` command and copying the url to your repository.
###Making Changes
There are three main commands in the console that you will use when working on your project.
* `git pull` will pull the repository's changes from GitHub
* `git commit` will commit any changes made to the code
* `git push` will push changes to GitHub
The first time you push changes to GitHub, it will ask you how you want to identify yourself.
A few other useful commands include:
* `git fetch` will get the latest information on GitHub without changing the local repository.
* `git status` will check the differences between the clones and will let you know if you are missing a commit.
###Handling merge conflicts
Typically, you can avoid merge conflicts by pulling the code and pushing it often. Merge conflicts occur if at least one line in the code differs between commits. You simulated a merge conflict in conflictTest.md. 
In testing the merge conflict, you can run the `git fetch` and the `git status` commands to check the differences.
```sh
➜  git fetch
➜  git status
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)
```
This will show that cloned repositories have diverged from each other. This is fine unless the exact same line was changed between commits. When you run the `pull` command, you will see this:
```sh
➜ git pull
Auto-merging conflictTest.md
CONFLICT (content): Merge conflict in conflictTest.md
Automatic merge failed; fix conflicts and then commit the result.
```
When you open up VSCode, you will see something like this
```
I will use this file to test merging conflicts.

<<<<<<< HEAD
Example: Conflict change made in development environment
=======
Conflict change made in GitHub
>>>>>>> b9f4c53c91eff509993d7291e60148f903827de0
```
To fix the merge conflict, you will use the file editor to keep the changes that you want to make from each commit and then push the result.
```
I will use this file to test merging conflicts.

Example: Conflict change made in development environment and in in GitHub
```
Use the `commit` command and the `push` command to push the changes.
```sh
➜  git commit -am "merge(notes) combined both edits"
➜  git push
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 701 bytes | 701.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/camilv12/startup.git
   a5acfe0..9bd6fdd  main -> main
```

## HTML
### Elements
#### Common elements

Modern HTML contains over 100 different elements. Here is a short list of HTML elements that you will commonly see.

| element   | meaning                                                                |
| --------- | ---------------------------------------------------------------------- |
| `html`    | The page container                                                     |
| `head`    | Header information                                                     |
| `title`   | Title of the page                                                      |
| `meta`    | Metadata for the page such as character set or viewport settings       |
| `script`  | JavaScript reference. Either a external reference, or inline           |
| `include` | External content reference                                             |
| `body`    | The entire content body of the page                                    |
| `header`  | Header of the main content                                             |
| `footer`  | Footer of the main content                                             |
| `nav`     | Navigational inputs                                                    |
| `main`    | Main content of the page                                               |
| `section` | A section of the main content                                          |
| `aside`   | Aside content from the main content                                    |
| `div`     | A block division of content                                            |
| `span`    | An inline span of content                                              |
| `h<1-9>`  | Text heading. From h1, the highest level, down to h9, the lowest level |
| `p`       | A paragraph of text                                                    |
| `b`       | Bring attention                                                        |
| `table`   | Table                                                                  |
| `tr`      | Table row                                                              |
| `th`      | Table header                                                           |
| `td`      | Table data                                                             |
| `ol,ul`   | Ordered or unordered list                                              |
| `li`      | List item                                                              |
| `a`       | Anchor the text to a hyperlink                                         |
| `img`     | Graphical image reference                                              |
| `dialog`  | Interactive component such as a confirmation                           |
| `form`    | A collection of user input                                             |
| `input`   | User input field                                                       |
| `audio`   | Audio content                                                          |
| `video`   | Video content                                                          |
| `svg`     | Scalable vector graphic content                                        |
| `iframe`  | Inline frame of another HTML page                                      |

#### Special Characters
| Character | Entity      |
| --------- | ----------- |
| &amp;     | `&amp;`     |
| <         | `&lt;`      |
| >         | `&gt;`      |
| "         | `&quot;`    |
| '         | `&apos;`    |
| &#128512; | `&#128512;` |

#### Structure
| Element    | Meaning                                                       |
| ---------- | --------------------------------------------------------------|
| `body`     | Top level container. Contains `p`, `span`, `nav`, and `div`.  |
| `header`   | A container with `p`, `span`, `nav`, and `div`                |
| `footer`   | A container with only a single `span`                         |
| `main`     | A containter with `section` and `aside`                       |
| `section`  | A container that contains either `ul` or `table`              |
| `aside`    | A container for content that does not fit the flow of sections|
| `p`        | Paragraph container                                           |
| `table`    | Container used to make a table. Contains `td`,`th`, and `tr`  |
| `ol/ul`    | Ordered List / Unordered list                                 |
| `div`      | Divisions of sub-content                                      |
| `span`     | A container used to markup part of a text inline              |

#### Input
| Element    | Meaning                          | Example                                        |
| ---------- | -------------------------------- | ---------------------------------------------- |
| `form`     | Input container and submission   | `<form action="form.html" method="post">`      |
| `fieldset` | Labeled input grouping           | `<fieldset> ... </fieldset>`                   |
| `input`    | Multiple types of user input     | `<input type="" />`                            |
| `select`   | Selection dropdown               | `<select><option>1</option></select>`          |
| `optgroup` | Grouped selection dropdown       | `<optgroup><option>1</option></optgroup>`      |
| `option`   | Selection option                 | `<option selected>option2</option>`            |
| `textarea` | Multiline text input             | `<textarea></textarea>`                        |
| `label`    | Individual input label           | `<label for="range">Range: </label>`           |
| `output`   | Output of input                  | `<output for="range">0</output>`               |
| `meter`    | Display value with a known range | `<meter min="0" max="100" value="50"></meter>` |

#### Media
Elements used to represent media are `img`, `audio`, and `video`. These elements reference external files. They require the `src` attribute to reference a file.
`svg` and `canvas` are elements that contain code to render an image.


