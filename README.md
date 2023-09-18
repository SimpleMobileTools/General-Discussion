# General-Discussion
A place for discussing all apps in general + anything else you want to say.

FAQ
---
## How do I suggest an improvement, ask a question or report an issue?
1. this General Discussion repository is used for bugs and suggestions that affect multiple apps. For issues affecting only 1 app use its separate repository
2. if you are reporting a bug, try giving steps for reproducing too. Also mention your app and OS version
3. make sure you use the latest app version and read the in-app FAQ before reporting anything
4. make sure the given thing isn't reported yet, you can also use Search with some keywords
5. if the thing you wanted to report has already been reported, don't forget giving it an upvote to increase its priority

<p>&nbsp;</p> 

## Contribution rules for developers
1. every project contains an .editorconfig file, it has definitions of required indentations, newlines etc
2. always format the code (Ctrl + Alt + L) and optimize imports (Ctrl + Alt + O) before creating a pull request
3. if you add a new string, add it into all languages. If you speak a language yourself, translate it. If not, just use the english version. Do not use machine translating
4. if you add a new icon, make sure it is prefixed with "ic_", it is white and try using vectors
5. if you change something in the UI, test the visibility with all themes, including Black & White and System default (Material You) on Android 12+. Test the changes by using the biggest system font size too.
6. use the existing code style and naming conventions, do not bring your own style
7. always use brackets, even at 1 liner "if", "return" or "continue" statements etc
8. if you add a new model or work with gson, test the build in release mode with proguard enabled aswell
9. there is no real functionality change between build flavors, only some About button visibility differences, Rate Us dialog and More Apps From Us buttons not showing up or so. The proprietary gallery build has a more advanced photo and video editor, while the foss one has a basic only.

If you try fixing a bug or adding a new feature, you should make sure that it is already reported at the given repository and the report is open and marked as a Bug or Feature Request. If the given issue is closed, chances are that we are not interested in the given feature and your pull request will likely be rejected.

<p>&nbsp;</p> 

## How can I suggest an edit to a file?
Creating pull requests with some changes is a lot simpler than most people think. Most suggestions are related to translating strings, there are 2 ways to do it.
You can find our apps on Weblate at https://hosted.weblate.org/projects/simple-mobile-tools/ , you can see untranslated strings there easily.

