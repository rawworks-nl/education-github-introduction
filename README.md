# Agenda

* [Why GitHub?](#why-github)
* [What is GitHub?](#what-is-github)
* [How it works](#how-it-works)
* [Workshop exercise](#workshop)
  * [Preparation](#preparation)
  * [Hands-on lab](#hands-on)
* [Wrap-up](#wrap-up)

---

# Why GitHub?

__GitHub allows you to collaborate on automation/code projects. There are several reasons why this is beneficial for you and me.__

GitHub is a platform that allows you to collaborate on automation/code projects. It provides a centralized location for all code and documentation, allows real-time collaboration, and facilitates sharing of code. By using GitHub for collaboration, you can improve your coding skills and knowledge while creating high-quality software.

## Version control

__Did you ever create a script and it doesn´t work anymore after some changes? 'git' is a powerful version control system that allows you to track and view changes to your scripts/code over time.__



## Collaboration

__GitHub provides a platform to collaborate on code with others. Developers can work on the same codebase, manage issues, and review each other's code.__



## Open source

__GitHub is home to a vast number of open-source projects. These projects are available to anyone to use, modify, and contribute to with the end goal of making better software, see: ['Free software, Free society' by RMS](https://www.youtube.com/watch?v=Ag1AKIl_2GM)__



## Community

__GitHub has a large and active community of people who share code, collaborate on projects, and help each other with technical issues.__



## Integration

__GitHub integrates with a wide range of tools and services, making it easy to automate tasks like testing, building, and deploying code.__



## The value of GitHub

  | Value | Benefits |
  | --- | --- |
  | Collaboration | work with anyone, anywhere, any time |
  | Contribute | make software even more better |
  | Code management | create effective, trackable and reversible code |
  | Community | interact and support eachother |
  | Convenience | code is easily available | 

## Overall

GitHub is a valuable tool for people who want to collaborate on code, contribute to open-source projects, and manage their code more effectively.__

---

# What is GitHub?

* GitHub is a web-based platform that provides hosting for Git repositories. It allows developers to store their code in a central location and collaborate with others on software development projects. GitHub provides a wide range of tools and features for managing code changes, tracking issues, reviewing code, and integrating with other tools and services. It is one of the most popular platforms for open-source development and is widely used by developers and organizations around the world. GitHub is maintained by Microsoft.

* 'git' is a distributed version control system that allows you to track changes to files and collaborate with others on software development projects. It provides a way to manage code changes, merge changes made by multiple people, and keep track of different versions of your code over time. Git is widely used in software development and is known for its speed, flexibility, and powerful features. 'git' is created in 2005 by Linus Torvald.

* GitLab is a web-based platform that provides hosting for Git repositories, similar to GitHub. However, GitLab offers additional features such as continuous integration and deployment, built-in code quality and security analysis, and project management tools. GitLab can be self-hosted or used as a cloud-based service, and it offers both free and paid plans for individuals and teams. It is a popular alternative to GitHub, particularly for organizations that require more advanced development and collaboration features. GitLab is maintained by GitLab Inc.

---

# How it works:

To fully understand and use GitHub, it's important to have a basic understanding of the following parts:

* Code (Repository)
  * Private
  * Public
* Issues
* Pull request
* Actions
* Projects
* Wiki
* Security
* Insights
* Settings (where the repo can be deleted, confirmation)


  * Text-based on [markdown language](https://www.markdownguide.org/cheat-sheet/)
  * Clone the repository
    * Start by cloning the repository to your local machine.
    * Create a new branch: Always create a new branch before starting any work.
    * Make changes: Now you can make any changes you need to make to the 'local branch' files on your laptop.
    * Stage changes: Once you have made your changes, you need to stage them. Make sure to stage all the files which are related to specific functionality, see `breaking commits`. __---- NEEDS LINK TO RELEVANT ITEM ----__
    * Commit changes: Once you have staged your changes, you can commit them in your local git clone. Remember to add a meaningful commit message that describes the changes you made.
    * Merge changes: If you are working in a team, someone else may have made changes to the same branch. In that case, you will need to merge their changes with yours before pushing.
    * Push changes: Finally, you need to push your changes to the remote repository. This makes your changes available to others, publicly or privately.
    * Pull changes: Before you start working again, you should always pull the latest changes from the remote repository.

It's a best practice to always commit and push your changes at the end of the working day/shift, so that the repo is always up to date.

---

# Workshop

What you are going to do? 

* Explore the possibilities of GitHub by creating your own repo, adding files.

* See how branches work, locally and remotely and combined with pull requests.

## Preparation

Install the prerequisites:

* [`Sign in`](https://github.com/login) or [`Sign up`](https://github.com/signup) for your GitHub account.
* Install [GitHub Desktop](https://desktop.github.com/) on your laptop.
* Install [Visual Studio Code](https://code.visualstudio.com/download) on your laptop.
* Add [YAML plugin (Redhat)](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) in Visual Studio Code.
* Add [indent-rainbow plugin](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow) in Visual Studio Code.

## Hands-on:

<ul>
  <li>
    <details>
      <summary>
        Create a new public or private repository.<br>
        Note: you can change the visibility whenever needed.
      </summary>
      <blockquote>
        <details>
          <summary>
            Public
          </summary>
          <blockquote>
            Public repositories are accessible to everyone on the internet
          </blockquote>
        </details>
        <details>
          <summary>
            Private
          </summary>
          <blockquote>
            Private repositories are only accessible to you, people you explicitly share access with, and, for organization repositories, certain organization members.
          </blockquote>
        </details>
      </blockquote>
    </details>
  </li>
  <li>
  <details>
    <summary>
      Create README.MD as heading type `H1`
    </summary>
    <blockquote>
      <details>
        <summary>
          Hint
        </summary>
        <blockquote>
           Read the [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/)
        </blockquote>
      </details>
    </blockquote>
  </details>
Note: you can change the visibility whenever needed
</li>
</ul>


* Create README.MD as heading type `H1`.Hint use the [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/)
* Customize README.MD as a sub-heading.
* Customize README.MD by adding an index or [table of contents](https://www.markdownguide.org/hacks/#table-of-contents) to the sub-heading.
* Create feature branch
* Create PR to own main repo, explain 4 eyes principle
* Create GitHub action workflow with Linux and Windows VM (explain that this is an Azure VM, 2000 minutes free per month to use)
* GitHub action workflow add action download repository files
* GitHub action workflow add export to text file Linux and Windows
* GitHub action workflow add upload artifact
* GitHub action workflow add dependency build->release
* GitHub action workflow add pre-release

## Favorable conduct

<ul>
  <li> <details><summary>Codes of conduct</summary><blockquote>
    <details><summary>important; DBAD!</summary><blockquote>[License terms](https://dbad-license.org/)</blockquote></details>
    <details><summary>In case of fire</summary><blockquote>[Take action!](assets/img/git-in-case-of-fire.png)</blockquote></details>
  </blockquote></details>
  </li>
</ul>

---

# Wrap-up

[Questions?](https://rawworks-nl.github.io/education-github-introduction/#/5)

---

# Acknowledgments

  * Ideas and content by [Etienne Haarsma](https://github.com/Etienne-RAW) and [Berry de Jager](https://github.com/berrydejager) with the help of [chatGPT](https://chat.openai.com)
* Visuals:
  * ['Reveal-Jekyll template'](https://github.com/sylhare/Reveal-Jekyll) created by [Sylhare](https://github.com/sylhare)
  * ['git workflow'](https://twitter.com/allison_horst/status/1563210538510737409) created by [Allison Horst](https://github.com/allisonhorst)
  * ['In case of fire'](https://github.com/louim/in-case-of-fire) created by [Louis-Michel Couture](https://github.com/louim)
  * 'QR for FSFS' is created using [QR code Generator](https://www.the-qrcode-generator.com/) 
* Bonus:
  * [Free Software, Free Society](https://www.tedxgeneva.net/talks/richard-stallman-free-software-free-society/) by [Richard Stallman](https://en.wikipedia.org/wiki/Richard_Stallman) at [TEDxGeneva](https://www.tedxgeneva.net/)

---