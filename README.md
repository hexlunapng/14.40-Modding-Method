# 14.40-Modding-Method
# For starters, you need multiple things.
1. Working Modding Project, use 14.30 uproject as a base (Cannot have cook errors). Will be open-sourcing one soon!
2. 14.40 Engine, fully compiled.
3. Some Method of packaging (Mine is VIA cmd)
# How to get Started
# Step 1.
Compile your uproject, for your 14.40 engine.
Add this asset to your Engine to fix issues
\Engine\Content\Functions\Engine_MaterialFunctions02\WorldPositionOffset\ObjectPivotPoint.uasset
ObjectPivotPoint.uasset.
You may need to fix issues with C++ code, isn't too hard.
# Step 2.
Once you are in the Uproject, set up your never cook list, you can't have any engine files or assets that are in the game. Only the assets you modify should be cooked.
Check if you have any cook errors by running a quick cook.
If you don't have cook errors, you can move onto the next step.
If you have cook errors, spend the time to fix them.
Unreal forums will be your best friend for this.
# Step 3.
Once you have 0 cook errors, you must setup chunk ids.
There is an experiment, but it is a scuffed way to do it.
Enable chunk ID assignments in Editor preferences, and set your chunk id for each asset.
There is a way to do it automatically, too much to explain, will be in the uproject I post.
# Step 4.
You can finally package now, if you get any issues you need to fix them.
For me the easiest way to package is via cmd.
Here is the cmd I use, just change the paths
"C:\14.40\Engine\Build\BatchFiles\RunUAT.bat BuildCookRun -project="C:\FNGameProj-Wesley\FortniteGame.uproject" -noP4 -platform=Win64 -clientconfig=Development -cook -allmaps -build -stage -pak -archive -archivedirectory="D:\OGFN\Paks" -compressed -iostore -generatechunks""
# Step 5.
Once it is done packaging, you can now put the utoc and ucas in your build. Take a sig from the build, NOT THE ONE UE PRODUCES. 
You will need a packer, like unreal pak.
Drop your asset reg into the pak, with the GUID.
Package it, then put it with your utoc and ucas.
This is about all you need to do tbh. If you get any issues, it will probably be fixed in my uproject.


# Credits to The Solaris team for the method
