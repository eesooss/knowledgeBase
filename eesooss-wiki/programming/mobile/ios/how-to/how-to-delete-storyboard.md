# How To Delete Storyboard

1. Delete files (SceneDelegate, Main.storyboard)
2. Delete entries in Info.plist (Application Scene Manifest)
3. Rewrite AppDelegate:

```swift
var window: UIWindow?
    
func application(
				 _ application: UIApplication, 
				 didFinishLaunchingWithOptions launchOptions: 
				 [UIApplication.LaunchOptionsKey: Any]?
				 ) -> Bool 
{
    window = UIWindow(frame: UIScreen.main.bounds)
    window?.makeKeyAndVisible()
    window?.backgroundColor = .systemBackground
    window?.rootViewController = ViewController()
        
    return true
}
```
