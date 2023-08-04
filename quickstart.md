---
title: Getting Started
route: /quick-start
tags: ['getting started', 'quick', 'installation']
layout: default
order: 8
date: 2023-08-02
---

If you want to integrate **CatalystSDK** into your Unity game development project, this step-by-step guide will help you install the package into Unity.

### Installation Guide

You can follow our [quick installation guide in our public Github repository](https://github.com/conductiveai/catalyst-unity-sdk), or continue following the instructions below.

### Requirements

- Unity 2018 or later installed on your computer
- An internet connection
- A GitHub account

### API Key

You will first want to acquire an API key by visiting the dashboard <https://app.conductive.ai> and selecting the settings icon at the bottom, followed by “Settings”.

![](https://github.com/conductiveai/catalyst-unity-sdk/blob/main/.github/settings.png?raw=true)

This should take you to the project settings below. Copy your API key provided for your project.

![](https://github.com/conductiveai/catalyst-unity-sdk/blob/main/.github/settings2.png?raw=true)

### Installing the Unity SDK

1. In Unity, go to **Window > Package Manager**. You can install the SDK using either the GitHub URL or the ZIP file.
2. Using GitHub:
    - Click the ➕ button, then go to **Add package from git URL**.
    - Paste <https://github.com/conductiveai/catalyst-unity-sdk.git> and click **Add**.
3. Using the ZIP file:
    - Go to [https://github.com/conductiveai/catalyst-unity-sdk](https://github.com/conductiveai/catalyst-unity-sdk.git) and [download the zip file](https://github.com/conductiveai/catalyst-unity-sdk/archive/refs/heads/main.zip)
    - Unzip the file
    - Click the ➕ button, then go to **Add package from disk**.
    - Select the folder that you unzipped select the package.json file.

![](https://github.com/conductiveai/catalyst-unity-sdk/blob/main/.github/step1.png?raw=true)

![](https://github.com/conductiveai/catalyst-unity-sdk/blob/main/.github/step2.png?raw=true)

![](https://github.com/conductiveai/catalyst-unity-sdk/blob/main/.github/step3.png?raw=true)

## Integration in Unity

1. In the packages list, go to **Packages > CatalystSDK > Prefab**
2. Drag the *CatalystSDK.prefab* to your project's loading scene or first scene

    ![](https://github.com/conductiveai/catalyst-unity-sdk/blob/main/.github/add-game-object.png?raw=true)

3. Fill in the `API_KEY` field in the *CatalystSDK.prefab* using the API key you acquired earlier.

### That’s it! 🚀

The Catalyst SDK will automatically capture user login events automatically.

No additional code is required! Placing the prefab in the game's first loaded scene or Main Menu ensures user logins are captured when the game starts.
