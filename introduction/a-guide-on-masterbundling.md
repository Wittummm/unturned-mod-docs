---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# A Guide on Masterbundling

## Setting up Your Mod Folder(in Unity)

Create a folder in Unity for all your mod's files to go in. In this example in Assets/MyMods/TestMod/TestModBundles

## Asset Label

By default, the inspector window should be opened on the right side. If not, go to the menu bar and click **Window** > **General** > **Inspector**.\
Navigate to the parent of your mod folder (in this case **MyMods**) and select your mod(**TestMod**) folder. Open the dropdown in **Asset Labels** and select **New...** Pick your desired bundle name suffixed with “.masterbundle”(mine will be testmodbundles.masterbundle). The name cannot contain spaces, underscores/dashes, capital letters, or special characters.

## Setting up folders for export

Create a folder to export your assets into. This is also where your .dat and .asset files will be. If you're doing this for a map, it must be in the **Bundles** folder. Here you will create a file named **MasterBundle.dat**. If you haven't already, enable file name extensions to allow you to create the file easier. Note that the extensions must be correct or else Unturned wont recognize it(.txt does not work).

## Examples

{% code title="MasterBundle.dat" %}
```
Asset_Bundle_Name testmodbundles.masterbundle 
// the directory in unity of everything before the bundle
Asset_Prefix Assets/MyMods/TestMod/TestModBundles
// 2021 -> 5 | 2020 -> 4 | 2019/2018.4 -> 3 | 2017.4 -> 2 | 5.5 -> 1
Asset_Bundle_Version 5
```
{% endcode %}

## Masterbundling

Open the master bundling tool via **Window** > **Unturned** > **Master Bundle Tool**. Expand the Asset Bundle and check your label(in this case testmodbundles.masterbundle). Expand the master bundle click the “…” and select your folder(in this case …/Maps/DemoMap/Bundles/TestMod). You can optionally check the multi-platform for the published version of the mod, for testing purposes it does not need to be checked.

**Your file structure should look something like this:**

```
.../Test map/Bundles
    MasterBundle.dat
    testmodbundles.masterbundle
    (other files are omitted form here to reduce confusion just ignore them)
    (...)
    Objects/Large/MyFirstBuilding (Has to match directly 1:1 with Unity hierachy)
        MyFirstBuilding.dat
        English.dat
```

All you need to do now is move MyFirstBuilding.dat and English.dat into the MyFirstBuilding folder like shown above.

Launch Unturned and go into the map and place your first building in! If it does not work be sure to check Workshop -> Error Logs.&#x20;

***

(Proofread: 2024/04/30)\
Sources:\
[A Steam guide on MasterBundling](https://steamcommunity.com/sharedfiles/filedetails/?id=2976338845)
