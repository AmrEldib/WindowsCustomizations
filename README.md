# Windows Customizations

This is a repository of registry entries to customize Windows.  

## Naming
Some rules for including entries to keep things organized:  
- Each entry should do one thing, as much as possible.  
- Each entry to add something should have an entry to remove that thing.  
- Include the source of where you found this information.  
- Entries should be named to allow for easy sorting.  
Example:  
```
This PC - User Folders - Add - 3D-Objects.reg
```
The name is clear, but it also makes for easy sort.  
`This PC` is a category. `User Folders` is one item under this category, other items could be added later.  
`Add` indicates that this entry will enable this feature. `3D-Objects` is the feature to be enabled.  
Words in the name are spaced out and delimited to allow for easy reading in a long list.  
All this enables discovery.  

## Run
To quickly import entries that you've specified. Run the PowerShell script named `_ImportMyCustomizations.ps1`  
Entries to import must be listed in a file named `_MyCustomizations.txt`  
To easily create this file, in the command line use:  
```cmd
dir *.reg /b > _MyCustomizations.txt
```
Or, in PowerShell
```powershell
Get-ChildItem *.reg | Select-Object -ExpandProperty Name > _MyCustomizations.txt
```
Then, remove all the additional entries you don't need.