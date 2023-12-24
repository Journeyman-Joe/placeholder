### [Princeton STEM Academy](../../index.md)

## Connecting Android Studio to GitHub
### What does this even mean?
This way of working is going to be new to most FIRST Tech challenge programmers; even if you're coming from a Lego League environment, and even if you've been programing in Python using an IDE (even the PyCharm IDE, from JetBrains).

It may help to separate two _functional areas_ in your thinking:

1. The development environment
2. Version control and cloud backup.

#### Development environment
The _development environment_ is what's in front of you. Mostly, it's _Android Studio_ and some supporting tools, such as the _Android Debug Bridge (ADB)_.

You write and edit your Robot Controller programs in the Android Studio editor, "build" a Robot Controller using the Gradle build system included (and configured by FIRST), and download it to  the Robot using the Android Debug Bridge.

If you always work alone, on the same computer, which never breaks or gets lost, and you never make any mistakes, that's all you need.
#### Version control
Most of us aren't like that. Many programmers start off inventing their own *ad hoc* version control, by saving old versions and making the new ones with different names: e.g., `RedAuton`, `RedAuton_A`, `RedAuton_B`, etc. And, for a whole lot of us, (both inside and outside of FIRST Tech Challenge) that works just fine for small- and medium- scale projects.

But, in the larger world, where programming projects go on for years and involve thousands of end-users and hundreds of programmers, we need a more formal system for managing program versions. The choice of programmers worldwide, and especially within the FIRST Tech Challenge, is a product called [Git](./installing-git.md). Mostly, Git functions are called from features of Android Studio, and you won't have to deal with Git commands directly. We won't cover them more than minimally in this article.

#### Cloud backup
To be blunt, any programmer who works without backing up their programs in a safe place is reckless, and putting his / her team in danger. It's irresponsible. Don't be that way.

We at The Princeton STEM Academy use *GitHub* as our cloud backup tool. So do most FIRST Tech Challenge teams, and a very large fraction of software developers in the outside world.

### The Workflow
#### What it isn't
This work environment is **not** like working with an integrated collaboration tool, like Google Docs.
With Google Docs, several people can be working in the same document.
There's only one copy, in the cloud, and everybody's changes are reflected everywhere, simultaneously.

#### What it is
In contrast, in our programming environment, several copies of the same file can exist in different places, at the same time.
It is up to the "liveware" (people) to ensure that we are not getting in each other's way, and creating conflicts.

We have resources to help manage collaboration in this environment.
The most important is to develop the habit of keeping your _Development Environment_ synchronized with the team _Verson Control / Cloud Backup_ environment.

[_homepage / index_](../../index.md)
