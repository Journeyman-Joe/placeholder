### [Princeton STEM Academy](../../index.md)

## Cloning the *Biobuzz* Repository

September 7, 2025

FTC has just released the initial Robot Controller SDK for the *Biobuzz* season; version 12.0. I have prepared these instructions to allow the Princeton STEM Academy teams to load the new SDK onto their personal laptops without my help, by leveraging their team access credentials from the prior season.

*Note that new programmers, or programmers who have switched teams, don't have prior season team access credentials. I'll be working with the programmers on those teams individually to get them set up.*

(Don't worry about the shared laptops in the Academy. I'll be updating those myself.)

### Note regarding Android Studio versions

FIRST introduced a *breaking change* with SDK 11.2. Check your Android Studio version (splash screen or `Help | About`). You need "Narwhal 3" or a newer version (Otter, Panda, or Quail) to use this SDK.

See the [Android Studio upgrade](#android-studio-upgrade) section, below.

### Note regarding third-party resources

As of this writing, Acme Robotics has not updated their Roadrunner repository to use the SDK 12.0 baseline. I have not looked for anything regarding Pedro Pathing, or any of the other third-party resources you may be using.

### Cloning the repository onto your personal laptop

I've copied this repository into a template for the Princeton STEM Academy teams:
*Biobuzz*, and uploaded it into your teams' GitHub accounts.

If you already have GitHub credentials from a prior season (*Decode*, *IntoTheDeep*, *CenterStage* or *PowerPlay*) on your personal laptop,
you should be able to clone the *Biobuzz* repository without my help.
I'll encourage you to try it on your own.
Assuming that you used my naming conventions when setting things up initially,
these instructions should work.

Open a Command Prompt Window (PC) or a Terminal Window (Mac). Your Android Studio projects will either be in a folder named `android-workspace`, or `StudioProjects`, or  `AndroidStudioProjects`. **Only one** of the following commands will work (use Copy & Paste):
```
cd android-workspace
cd StudioProjects
cd AndroidStudioProjects
```
Then, enter one of the following commands:

PC:
```
dir
```

Mac:
```
ls
```

You should see a list of your current repositories, which may include *Decode* *IntoTheDeep*, *IntoTheDeepRR*, *CenterStage*, *CenterStageRR*, *CenterStageQQ*, *PowerPlay* or *PowerPlayRR*.
Enter **one (and only one)** of these commands to match (it doesn't matter which one you have):
```
cd Decode
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
Your prompt should now be back at `android-workspace`, `StudioProjects` or `AndroidStudioProjects`,
and not show you as being inside a `Decode`, `IntoTheDeep`,  `PowerPlay` or `CenterStage` repository.

Type
```
git clone
```
add a space, and then paste (with CTRL-V) the URL that you copied before.
**Do not hit enter!** Using the left and right cursor arrow keys, and the backspace key,
delete the *Decode*, *IntoTheDeep*, *PowerPlay* or *CenterStage* reference, and replace it with *Biobuzz* (exactly).
Leave the `.git` suffix attached.

Let's look for a moment at what you've got.
It's a `git clone` command, pointing to your team GitHub account.
The string that starts with `ghp_` and ends before the `@` sign is your GitHub *Personal Access Token* (PAT)
that lets you push and pull to and from your team's account.
The manual edits point the `git clone` command to the new *Biobuzz* repository.

Now go ahead and hit *enter*.
You should see a download of you new repository.

[_homepage / index_](../../index.md)
