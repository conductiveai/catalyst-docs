---
title: Sending Quest Events in Catalyst
route: /quest-events-catalyst
tags: ['quests', 'events', 'achievements']
layout: default
order: 11
date: 2023-12-20
---
# Sending Quest Events in Catalyst

The Conductive Catalyst SDK is designed with an easy to use and flexible quest system. Developers can use methods in our SDK to track different types of in game events and reward users for their progress.

!!! :warning:
In order to effectively use the features of Catalyst, it is important to identify your complete the [Unity SDK integration](https://catalyst.conductive.ai/catalyst-unity-sdk/) and use your unique `API_KEY`.
!!!

## AdView
This method is used to track with a player views an advertisment in your game. For richer data, you can pass an id for the ad as a parameter.

### Example Usage
```csharp
CatalystSDK.Instance.AdView(string id);
```
### Best Practices
Place this method in your game when a new advertisement is shown to a player.

## LootboxOpen

This method is used to track when a player opens a lootbox or triggers a gatcha action. For richer data, you have the option to pass the type of lootbox opened and the reward the player received from the lootbox.

### Example Usage
```csharp
CatalystSDK.Instance.LootboxOpen(string lootboxType, string reward);
```
### Best Practices
Place this method in your game when a player opens a lootbox.

## UserPurchase

This method is used to track in-app purchase (IAP) spend for a player and create quests with rewards after a player reaches a spend threshold. You can pass the amount a user spent as an integer. The name of the item purchased is an optional parameter.

### Example Usage
```csharp
CatalystSDK.Instance.UserPurchase(int userSpend, string itemPurchased);
```
### Best Practices
Place this method in your game when a player completes purchases of an item from an app store.

## CurrencySpend

This method is used to track when a player spends standard or soft currency. You can pass the amount of currency used. The name of the currency is an optional parameter.

### Example Usage
```csharp
CatalystSDK.Instance.CurrencySpend(int amount);
```
### Best Practices
Place this method in your game when a player spends soft currency.

## PremiumCurrencySpend

This method is used to track when a player spends premium currency. You can pass the amount of premium currency used. The name of the premium currency is an optional parameter.

### Example Usage
```csharp
CatalystSDK.Instance.PremiumCurrencySpend(int amount);
```
### Best Practices
Place this method in your game when a player spends premium currency.

## LevelEvent

This method is used to track when a player level increases in a game. It can also be used to track overall player progress in a stage or level based game.

### Example Usage
```csharp
CatalystSDK.Instance.LevelEvent();
```
### Best Practices
Place this method in your game when a player completes a level or increases their player level.

## ScoreEvent

This method is used to track the quantity of points a player earned. ScoreEvent quests are completed when a player reaches a cumulative score. You can pass the points a player earned. The type of score or level where the score is earned can be passed as an optional parameter.

### Example Usage
```csharp
CatalystSDK.Instance.ScoreEvent(int score, string scoreType);
```
### Best Practices
Place this method in your game when a player's score is recorded. We recommend sending the score at the total score at the end of a level or session.

## AchievementComplete

This method is used to track when a player completes an achievement on Game Center or Google Play. You can pass the name of the acheivement as a parameter.

### Example Usage
```csharp
CatalystSDK.Instance.AchievementComplete(string achievementName);
```
### Best Practices
Place this method in your achievement manager script or when a player completes an achievement.

### QuestEvent

This method allows developers to create custom events and create custom quests. You can pass the event name for the quest to track, an optional integer, and a key value pair array to add additional data.

#### Example Usage
```csharp
CatalystSDK.Instance.QuestEvent(string eventName, int? value, params KeyValuePair<string, object>[] eventData);
```

Creating custom quests is a way to deeply integrate the Conductive Catalyst SDK for your game and improve player LTV based on your game's unique loop. Custom quests can be easily created with one line of code like this:

#### Example Usage
```csharp
CatalystSDK.Instance.QuestEvent("MyCustomQuest");
```