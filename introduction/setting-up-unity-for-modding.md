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

# Setting up Unity for modding

## Getting Started

Installing the Unity Editor is required for exporting custom content into Unturned. Most 2021.3 LTS version should be compatible; Unturned currently uses 2021.3.29f1 (as of 2024/4/23).

Once Unity is installed, a project can be created for your mods. At this point, it is recommended to import Unturned’s provided Unity packages.

### Unity Packages

Unturned provides multiple Unity packages with the base installation of the game. These packages include examples that can be referenced when creating custom content, and provide the tools necessary to export content from Unity.

These Unity packages are located in the `.../Unturned/Extras/Sources` directory, and are regularly updated alongside any major updates to the game. You may want to occasionally reimport these packages.

1. Open your Unity project.
2. Select **Assets > Import Package > Custom Package…** from the toolbar.
3. In the file browser, navigate to the `.../Unturned/Extras/Sources` directory.
4. Import the `Project.unitypackage` file; importing the `ExampleAssets.unitypackage` file is optional.

#### Project.unitypackage

This package contains the bare-bones required to export custom content:

* Default Project Settings
* [Asset Bundling Tools](https://docs.smartlydressedgames.com/en/stable/assets/asset-bundles.html#doc-asset-bundles)
* [Mod Hooks](https://docs.smartlydressedgames.com/en/stable/assets/mod-hooks.html#doc-assets-mod-hooks) (optional)

#### ExampleAssets.unitypackage

This package contains vanilla content examples, and several useful prefabs:

* `CoreMasterBundle` directory has an example of each type of vanilla asset.
* `Game/Sources/Animations` directory has all of the vanilla item animations.
* `Resources/Characters/Preview.prefab` is helpful for previewing clothes.

{% hint style="warning" %}
Warning

Custom content should not be placed into the CoreMasterBundle directory. Instead, create a separate directory to house your custom content.
{% endhint %}

(Proofread: 2024/04/23)
Sources:
[Source: Official documentation](https://docs.smartlydressedgames.com/en/stable/about/getting-started.html)
