# My snippets

Show: `⌘` + `⇧ Shift` + `L`

Create: `Editor` -> `Create Code Snippet...`

## Marks
```swift
// MARK: - Private/Override Properties
// MARK: - Private/Override Methods
// MARK: - Creating Subviews
// MARK: - Initilization
// MARK: - AutoLayout
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
        
        func makeUIViewController(context: UIViewControllerRepresentableContext<Containter>) -> <#ViewController#> {
            
            return <#ViewController()#>
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
        fatalError("TypeCasting Error: view must be \(<#ViewClass#>.self)")
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
        window?.rootViewController = <#ViewController()#>
        window?.makeKeyAndVisible()
    }
}
```

# Sources

- [sarunw.com: How to create code snippets in Xcode](https://sarunw.com/posts/how-to-create-code-snippets-in-xcode/)
- [GitHub: Xcode MVP+C Templates](https://github.com/IrelDev/Xcode-MVP-C-Templates/blob/master/MVP-C%20Structure.xctemplate/___FILEBASENAME___Presenter.swift)