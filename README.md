# Example for duplicate symbols issue using GooglePlaces SDK and CocoaPods
This is a minimal project with
- One iOS App target
- One framework target, linked to the main iOS App target
- Podfile specifying that both targets need GooglePlaces

At the time of creation I used `CocoaPods 1.2.1` and `Xcode 8.3.2`.
When running the project I get logs indicating duplicate symbols of the form:
```
…
Class GMSAutocompleteResultsViewController is implemented in both ~/Library/Developer/Xcode/DerivedData/GP-bwyegobhixkihmeuknrdbpdrhkwc/Build/Products/Debug-iphonesimulator/GPF.framework/GPF (0x10e6ac360) and ~/Library/Developer/CoreSimulator/Devices/294199C5-9818-4971-9E8F-A17ACBB74D75/data/Containers/Bundle/Application/D0AD7A15-BCF7-4566-A1BF-1BE7058529FF/GP.app/GP (0x10bbd8508). One of the two will be used. Which one is undefined.
–
```
