# New page!

Early mornings are chilly in Los Romero, a village high up in the mountains of western Guatemala. As in other predominantly Mam villages – Indigenous Maya people who have lived here since pre-Columbian times – households come quietly to life before dawn. Isabel Romero, a grandmother with long black hair, used to feel somewhat trapped in hers.

“I was afraid of speaking because I was cooped up at home. I didn’t go out,” she says, explaining that like many Mam women, her days were dedicated to the hard work of running a household with little money, and she rarely spoke with other women. “I worried a lot and had headaches.”

Residents of Los Romero live mainly from subsistence farming, growing maize, beans and squash, or grazing livestock. Almost 50% of the population is Indigenous in Guatemala, Central America’s biggest economy, but they do not share in its prosperity. Indigenous women in particular are discriminated against and dispossessed, with a life expectancy 13 years lower, and a maternal mortality rate two times higher, than the national average, according to the World Bank.

1. wsa\
   ![](<.gitbook/assets/CleanShot 2024-02-29 at 19.08.35@2x.png>)
2.
3.
4.
5.

Initialize Netmera

1. Navigate to iOS folder in your terminal and run the following command.

```
$ pod install
```

2. If you want to use Android alike message sending from iOS to react native please consider shaping your AppDelegate class as following.

```objectivec
#import <React/RCTBridgeDelegate.h>
#import <UIKit/UIKit.h>
#import <Netmera/Netmera.h>
#import <NetmeraCore/NetmeraPushObject.h>
#import <UserNotifications/UserNotifications.h>

@interface AppDelegate : UIResponder <UIApplicationDelegate, RCTBridgeDelegate, UNUserNotificationCenterDelegate, NetmeraPushDelegate>

@property (nonatomic, strong) UIWindow *window;

@end
```

```objectivec
#import "AppDelegate.h"

#import <RNNetmera/RNNetmeraRCTEventEmitter.h>
#import <RNNetmera/RNNetmeraUtils.h>
#import <RNNetmera/RNNetmera.h>

@implementation AppDelegate

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{

  // Add these lines to init Netmera
  [RNNetmera logging: YES]; // This is for enabling Netmera logs.
  [RNNetmera initNetmera:[<YOUR NETMERA API KEY>]]; // Replace this with your own NETMERA API KEY.
  [RNNetmera requestPushNotificationAuthorization];
  [RNNetmera setPushDelegate:self];
  [Netmera setAppGroupName:<YOUR APP GROUP NAME>]; // Set your app group name

  return YES;
}

// Take push payload for Push clicked:
-(void)userNotificationCenter:(UNUserNotificationCenter *)center didReceiveNotificationResponse:(UNNotificationResponse *)response withCompletionHandler:(void (^)(void))completionHandler
{
  if ([response.actionIdentifier isEqual:UNNotificationDismissActionIdentifier]) {
    [RNNetmeraRCTEventEmitter onPushDismiss: @{@"userInfo" : response.notification.request.content.userInfo}];
  } else if ([response.actionIdentifier isEqual:UNNotificationDefaultActionIdentifier]) {
    [RNNetmeraRCTEventEmitter onPushOpen: @{@"userInfo" : response.notification.request.content.userInfo}];
  }
  completionHandler();
}

// Take push payload for push Received on application foreground:
-(void)userNotificationCenter:(UNUserNotificationCenter *)center willPresentNotification:(UNNotification *)notification withCompletionHandler:(void (^)(UNNotificationPresentationOptions))completionHandler
{
  completionHandler(UNNotificationPresentationOptionAlert);
  [RNNetmeraRCTEventEmitter onPushReceive: @{@"userInfo" : notification.request.content.userInfo}];
}

- (void)application:(UIApplication *)application didRegisterForRemoteNotificationsWithDeviceToken:(NSData *)deviceToken
{
  if(deviceToken == nil) {
    return;
  }
  [RNNetmeraRCTEventEmitter onPushRegister: @{@"pushToken" : deviceToken}];
}

@end
```

For instance, if you trigger `[RNNetmeraRCTEventEmitter onPushReceive: @{@"userInfo" : notification.request.content.userInfo}]` from `AppDelegate` the following method will be triggered in the react native part.

```objectivec
export const onPushReceive = async (message) => {
    console.log("onPushReceive: ", message);
};
```

{% hint style="danger" %}
**Please make sure you get the API key value from the relevant panel**

YOUR\_SDK\_API\_KEY: You can get the api key from **Developers > API > SDK API Key** from your Netmera Panel.
{% endhint %}

### Request Push Notification Authorization <a href="#request-push-notification-authorization" id="request-push-notification-authorization"></a>

Request push notification authorization from user by calling the following method in an appropriate place.

```javascript
if (Platform.OS === "ios"){
     Netmera.requestPushNotificationAuthorization()
}
```

### Using iOS10 Media Push <a href="#using-ios10-media-push" id="using-ios10-media-push"></a>

Rich Media Integration for Versions 3.14.4 and higher. Please see the following documentation to see how to integrate iOS Media Push on [Broken link](broken-reference "mention").

### Podfile Configuration <a href="#podfile-configuration" id="podfile-configuration"></a>

```
pod "Netmera", "3.14.10-WithoutDependency"
pod "Netmera/NotificationServiceExtension", "3.14.10-WithoutDependency"
pod "Netmera/NotificationContentExtension", "3.14.10-WithoutDependency
```

However, you need to add these pods outside of your target in Podfile as in the following document.

{% embed url="https://github.com/Netmera/Netmera-React-Native-Example/blob/master/ios/Podfile" %}

## <mark style="color:green;">Step 3: Setup / Android</mark> <a href="#setup-android-part" id="setup-android-part"></a>

### Create Firebase Cloud Messaging Configuration <a href="#create-firebase-cloud-messaging-configuration" id="create-firebase-cloud-messaging-configuration"></a>

This section provides information about the basic steps required in order to be able to receive push notifications sent from Netme\


```
// Some code
```



* one
* two
* three

|       |      |      |
| ----- | ---- | ---- |
| hello |      |      |
|       | font |      |
|       |      | done |
