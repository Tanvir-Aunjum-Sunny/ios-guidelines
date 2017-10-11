# iOS Distribution Guidelines

## Testflight

Steps to walk a new internal tester through setting up TestFlight for beta app distribution. 

##### 1. Apple ID
In order to be added as a Tester, please send your Apple ID to rabin.joshi@nrccua.org asking to be added to iTunes Connect team. If you do not know your Apple ID you can find it from `Settings > iTunes & App Store`. If you're not signed in, or are signed in to a different account, please make sure that you are, and to the same account that you've mentioned in the email.

![Settings > iTunes & App Store 1](https://github.com/nrccua/testflight-distribution-guidelines-ios/blob/master/images/IMG_0074.PNG) ![Settings > iTunes & App Store 2](https://github.com/nrccua/testflight-distribution-guidelines-ios/blob/master/images/IMG_0075.PNG)

Please ensure that the email is a primary email for the Apple ID, with associated birthdate and the recovery emails. If this is not the case the folowing message is displayed when I attempt to add a new user: 
> This email address is not available for use as an Apple ID.
> You may already have an Apple ID associated with this address. 
> Please try again or sign in using your existing Apple ID.

##### 2. iTunes Connect

- You will recieve an invite from iTunes Connect with the subject `Welcome new iTunes Connect User`. Please tap `Activate your account`.

- That'll launch Safari and display the iTunes Connect `Terms of Service`.

- On tapping `Accept`. You'll be taken to Sign In Screen. Please verify that you can successfully Sign In.

![Welcome new iTunes Connect User](https://github.com/nrccua/testflight-distribution-guidelines-ios/blob/master/images/IMG_0072.PNG) ![Terms of Service](https://github.com/nrccua/testflight-distribution-guidelines-ios/blob/master/images/IMG_0073.PNG)


##### 3. TestFlight

- Install the `TestFlight` App from the App Store. You can find it by following [this link] (https://itunes.apple.com/us/app/testflight/id899247664?mt=8) or by searching for ‘testflight’ in the App Store. 

- Lauch TestFlight and accept the `Terms & Conditions`.

- Select `Allow Push Notifications`. Doing this will ensure that you’ll receive notifications every time a new version on the app is pushed.

![testflight](https://github.com/nrccua/testflight-distribution-guidelines-ios/blob/master/images/IMG_0076.PNG) ![TestFlight Terms and Conditions](https://github.com/nrccua/testflight-distribution-guidelines-ios/blob/master/images/IMG_0079.PNG) ![Allow Push Notifications](https://github.com/nrccua/testflight-distribution-guidelines-ios/blob/master/images/IMG_0080.PNG)


##### 4. Wait!

- Once you've completed all the steps above you're all set to recieve builds whenever a new one is posted.


##### 5. Installation

- When a new build is posted, you’ll receive an email notifying you of the new version of the app being available. You must open the email on your device.
<img>
- Tap `Start Testing` and `Accept` and `Install`. 
<img>
- The App will be downloaded with an orange mark next to its name to indicate a test build.


##### 6. Subsequent Builds

From this point on, whenever a new build is pushed to TestFlight you'll recieve an email (in addition to the push notification if you’ve chosen to receive them) like before. All you need to do now is Update your app and you'll have the latest version up and running. 


## Versioning

Apple specifies the following rules for valid version and build numbers in [Technical Note TN2420](https://developer.apple.com/library/content/technotes/tn2420/_index.html):

- The value for a version number or build number must consist only of '.'s and numbers and must begin and end with a number. 
- Each integer value separated by a period is a component of the version. Version numbers and build numbers may have up to three components separated by periods. 
- The total number of characters in your version number or in your build number cannot exceed eighteen characters.`

Apple doesn't define or require a specific convention for what eacr of the components in the version/build numbers are supposed to signify. In keeping with [semantic versioning](http://semver.org), here's what we do:

- Every new release will have a unique version number
- Versions numbers will be of the form `MAJOR.MINOR.PATCH`
- Significant and major releases will increment `MAJOR`
- Smaller releases introducing new features and UI changes will increment `MINOR`
- Bug Fixes and non-visual changes will increment `PATCH`


