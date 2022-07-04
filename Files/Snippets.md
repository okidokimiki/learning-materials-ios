# My snippets

`⌘` + `⇧ Shift` + `L`

## Marks
```swift
// MARK: - Public/Private/Override Properties
// MARK: - Public/Private/Override Methods
// MARK: - Creating Subviews
// MARK: - Initilization
// MARK: - Layout
```
## SUI

- SUIPreview: preview canvas simulator from SwiftUI:

```swift
import SwiftUI

// MARK: - SUIPreview

struct FlowProvider: PreviewProvider {
    static var previews: some View {
        SUIContainterView().edgesIgnoringSafeArea(.all)
    }
    
    struct SUIContainterView: UIViewControllerRepresentable {
        typealias Containter = FlowProvider.SUIContainterView
        
        func makeUIViewController(context: UIViewControllerRepresentableContext<Containter>) -> <#YourViewController#> {
            
            return <#YourViewController()#>
        }
        
        func updateUIViewController(_ uiViewController: Containter.UIViewControllerType,
                                    context: UIViewControllerRepresentableContext<Containter>) { }
    }
}
```

## UIKit

- CastView: casting View of ViewController to customView

```swift
private var <#viewName#>: <#ViewClass#> {
    guard let castedView = view as? <#ViewClass#> else {
        fatalError("TypeCasting Error: presenterView must be \(<#ViewClass#>.self)")
    }

    return castedView
}
```

- Disabling Storyboard layout:

```swift
import UIKit

class SceneDelegate: UIResponder, UIWindowSceneDelegate {
    
    var window: UIWindow?
    
    func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
        guard let windowScene = (scene as? UIWindowScene) else { return }
        
        window = UIWindow(windowScene: windowScene)
        window?.rootViewController = <#YourRootViewController#>
        window?.makeKeyAndVisible()
    }
}
```

# Sources

- [sarunw.com: How to create code snippets in Xcode](https://sarunw.com/posts/how-to-create-code-snippets-in-xcode/)