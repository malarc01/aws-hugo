# Continuous Deployment from Amazon Web Services for Hugo (The world’s fastest framework for building websites)
<p>
<img src="https://imgur.com/Y1b8rqX.png" height="80%" width="80%" alt="General Overview"/>
</p>

# [YouTube: Hugo on AWS Amplify on Terminal as a Second Brain](https://youtu.be/o1DOPndIR1w)


# Install Homebrew - The Missing Package Manager for macOS (or Linux)

go to the following site to install homebrew => https://brew.sh/
<p>
<img src="https://imgur.com/9FSO1eW.png" height="80%" width="80%" alt="General Overview"/>
</p>
Paste this into terminal
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`




# Check for git version
check if git is present via `git --version` if not install git via `brew install git`
<p>
<img src="https://imgur.com/mkLgBeo.png" height="80%" width="80%" alt="General Overview"/>
</p>
# Check for Hugo and Install If Necessary

check if hugo is installed via `hugo version`

# Install Hugo
install hugo via `brew install hugo`

using `hugo version` should work.
<p>
<img src="https://imgur.com/VBZpH3e.png" height="80%" width="80%" alt="General Overview"/>
</p>
# Git Clone with Theme
Choose a directory to clone(copy) the github repository use the following git commands if you are using a theme in Hugo.
<p>
<img src="https://imgur.com/3BHdbkQ" height="80%" width="80%" alt="General Overview"/>
</p>


use `git clone --recurse-submodules GITHUB_CLONE_URL_FROM_REPOSITORY` this will assuming you are using the same PaperMod theme it will automatically copy that theme repository into your themes folder. If you are not using a theme you do not need to worry about this.
<p>
<img src="https://imgur.com/QWUqhQk.png" height="80%" width="80%" alt="General Overview"/>
</p>
use `hugo server` to get a local server to check to make sure Hugo is up and running in your browser.
<p>
<img src="https://imgur.com/H2G4abd.png" height="80%" width="80%" alt="General Overview"/>
</p>
create a post by copying the following information into a markdown file for example you can create a file called 2025.md and inside it would have to have the following.

<p>
<img src="https://imgur.com/XcAvn0T.png" height="80%" width="80%" alt="General Overview"/>
</p>


```
+++
title = 'My First Post of March 2025'
date = 2024-03-10T07:07:07+01:00
draft = true
+++

Today was a good day with Hugo.
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

```


make sure you change the draft = true to false if you want it to be published on the site.

`git status` checks the status of git

`git add . ` this adds the changes to be tracked for version control

use `git commit -m "updated for 2025` to commit the changes with the -m flag for a message

Make sure you create a fine-grained token on the Github website in order to use `git push` which will allow you to upload/push the changes on your computer to the Github website. Select on access to the Github repository that you are using for and give all the permissions to that repository. *MAKE SURE TO WRITE THE TOKEN SOMEWHERE*

<p>
<img src="https://imgur.com/o9IK6Bw.png" height="80%" width="80%" alt="General Overview"/>
</p>

After creating the fine-grained token which is a lengthy sequence of characters you can use `git push `.
It will ask you for your Github username and password.

For the password you want to enter the fine-grained token into the password area.

After this AWS Amplify will build the new changes and publish them to your site.
Please complete the following tasks before continuing:

1. Create an AWS account
2. Install Git
3. Create a Hugo site and test it locally with hugo server
4. Commit the changes to your local repository
5. Push the local repository to your GitHub, GitLab, or Bitbucket account


# Amazon Web Services Instructions
Create a file name in the root of your repository 
`touch amplify.yml`
copy and paste the into the file you created the following.


Log in to your AWS account, navigate to the Amplify Console, then press the Deploy an app button.

Choose a source code provider, then press the Next button.

Authorize AWS Amplify to access your GitHub account.

Select your personal account or relevant organization.

Authorize access to one or more repositories.

Select a repository and branch, then press the Next button.


On the “App settings” page, scroll to the bottom then press the Next button. Amplify reads the amplify.yml file you created in Steps 1-3 instead of using the values on this page.

On the “Review” page, scroll to the bottom then press the Save and deploy button.

When your site has finished deploying, press the Visit deployed URL button to view your published site.


