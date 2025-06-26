### [Princeton STEM Academy](../../index.md)

## Cloning the *RC-10_3* Repository

June 26, 2025

FTC has just released the (presumed) final Robot Controller SDK for the *Into The Deep* season; version 10.3. Historically, the post-season SDK release provides FTC teams with an early look at new features for the upcoming season. (No doubt that FIRST benefits from the expanded testing community, as well.)

I've  cloned this repository into a template for the Princeton STEM Academy teams:
*RC-10_3* and uploaded it into your teams' GitHub accounts.
I have also pulled it down onto the PSA shared laptops (all teams).

If you already have GitHub credentials from a prior season (*IntoTheDeep*, *CenterStage* or *PowerPlay*) on your personal laptop,
you should be able to clone the *RC-10_3* repository without my help.
I'll encourage you to try it on your own.
Assuming that you used my naming conventions when setting things up initially,
these instructions should work.

Open a Command Prompt Window (PC) or a Terminal Window (Mac). Your Android Studio projects will either be in a folder named `android-workspace`, or a folder named `AndroidStudioProjects`. **Only one** of the following commands will work (use Copy & Paste):
```
cd android-workspace
cd AndroidStudioProjects
```
Then, enter the following command:
```
dir
```
You should see a list of your current repositories, which may include *IntoTheDeep*, *IntoTheDeepRR*, *CenterStage*, *CenterStageRR*, *CenterStageQQ*, *PowerPlay* or *PowerPlayRR*.
Enter **one (and only one)** of these commands to match (it doesn't matter which one you have):
```
cd IntoTheDeep
cd IntoTheDeepRR
cd CenterStage
cd CenterStageRR
cd CenterStageQQ
cd PowerPlay
cd PowerPlayRR
```
Now, enter the command:
```
git remote -v
```
Note that the output contains a URL; (the same URL, twice).
Highlight and copy (with CTRL-C) that URL, from `https://` through `.git`.
Don't copy the space after `.git`.

Enter this command:
```
cd ..
```
Your prompt should now be back at `android-workspace` or `AndroidStudioProjects`,
and not show you as being inside an `IntoTheDeep`,  `PowerPlay` or `CenterStage` repository.

Type
```
git clone
```
add a space, and then paste (with CTRL-V) the URL that you copied before.
**Do not hit enter!** Using the left and right cursor arrow keys, and the backspace key,
delete the *IntoTheDeep*, *PowerPlay* or *CenterStage* reference, and replace it with *RC-10_3* (exactly).
Leave the `.git` suffix attached.

Let's look for a moment at what you've got.
It's a `git clone` command, pointing to your team GitHub account.
The string that starts with `ghp_` and ends before the `@` sign is your GitHub *Personal Access Token* (PAT)
that lets you push and pull to and from your team's account.
The manual edits point the `git clone` command to the new *RC-10_3* repository.

Now go ahead and hit *enter*.
You should see a download of you new repository.

That's it; open Android Studio and start exploring.
Note that it won't show up in your "recently used" list, the first time.
You will have to "Open" it as a new repository from the top menu,
and "Trust" the project.

[_homepage / index_](../../index.md)
