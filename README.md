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
* Settings (dangerzone for repo as it can be deleted)

It's a best practice to always commit and push your changes at the end of the working day/shift, so that your remote repo is always up to date.

---

# Workshop

What you are going to do?

* Explore the possibilities of GitHub by creating your own repo, adding files.
* See how GitHub Actions work, so code can be executed automagically.
* Execute GitHub Actions and fix any given issues.

## Preparation

Install the prerequisites:

* [`Sign in`](https://github.com/login) or [`Sign up`](https://github.com/signup) for your GitHub account.
* Install [GitHub Desktop](https://desktop.github.com/) on your laptop.
* Install [Visual Studio Code](https://code.visualstudio.com/download) on your laptop.
* Add [YAML plugin (Redhat)](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) in Visual Studio Code.
* Add [indent-rainbow plugin](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow) in Visual Studio Code.

---

## Hands-on:

### Online - Create repo

* Create repository on [`github.com`](https://github.com)
* Choose `Public`
* Select `Add a README file`
* Click `Create repository`

### Online - Edit README

The README file in a repository provides essential information about the project, guiding users and contributors on its purpose, installation, and usage.

* Check out the [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/)
* Customize README.MD using a sub-heading or other formatting to your liking.

### Local - Clone repo
* Create local Github folder (not to synced drive) eg `C:\Github`
* Start Github Desktop
* Clone repository to earlier created local Github root folder

### Online - Create action workflow
* Create action workflow, click on the `Actions` tab, click on `Simple workflow` template on [`github.com`](https://github.com), click `Configure`
* Save as `build.yml` in `main`
* Start `Commit changes`

### Online - Check results of the workflow
* Navigate to `Actions` and open `All workflows`
* Select the name of the workflow `CI` on the left node.
* Click on the last workflow run (name contains the last commit message)
* Click on `build`
* Inspect the outcome.

### Local - Add a certain action to the workflow
* Open Visual Studio Code
* Open repository folder from File Explorer or Visual Studio Code
* Open `.github/workflows/build.yml`
* Enhance the script with the a lookup of the OS version, put the following in the one-liner `uname -a`
* Make sure that [the output is saved to a file](https://askubuntu.com/questions/420981/how-do-i-save-terminal-output-to-a-file), the filename must be `${{ github.workspace }}/release.txt` for further processing reasons
* Save `build.yml`
* Commit changes
* Push to origin

### Local - Alter action workflow to use other OS-release on action runner
* Open `.github/workflows/build.yml`
* Inspect which FB is active in Github Desktop
* Change `ubuntu-latest` to `ubuntu-1337`
* Save `build.yml`
* Commit changes
* Push to origin

### Online - Check action runner workflow for the build.yml
* Check the Action on Github.com
* Check the outcome of the action workflow

### Local - Revert the changes
* Make sure that the correct type of OS-release on action runner is used again
* Commit changes

### Online - Re-check action runner workflow for the build.yml
* Check the Action on Github.com again

### Artifacts

A GitHub artifact is a file or collection of files generated during the software development process and stored on GitHub for easy access and distribution.

* Include the `upload artifact` action in the previously created workflow.

### Create `Upload a Build Artifact` artifact action to the workflow on github.com
* Open `.github/workflows/build.yml`
* Click `Edit this file` (Pro-tip: ✎)
* Search `Upload a Build Artifact` from the marketplace.
* Copy snippet to the `build.yml`
* Make sure the indention is correct
* Delete all lines from 'Available Options:' to EOF.
* Set `name` to: `name : Artifact RawWorks`
* Set `path` to: `path : ${{ github.workspace }}/release.txt`
* Save build.yml
* Validate the `Actions` output

# Wrap-up

## Favorable conduct

<ul>
  <li> <details><summary>Codes of conduct</summary><blockquote>
    <details><summary>In case of fire!</summary><blockquote><img src="https://rawworks-nl.github.io/education-github-introduction/assets/img/git-in-case-of-fire.png"></blockquote></details>
    <details><summary>Growth-oriented stance</summary><blockquote><a href=https://github.com/Coding55/developer-mindset target="_blank">Developer mindset by Coding55</a></blockquote></details>
    <details><summary>Important; License terms</summary><blockquote><a href=https://dbad-license.org target="_blank">DBAD</a></blockquote></details>
  </blockquote></details>
  </li>
</ul>

## Q&A

[Questions?](https://github.com/rawworks-nl/education-github-introduction/issues)

---

# Acknowledgments

  * Ideas and content by [Etienne Haarsma](https://github.com/Etienne-RAW) and [Berry de Jager](https://github.com/berrydejager) with the help of [chatGPT](https://chat.openai.com)
* Visuals:
  * ['Reveal-Jekyll template'](https://github.com/sylhare/Reveal-Jekyll) created by [Sylhare](https://github.com/sylhare)
  * ['In case of fire'](https://github.com/louim/in-case-of-fire) created by [Louis-Michel Couture](https://github.com/louim)
  * 'QR for FSFS' is created using [QR code Generator](https://www.the-qrcode-generator.com/)
* Audio:
  * 'Get ready intro' is curated by [Krafty Kuts](https://kraftykuts.com/)
* Bonus:
  * [Free Software, Free Society](https://www.tedxgeneva.net/talks/richard-stallman-free-software-free-society/) by [Richard Stallman](https://en.wikipedia.org/wiki/Richard_Stallman) at [TEDxGeneva](https://www.tedxgeneva.net/)

---
