## My snippets

- Marks
```swift
// MARK: - Layout
// MARK: - Public/Private Methods
// MARK: - Public/Private Properties
// MARK: - Creating Subviews
// MARK: - Initilization
```
- SUI

Preview canvas simulator from SwiftUI:

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
                                    context: UIViewControllerRepresentableContext<Containter>) {
        }
    }
}
```

Disabling Storyboard layout:

```swift
import UIKit

class SceneDelegate: UIResponder, UIWindowSceneDelegate {
    
    var window: UIWindow?
    
    func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
        guard let windowScene = (scene as? UIWindowScene) else { return }
        
        window = UIWindow(windowScene: windowScene)
        window?.rootViewController = <#YourRootViewController#>
        window?.overrideUserInterfaceStyle = .light
        window?.makeKeyAndVisible()
    }
}
```

---
## Sources

- [How to create code snippets in Xcode](https://sarunw.com/posts/how-to-create-code-snippets-in-xcode/)