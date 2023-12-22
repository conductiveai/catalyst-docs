---
title: SDK Events Examples
route: /sdk-events-examples
tags: ['examples', 'sdk', 'unity', 'custom']
layout: default
order: 9
date: 2023-08-02
---
# Event example

### Manually capturing events

Here's an example code snippet that shows how to use the `CatalystSDK` in your game's code

```csharp
public class GameClassSomething : MonoSingleton {
  private int Coin;

  public void Start() {
    CatalystSDK.Instance.ScreenView("Game");
  }

  public void IncreaseCoin(int incCoin) {
    Coin += incCoin;

    CatalystSDK.Instance.Capture("IncreaseCoin", new Dictionary<string, object>{{ "coins", Coin }});
  }

  public void DecreaseCoin(int incCoin) {
    Coin -= incCoin;

    CatalystSDK.Instance.Capture("DecreaseCoin", new Dictionary<string, object>{{ "coins", Coin }});
  }

  public void Login(string email, int age, string name) {
    CatalystSDK.Instance.Identify(email, new Dictionary<string, object>{
      { "age", age },
      { "email": email },
      { "name": name }
    });
  }
}
```