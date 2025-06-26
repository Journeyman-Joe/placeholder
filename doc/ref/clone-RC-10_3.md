### [Princeton STEM Academy](../../index.md)

## Cloning the *RC-10_3* Repository

June 26, 2025

FTC has just released the (presumed) final Robot Controller SDK for the *Into The Deep* season; version 10.3. Historically, the post-season SDK release provides FTC teams with an early look at new features for the upcoming season. (No doubt that FIRST benefits from the expanded testing community, as well.)

### Note regarding Android Studio versions

FIRST introduced an unavoidable *breaking change* with SDK 10.1.1. If your team used SDK 10.0 or SDK 10.1 during the *Into The Deep* season, you probably have a "Koala" or earlier version of Android Studio on your laptop. You will have to update your version of Android Studio to "Ladybug", or newer to use this RC-10_3 SDK, or the expected SDK 11.0 next season.

See the [Android Studio upgrade](#android-studio-upgrade) section, below.

### Note regarding third-party resources

As of this writing, Acme Robotics has not updated their Roadrunner repository to use the SDK 10.3 baseline. I have not looked for anything regarding Pedro Pathing, or any of the other third-party resources you may be using.

### Cloning the repository onto your personal laptop

I've copied this repository into a template for the Princeton STEM Academy teams:
*RC-10_3*, and uploaded it into your teams' GitHub accounts.
(I have not yet pulled it down onto the PSA shared laptops, as they do not have compatible versions of Android Studio at this time.) 

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

### Android Studio upgrade

In brief: Newer versions of the SDK won't work with older versions of Android Studio. Also: newer versions of Android Studio won't work with older versions of the SDK.

This is awkward for everybody. It can't be helped.

#### Option 1: Don't look back

With this option, you upgrade your Android Studio installation to "Ladybug", or newer ("Narwhal", as of this writing). You will not be able to build your SDK 10.1 or older repositories.

To keep your *IntoTheDeep* robot functional, I recommend copying your Java classes from your old repository into the new RC-10_3 repository, and build an *IntoTheDeep* Robot Controller using SDK 10.3. I've already created an `IntoTheDeep` branch in our new RC-10_3 repository for that purpose.

This should work well for teams that aren't using Roadrunner, or other third-party libraries.

#### Option 2: Multiple versions of Android Studio

Online search suggests that it's possible to have multiple versions of Android Studio on the same computer, without interference. I will be testing this capability on Windows, and will update this section accordingly.

I have no idea whether or not Macs will support multiple versions of Android Studio, and would welcome contributions from our Mac-fan group of programmers.

This is probably the best solution for teams that **are** using Roadrunner, or other third-party libraries.




[_homepage / index_](../../index.md)
