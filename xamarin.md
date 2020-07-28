# Xamarin
### Fonts
In iOS you must add the font files to Resources and set the **Build Action** as  **BundleResource** then add an entry to to the file *Info.plist* under UIAppFonts .

In Android the font file needs to be in the **Assets** folder. To style the fonts of a control, add the font file in the Assets, and make sure the **Build Action** is set to **AndroidAsset**.

To Apply fonts use the following code 

    <OnPlatform x:TypeArguments="x:String">
    <On Platform="iOS" Value="Cairo" />
    <On Platform="Android" Value="Cairo.ttf#Cairo" />
    </OnPlatform>

in android after the hash (#Cairo) is the font name as seen when you open the fonts in windows Fonts.
