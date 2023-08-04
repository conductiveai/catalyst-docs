---
title: Troubleshooting the SDK
route: /troubleshooting-the-sdk
tags: ['help', 'error', 'issues', 'troubleshooting']
layout: default
order: 3
date: 2023-08-02
---

# Mac M1

## **Building for iOS / XCode**

If you receive a CocoaPods error such as: `...ruby/2.6.0/gems/ffi-1.15.5/lib/ffi_c.bundle' (mach-o file, but is an incompatible architecture (have 'arm64', need 'x86_64')),`
This means you have `ffi` built for `arm64` but not `x86_64` architecture.
Make sure you have Developer Mode enabled on your iOS device: `Settings → Privacy → Developer mode → on`
Then, do the following:

(1) Install llvm:
```
arch -arm64 brew install llvm
export LDFLAGS="-L/opt/homebrew/opt/llvm/lib"
export CPPFLAGS="-I/opt/homebrew/opt/llvm/include"
```
(2) Uninstall ffi:
```
sudo gem uninstall ffi
```

(3) If prompted, uninstall ALL versions. install ffi gem for x86_64:
```
sudo arch -x86_64 gem install ffi`
```

- Reference: https://stackoverflow.com/questions/66644365/cocoapods-on-m1-apple-silicon-fails-with-ffi-wrong-architecture

## Issues building for iOS

- Be sure to disable `bitcode`
- Be sure to remove `Quoted Include` in Framework Header to no