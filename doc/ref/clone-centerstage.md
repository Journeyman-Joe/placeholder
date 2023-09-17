### [Princeton STEM Academy](../../index.md)

## Cloning the *CenterStage* and *CenterStage - RoadRunner Quickstart* Repositories

FTC has already released the new Robot Controller SDK 9.0 for the Center Stage season; very timely.
The good folks at Acme Robotics were right on top of it, too:
there's a new RoadRunner Quickstart repository for this version of the SDK, also ready to go.

I've  cloned both repositories into templates for the Princeton STEM Academy teams:
*CenterStage* and *CenterStageRR*, and uploaded them into your teams' GitHub accounts.
I have also pulled them down onto the PSA shared laptops (all teams).

If you already have GitHub credentials from the *PowerPlay* season on your personal laptop,
you should be able to clone either (or both) of the *CenterStage* repositories without my help.
I'll encourage you to try it on your own.
Assuming that you used my naming conventions when setting things up initially,
these instructions should work.

Open a Command Prompt Window (PC) or a Terminal Window (Mac).
Enter the following commands (Copy and Paste will work):
```
cd android-workspace
dir
```
You should see a list of your current repositories, which may include *PowerPlay* or *PowerPlayRR*.
Enter **one (and only one)** of these commands to match:
```
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
Your prompt should now be back at `android-workspace`,
and not show you as being inside a `PowerPlay` repository.

Type `git clone`, add a space, and then paste (with CTRL-V) the URL that you copied before.
Do not hit enter!  Using the left and right cursor arrow keys, and the backspace key,
delete the *PowerPlay* reference, and replace it with either *CenterStage* or *CenterStageRR*.
Leave the `.git` suffix attached.

(If it's not already clear:
Clone *CenterStage* if you want the plain FTC SDK.
Clone *CenterStageRR* if you want the Acme Robotics RoadRunner Quickstart SDK.
You can clone both, if you want:
Just use the "up" cursor arrow after the first clone operation,
and edit the `git clone` command (arrow and backspace keys only) 
to point to the other repository.)

Let's look for a moment at what you've got.
It's a `git clone` command, pointing your your team GitHub account.
The string that starts with `ghp_` and ends before the `@` sign is your GitHub Personal Access Token (PAT)
that lets you push and pull to and from your team's account.
The manual edits point the `git clone` command to the new *CenterStage* repository.

Now go ahead and hit *enter*.
You should see a download of you new repository.

That's it; open Android Studio and start exploring.
Note that it won't show up in your "recently used" list, the first time.
You will have to "Open" it as a new repository from the top menu,
and "Trust" the project.

I'll encourage you to start with the *AprilTags* samples,
in the *external.samples* folder.
*ConceptAprilTagEasy.java* is a good place to begin.

[_homepage / index_](../../index.md)
