# General-Discussion
A place for discussing all apps in general + anything else you want to say.

FAQ
---
### How do I suggest an improvement, ask a question or report an issue?
If you want to do anything from above, just create a new issue at the [Issues section](https://github.com/SimpleMobileTools/General-Discussion/issues) . Please be constructive and on-topic. In case you are reporting an issue either here, or at some specific app's repository, please give as much useful information as possible, ideally with steps to reproduce. Being able to reproduce a bug and understand it can really speed up the fixing.

<h3>How can I suggest an edit to a file?</h3>
Creating pull requests with some changes is a lot simpler than most people think. Most suggestions are related to the translated strings, the steps are as follows:

1. Log in to Github
2. Find the file with the strings (app/src/main/res/values(-xx)/strings , i.e. https://github.com/SimpleMobileTools/Simple-Gallery/blob/master/app/src/main/res/values/strings.xml
3. Click the pencil button at the top right corner of the file
4. Edit the file with your suggestions*
5. Enter a commit message to the first row under the file, optionally a description in the second one
6. Click "Propose file change"
7. Thank yourself!

\* Change only the string which is between ">" and "\</string\>", _not_ the first one after the "name=" tag. That will save me a lot of headaches.

<h3>How do I add a new file?</h3>
You will most likely want to add a new file only if you translate an app in a new language. Doing it is actually pretty fairly straightforward, just read on.

1. Log in to Github
2. Find the place where the new file belongs. If it's really a translation of the strings in a new language, go to app/src/main/res, for example https://github.com/SimpleMobileTools/Simple-Camera/tree/master/app/src/main/res
3. At the top right corner click at "Create new file"
4. After the "res" folder you can type in your file path. For creating a new folder just type in "values-xx/" (where xx is your country code). The new folder will be added automatically after typing the slash.
5. Add a file name, i.e. strings.xml.
6. Copy the contents of an already existing strings.xml file into the new file (for example the content of https://github.com/SimpleMobileTools/Simple-Camera/blob/master/app/src/main/res/values/strings.xml)
7. Make sure to delete the lines which contain the "translatable=false" part. You could copy the contents of a non-english file aswell which already don't contain those lines, but you would still have to read the english version to understand what does the string say.
8. Add your string translations*
9. Add a commit message, optionally a description too.
10. Press "Propose new file"
11. Thank yourself!

\* Change only the string which is between ">" and "\</string\>", _not_ the first one after the "name=" tag.
