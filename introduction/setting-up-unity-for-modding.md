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

Modding Unturned requires using Unity. Most 2021.3 LTS version should be compatible; Unturned currently uses 2021.3.29f1 (as of 2024/4/23).

Once you install Unity, create a project to store your mods.

### Unity Packages

Unturned provides multiple Unity packages. These packages include examples that can be referenced when creating custom content, and provide the tools necessary to export content from Unity.

1. Open your Unity project.
2. Select **Assets > Import Package > Custom Package…** from the toolbar.
3. In the file browser, navigate to the `.../Unturned/Extras/Sources` directory.
4. Import the `Project.unitypackage` and `ExampleAssets.unitypackage`&#x20;

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

***

(Proofread: 2024/04/23)\
Sources: [Source: Official documentation](https://docs.smartlydressedgames.com/en/stable/about/getting-started.html)
