---
title: Getting started
route: /quick-start
tags: ['getting started', 'quick', 'installation']
layout: default
order: 8
date: 2023-08-02
---

If you want to integrate **ConductiveUnitySDK** into your Unity game development project, this step-by-step guide will help you install the package into Unity.

### Installation Guide

You can follow our [quick installation guide in our public Github repository](https://github.com/conductiveai/conductive-unity-sdk), or continue following the instructions below.

### Requirements

- Unity 2018 or later installed on your computer
- Internet connection
- GitHub account

### API Key

You will first want to acquire an API key by visiting the dashboard https://app.conductive.ai and selecting the settings icon at the bottom and then “Settings”

![](https://github.com/conductiveai/conductive-unity-sdk/blob/main/.github/settings.png?raw=true)

This should take you to the project settings below, copy your API key provided for your project.

![](https://github.com/conductiveai/conductive-unity-sdk/blob/main/.github/settings2.png?raw=true)

### Installing the Unity SDK

1. In Unity, go to **Window > Package Manager**
2. Using the GitHub:
    - In the ➕ button, go to **Add package from git URL**
    - And paste https://github.com/conductiveai/conductive-unity-sdk.git and click **Add**
3. Using the ZIP file:
    1. Go to [https://github.com/conductiveai/conductive-unity-sdk](https://github.com/conductiveai/conductive-unity-sdk.git) and [download the zip file](https://github.com/conductiveai/conductive-unity-sdk/archive/refs/heads/main.zip)
    2. In the ➕ button, go to **Add package from disk**
    3. Select the zip file, that you download from GitHub.

![](https://github.com/conductiveai/conductive-unity-sdk/blob/main/.github/step1.png?raw=true)

![](https://github.com/conductiveai/conductive-unity-sdk/blob/main/.github/step2.png?raw=true)

![](https://github.com/conductiveai/conductive-unity-sdk/blob/main/.github/step3.png?raw=true)

## Integration in Unity

1. In packages list, go to go to **Packages > ConductiveUnitySdk > Prefab**
2. Drag ConductiveSDK prefab to your project's loading scene or first scene
    
    ![](https://github.com/conductiveai/conductive-unity-sdk/blob/main/.github/add-game-object.png?raw=true)
    
3. Fill in the `API_KEY` field in the ConductiveSDK prefab using the api key you acquired earlier.

### That’s it! 🚀

The Conductive SDK will capture user login events automatically.

No additional code needed! Placing the prefab in the game's first loaded scene or Main Menu ensures user logins are captured when the game starts.