# Translating Files

#### The first step is to create a fork of the Files repository where you can make changes.
### Software requirements
- Visual Studio 2017 or newer
- [Multilingual App Toolkit Extension](https://marketplace.visualstudio.com/items?itemName=MultilingualAppToolkit.MultilingualAppToolkit-18308)
- [Multilingual App Toolkit Editor](https://developer.microsoft.com/en-us/windows/develop/multilingual-app-toolkit) (optional)

### Adding a new localization
#### These next steps require Visual Studio with the Multilingual App Toolkit Extension installed
- Open the Files solution in Visual Studio
- Find the "Solution Explorer" window
- Right-click on the project Files(Universal Windows)
- Click on "Multilingual App Toolkit" > "Add translation languages..."
- There may be a dialog that says, "Translation provider manager issue", you can just click "OK" to ignore it.
- Select the language you want to translate by ticking the ✅ in front of that language.
- The resource file that you will translate can be found under `Files(Universal Windows)\MultilingualResources\Files.[language_code].xlf`

### Editing a resource file with the Multilingual App Toolkit Editor
- Navigate to the project folder
- The XLF File should be located at `Files\Files\MultilingualResources\Files.[language_code].xlf`
- Open the file with the "Multilingual App Toolkit Editor"

### Working with resource files
- You can use the translation menu to help with translating, and you can review it later to see if it is correct by using "Translation" > "Translate all" on the Translation section.
- You can use the suggestions for the current text you are translating by using the "Suggest" option under the Translation section in the ribbon.
- The "State Filter" section is useful if you are working with an existing resource file. You can uncheck "Translated" to hide all the strings that were already translated.
- To translate a string, simple type your translation in the "Translation" box.
- A strings state will automatically switch to the "Translated" state when you type a translation into the translation section.

### Different States

- "Need Review" means a string was translated but the source string from en-US source was changed.
- "New" means a string was not yet translated.
- "Translated" is when has string has been translated. 
- "Source" shows the original text of the string. 

### Saving your changes
- Save your changes in Visual Studio and push them to your fork on GitHub.
- Create a pull request and someone will review it.
- Before submitting the pull request, check that `Files.[language_code].xlf` was the only modified file. If you added a new localization, then make sure the `cproj` file was modified as well with the path to the new resource file.
