
# NECX Project Page

This is the repository that holds the project work for the Nuclear Engineering 
Curriculum eXchange.

## Building This Website

This website should be maintained collectively by the members of the project.

### Set Up


1. (Optional) Install the build dependencies for the website. These include ruby, jekyll,
   and jekyll-scholar. Get started [here.](https://jekyllrb.com/docs/installation/).
2. [Fork](https://github.com/necx-org/necx-org.github.io#fork-destination-box) the website repository.
3. Clone your fork. If you have [your ssh keys set up](https://help.github.com/articles/generating-an-ssh-key/)
   and your username is USERNAME, the command is `git clone
   git@github.com:USERNAME/necx-org.github.io`
4. Add the group fork as a remote. `cd necx-org.github.io && git remote add upstream
   git@github.com:necx-org/necx-org.github.io`
5. Use `git branch` to confirm that you are in the `source` branch.

Now, you're ready to make changes to the website. There are a few types of
changes that are common:

- Edits to the text
- Adding yourself to the people page
- Creating a manual entry or node description.

### Rendering the nodes

The curriculum content appears in [the nodes repository](https://github.com/necx-org/nodes). To render them within the website, follow these instructions:

1. Do the setup steps above. 
1. change to the top-level directory for this repo `cd necx-org.github.io`
1. initialize the `_nodes` submodule with `git submodule init`
1. update the `_nodes` submodule with `git submodule update`
1. run a `jekyll serve` instance and look at http://localhost:4000/nodes/

To review changes to nodes we need to pull in the nodes repository in a way that this repository understands it. The way to do this is with a submodule, as below.

1. go to the `_nodes` directory
2. checkout a branch that has the changes you are interested in reviewing
  * you may want/need to add another git remote to fetch those changes
3. If you don't see your changes, you may need to restart the jekyll server (kill with `ctrl-c` and restart with `jekyll serve`)  and look at http://localhost:4000/nodes/



### Add Yourself: Customize

One fun exercise to get started with this website is to add yourself to the people page.

1. Once you have done the set up steps, enter the source branch of the repository. `git checkout source`
2. Add your photo to the repository (in img/people). If your name is Jane Doe, call it `doej.png`.
3. Don't forget to git add and git commit the photo `git add img/people/doej.png` and `git commit -am "adds a photo of Jane Doe"`
4. Open the file `_data/people.yml` and add your details.
5. Close the file and commit your changes (`git commit -am "added Jane Doe details to people data"`)
6. (Optional) Check whether your changes succeeded by typing `jekyll serve` from the top
   level directory of the website repository. Then, open a browser to
   `localhost:4000`.
7. When you're satisfied, push your changes to your own fork with `git push origin
   source`.
8. Finally make a pull request from your source directory to the necx-org fork of necx-org.github.io.

If you're feeling confident, you can skip the pull request. Instead, you can
just push changes to the website directly with the command `rake publish`. Only
do this if you don't need anyone to double check your work.

### Useful Resources

If you're new to contributing, here are some great resources:

#### Git and GitHub

- [Yes, you can git! An introduction to git and GitHub](https://speakerdeck.com/willingc/yes-you-can-git)
- [Git cheatsheet by GitHub](https://services.github.com/kit/downloads/github-git-cheat-sheet.pdf)

#### Markdown

- [Markdown cheatsheet by GitHub](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)
