## Part 2: CocoaPods

**CocoaPods** is a dependency manager for Swift and Objective-C Cocoa projects. It has over 24 thousand libraries and is used in over 1.2 million apps. You can learn more on the [CocoaPods website](https://cocoapods.org/).

If you have not already done so, you should go ahead and install Cocoapods. The process is very simple. First, open a Terminal and run this command `sudo gem install cocoapods`. To complete the setup enter this command: `pod setup --verbose`. Great, you're now set up to use CocoaPods!

### Installing our Pods

For our Weather App, we will be using two third-party libraries: Alamofire and SwiftyJSON. We will be using Alamofire to handle networking in our app, and we will be using SwiftyJSON to parse the JSON data obtained from the DarkSky API. To install our pods, we need to initialize our Podfile. Open up your terminal and CD to the directory where you created your Xcode project. Once you're there, run this command: `pod init`. This command will create a Podfile for your project. Type this command to open the Podfile using Xcode for editing: `open -a Xcode Podfile`.

When your Podfile is opened, it should look something like this:

<p align="center"> <img src="/images/Podfile.png" align="center"> </p>

Go ahead and uncomment these two lines: `# platform :ios, '8.0'` and `# use_frameworks!`. Now change the platform from iOS 8 to iOS 10. To use Alamofire and SwiftyJSON we need to add two lines to our Podfile between `target 'Weather App' do` and `end`. If you take a look at the Github repos for these libraries, you'll see that these are the lines we need to add: `pod 'Alamofire', '~> 4.0'` and `pod 'SwiftJSON'`. When you're done your Podfile will now look like this:

<p align="center"> <img src="/images/podfileWithPods.png" align="center"> </p>

To finish setting up our pods we have to do one more thing. Go back to the terminal where you initialized your Podfile. Don't worry if you closed it. Just open a new terminal and CD to your Xcode project directory. Once you're there, run this command: `pod install`. This command will install the dependencies for your project. Once this process is done, we'll be ready to start working on our app!

### Next Time

Now that we have our pods set up, we will start creating the interface for our Weather App!
