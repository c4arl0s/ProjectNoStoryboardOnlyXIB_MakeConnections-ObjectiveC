# ProjectNoStoryboardOnlyXIB_MakeConnections-ObjectiveC
ProjectNoStoryboardOnlyXIB_MakeConnections-ObjectiveC

# In  this case you just delete the main storyboard and then you kept the Viewcontroller class, you have to add a new xib file view and make the connections.

# How does AppDelegate.h looks like ?

``` objective-c
//
//  AppDelegate.h
//  ProjectOnlyXIB_MakeConnections
//
//  Created by Carlos Santiago Cruz on 4/27/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import <UIKit/UIKit.h>

@interface AppDelegate : UIResponder <UIApplicationDelegate>

@property (strong, nonatomic) UIWindow *window;


@end
```

# How does AppDelegate.m looks like ?

``` objective-c
//
//  AppDelegate.m
//  ProjectOnlyXIB_MakeConnections
//
//  Created by Carlos Santiago Cruz on 4/27/19.
//  Copyright © 2019 Carlos Santiago Cruz. All rights reserved.
//

#import "AppDelegate.h"
#import "ViewController.h"

@interface AppDelegate ()
{
    ViewController *viewController;
}
@end

@implementation AppDelegate


- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    self.window = [[UIWindow alloc] initWithFrame:[UIScreen mainScreen].bounds];
    // Remember: You delete the storyboard, and you keep the ViewController class.
    // other case is when you add a new file, add a ViewController subclass of UIController and add the xib file. In this case you don`t have to make the connections.
    // Remember, after instanciate the class, you have to go to xib file and make the connections.
    viewController = [[ViewController alloc] initWithNibName:@"ViewController" bundle:nil];
    self.window.rootViewController = viewController;
    [self.window makeKeyAndVisible];
    return YES;
}


- (void)applicationWillResignActive:(UIApplication *)application {
    // Sent when the application is about to move from active to inactive state. This can occur for certain types of temporary interruptions (such as an incoming phone call or SMS message) or when the user quits the application and it begins the transition to the background state.
    // Use this method to pause ongoing tasks, disable timers, and invalidate graphics rendering callbacks. Games should use this method to pause the game.
}


- (void)applicationDidEnterBackground:(UIApplication *)application {
    // Use this method to release shared resources, save user data, invalidate timers, and store enough application state information to restore your application to its current state in case it is terminated later.
    // If your application supports background execution, this method is called instead of applicationWillTerminate: when the user quits.
}


- (void)applicationWillEnterForeground:(UIApplication *)application {
    // Called as part of the transition from the background to the active state; here you can undo many of the changes made on entering the background.
}


- (void)applicationDidBecomeActive:(UIApplication *)application {
    // Restart any tasks that were paused (or not yet started) while the application was inactive. If the application was previously in the background, optionally refresh the user interface.
}


- (void)applicationWillTerminate:(UIApplication *)application {
    // Called when the application is about to terminate. Save data if appropriate. See also applicationDidEnterBackground:.
}


@end
```

![Captura de Pantalla 2019-04-27 a la(s) 11 17 40](https://user-images.githubusercontent.com/24994818/56852450-e96d7480-68d8-11e9-81b6-a9c38934a831.png)

![Captura de Pantalla 2019-04-27 a la(s) 11 18 24](https://user-images.githubusercontent.com/24994818/56852467-13269b80-68d9-11e9-9c66-5e7c12e2ba99.png)

![Captura de Pantalla 2019-04-27 a la(s) 11 25 19](https://user-images.githubusercontent.com/24994818/56852470-1a4da980-68d9-11e9-8669-d700002b1cc1.png)

![Captura de Pantalla 2019-04-27 a la(s) 11 43 24](https://user-images.githubusercontent.com/24994818/56852545-efb02080-68d9-11e9-92f7-070537004946.png)




