## Workshop 03
 
**What is the location framework called in iOS**
  CoreLocation
  ```swift 
  import CoreLocation
  ```
  
**What are the two numbers that determine location**
  longitude and latitude
  
**There are two keys you need to add to the info.plist in order to use gps of a device, what are they?**
Privacy - Location Always and When In Use Usage Description
Privacy - Location When In Use Usage Description
You are required to ask for premission to use the users location

**Can you explain the role of the CLLocationManager delegate that we looked at?**
Delegating a job to itself

**How can you simulate location on the simulator?**
Setting up gpx file

``` swift
extension ViewController: CLLocationManagerDelegate {
    
    func locationManager(_ manager: CLLocationManager, didUpdateLocations locations: [CLLocation]) {
        
        print(locations.last!)
        
        cordinateLabel.text = "\(locations.last!.coordinate.latitude) \(locations.last!.coordinate.longitude)"
        
        
        
    }
```

**How do you create a custom simulator for testing?**
gpx file with locations and use the little "location arrow" to change the location

**How can you automatically tell the simulator to use this when you run your app?**
Filename up top - Edit Scheme - Options - Default Location 
