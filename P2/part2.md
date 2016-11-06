## Part 2: Set up screen layout for Weather App

**Interface builder** is Xcode's GUI editor. For most projects, the interface is contained in the `Main.storyboard` file. Open it up and have a look around:

<p align="center"> <img src="/images/storyboardPic.png" align="center"> </p>

For this Weather app, there are 5 parts in the interface we're building:
1. A label to display the location
2. A label to display a description of the weather
3. A label to display the temperature
4. A label to display an icon
5. A bar button item to refresh the weather forecast

### Adding UI Elements

Embed the view controller in a Navigation Controller (select the view controller, Editor-> Embed in -> Navigation Controller), and add the 5 elements described above as well as the necessary constraints to your storyboard. You should have a result similar to this:

<p align="center"> <img src="/images/uiResult.png" align="center"> </p>

### WeatherViewController

In order to provide functionality to the app, there must be a way to connect the labels and bar button item to actual code. The view controller displayed in front of you is automatically connected to a file called `ViewController.swift`. We want a file with a more meaningful name, so you can go ahead and delete `ViewController.swift` and then create a new Swift file named `WeatherViewController.swift`. Make sure this new file is a subclass of `UIViewController`. Your new class should have the following code:

```swift
import UIKit

class WeatherViewController: UIViewController {

}
```

After your `WeatherViewController.swift` file is done, make sure your view controller is connected to this new file. To do this, go back to the storyboard and select the view controller. On the inspector pane to the right, select the identity inspector menu, and make sure the view controller's class is `WeatherViewController.swift`.

<p align="center"> <img src="/images/weatherVC.png" align="center"> </p>

### Label and Button Linking

Now, let's start with linking the labels and button in our view controller to the actual Swift code. In order to do this, we will use the usual control-click and drag method. Do this to link your labels as `IBOutlet`s and your button as an `IBAction`. Use the same variable/function names as in the code below:

```swift
class WeatherViewController: UIViewController {

    @IBOutlet weak var weatherLocation: UILabel!
    @IBOutlet weak var weatherDescription: UILabel!
    @IBOutlet weak var temperature: UILabel!
    @IBOutlet weak var weatherIcon: UILabel!


    @IBAction func refreshButtonPressed(_ sender: UIBarButtonItem) {
        print("Refresh!")
    }
}
```

### Next Time

Awesome! Now we have added connections for both the labels and the bar button item to Swift code. In the next parts, we will be using the DarkSky API to obtain weather data and show it in our newly created UI!