However, if you prefer the oldstyle file updating via Github, you can still do it. The process is the following:
1. log in to Github
2. find the file with the strings (app/src/main/res/values(-xx)/strings, for example the Italian translation of the Gallery is at https://github.com/SimpleMobileTools/Simple-Gallery/blob/master/app/src/main/res/values-it/strings.xml
3. click the pencil button at the top right corner of the file
4. edit the file with your suggestions*
5. add a commit message under the file, to the textfield which has a hint similar to "Update strings.xml". Just type in what have you done, for example "updating spanish strings"
6. click `Propose file change`
7. click the green button `Create pull request`
8. thank yourself!

\* Change only the string which is between ">" and "\</string\>", _not_ the first one after the "name=" tag, also not the strings between "\<!--" and "-->"  
\* Please escape apostrophes, meaning you have to put a backslash before every apostrophe to make it look like: \\'

For finding the proper language file at the Gallery go to https://github.com/SimpleMobileTools/Simple-Gallery/blob/master/app/src/main/res, then look for a "values-[language code]" folder. Use the `strings.xml` file inside it. If you can\'t find your language code, the file might not be translated to your language at all yet and you will have to create the whole new file.

<p>&nbsp;</p> 

## How do I add a new file?
You will most likely want to add a new file only if you translate an app in a new language. Doing it is actually not difficult at all, just read on.

1. log in to Github
2. find the place where the new file belongs. If it's really a translation of the strings in a new language, go to app/src/main/res, for example https://github.com/SimpleMobileTools/Simple-Camera/tree/master/app/src/main/res
3. at the top right corner click at `Create new file`
4. after the `res` folder you can type in your folder path. For creating a German translation just type in `values-de/` (where `de` is the country code). The new folder will be added automatically after typing the slash
5. add a file name, i.e. `strings.xml` (the path should look similar to the image below)<img alt="Github new file path" src="Media/Screenshots/Readme/github_new_file.png" />
6. copy the contents of an already existing strings.xml file into the new file (for example the content of https://github.com/SimpleMobileTools/Simple-Camera/blob/master/app/src/main/res/values/strings.xml)
7. add your string translations*
8. add a commit message under the file, to the textfield which has a "Create new file" hint. Just type in what have you done, for example "adding spanish strings"
9. press `Propose new file`
10. click the green button `Create pull request`
11. thank yourself!

\* Change only the string which is between ">" and "\</string\>", _not_ the first one after the "name=" tag.  
\* Please escape apostrophes, meaning you have to put a backslash before every apostrophe to make it look like: \\'

<p>&nbsp;</p> 

## How can I get notified if a translated file changes?
Sadly Github doesn't have any built in way of setting up notifications/emails when a file changes, but there is a third party service https://app.github-file-watcher.com which seem to work just fine. It sends you an email whenever a new string is added or the watched file changes for whatever reason.
There are 3 fields you have to fill.
1. your email address
2. the repository which contains the target file, here is a list of the repositories. It appears that you will have to fill in the forms for every repository one by one, batch adding doesn't seem to be supported.  

    SimpleMobileTools/Simple-App-Launcher  
    SimpleMobileTools/Simple-Calculator  
    SimpleMobileTools/Simple-Calendar  
    SimpleMobileTools/Simple-Camera  
    SimpleMobileTools/Simple-Clock  
    SimpleMobileTools/Simple-Contacts  
    SimpleMobileTools/Simple-Dialer  
    SimpleMobileTools/Simple-Draw  
    SimpleMobileTools/Simple-File-Manager  
    SimpleMobileTools/Simple-Flashlight  
    SimpleMobileTools/Simple-Gallery  
    SimpleMobileTools/Simple-Keyboard  
    SimpleMobileTools/Simple-Launcher  
    SimpleMobileTools/Simple-Music-Player  
    SimpleMobileTools/Simple-Notes  
    SimpleMobileTools/Simple-SMS-Messenger  
    SimpleMobileTools/Simple-Thank-You  
    SimpleMobileTools/Simple-Voice-Recorder  

    SimpleMobileTools/Simple-Commons (for this repository the file path in the next step will be different)

3. the file path. For all regular apps the path will be `app/src/main/res/values-xx/strings.xml`, replacing `xx` with your language code. For `Simple-Commons` repository the path begins with `commons`, making it `commons/src/main/res/values-xx/strings.xml`.

If you've setup everything properly, you should get a confirmation email for every repository. Then, whenever a file changes, you will get an email about it. The email will arrive only a couple hours after the actual file has been changed, but it's still good enough.

This is a sample email, that you will receive once a file changes, in this example I'm using the German translation of the Calendar app.  

<img alt="Github File Watcher" src="Media/Screenshots/Readme/github_watcher_email.png" />

You can see that it contains multiple clickable links, let's describe them from the bottom. The first one is for easy unsubscribing, when you don't want to watch the file anymore.  
The middle one contains a link to the specific commit, which changed the file. If you search for "values-de", you can easily see what exactly changed.  
The link at the top points to the new version of the file, created by the commit. It points to a side branch though, you will have to switch to the master branch. It's really easy, just look at the part above the file and look for a `Tree: xxxx` button, as seen on this screenshot.

<img alt="Github File Watcher" src="Media/Screenshots/Readme/github_watcher_branch.png" />

Click on it, then select `master`. You will be redirected to the latest version of the file, which you can already edit by pressing the pencil, as described [here](https://github.com/SimpleMobileTools/General-Discussion#how-can-i-suggest-an-edit-to-a-file).
