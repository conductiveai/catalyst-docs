---
title: Sending Events in Catalyst
route: /sending-events-in-catalyst
tags: ['events', 'analytics', 'capture', 'identity']
layout: default
order: 5
date: 2023-08-02
---
# Sending events

By default, adding your `API_KEY` will automatically send a registration event to Catalyst’s backend so we know you use exists and logged into your application.

<aside>
⚠️ In order to effectively use the features of Catalyst though, it is important you identify you user using `CatalystSDK.identify()` and identify them using your own internal user ID. This will be vital when integrating additional features.

</aside>

### Identify

Identify a user with your application/games unique internal ID instead of a Catalyst. If not provided, Catalyst will generate a random but unique identifier. If this method is never called, then unique visitors will be identified by a randomly generated UUID generated the first time they launch your application.

```csharp
CatalystSDK.Instance.Identify("USER_UNIQUE_ID", new Dictionary<string, object>{
    { "age", Age },
    { "email": Email },
    { "name": Name }
});
```

Ideally, you should only capture this once. For example, once a user successfully registered and verifies their email address, you can fire this event once.

If you can’t avoid firing this frequently (like at app cold launch), then it is ok. We will still track the user for you.

### Custom Capture

Captures a custom event. This Catalyst function allows you to capture additional events in the game. You do not need to use Capture to capture daily logins as we will do this for you.

At a high-level, this is useful if you wish to build user funnels and understand the effectiveness of a feature. Parameters are provided if you wish to capture additional metadata about the event.

```csharp
CatalystSDK.Instance.Capture("ACTION", new Dictionary<string, object>{
    { "param1", Param1 },
    { "param2", Param2 },
    { "param3", Param3 },
    { "param4", Param4 }
});
```

Suggestions on how to use this:

- When a user engages with the feature like `PLAY_LEVEL`
- When a user achieves a result like `WIN_LEVEL`
    - Parameters could include the level played, XP earned, etc.
- When a user attempts to make a purchase and when the purchase is successful

In general it is important to capture key events around Monetization and Engagement using the `Capture` method. The `PageView` method will help you capture Retention metrics/KPIs. This will be ultimately useful for tracking LTV.

### Alias

Create an alias, which Catalyst will use to link two user ID’s going forward (not retroactively). Multiple aliases can map to the same USER_UNIQUE_ID, but not vice-versa.

```csharp
CatalystSDK.Instance.Alias("USER_UNIQUE_ID", "ALIAS_ID");
```

The context for using this is if you user has multiple identifiers you wish to leverage later for analytics or Catalyst feature purposes. For example, once you’ve used the `Identify()` method, you later might capture a user’s Twitter handle. If you wish to track this later, simply provide their unique user ID you used for `Identify()` as the first parameter, and the secondary identifier in the second parameter.

Like `Identify()`, this only needs to be fired once.

### ScreenView

This method to track when the user views a specific screen in your game. You can pass additional properties you wish to use later.

```csharp
CatalystUnitySDK.Instance.ScreenView("SCREEN_NAME", new Dictionary<string, object>{
    { "param1", Param1 },
    { "param2", Param2 },
    { "param3", Param3 },
    { "param4", Param4 }
});
```

It is extremely helpful to track screens because it allows us to track user retention for you as well as user LTV.