```swift
for family in UIFont.familyNames {
    print("\(family)")

    for name in UIFont.fontNames(forFamilyName: family) {
        print("\(name)")
    }
}
```

- [Building a Design System for iOS - Typography](https://www.ramshandilya.com/blog/design-system-typography/)