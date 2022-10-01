# Fork of Flutter blur_bottom_bar

> _directly drawing the color with opacity is faster. Also using an `Opacity` widget was not necessary in this case. So i removed it._

## Original README
This is a recreation of the ios tab view with material design for android and ios


![BlurBottomBar Gif](screenshot-ios.gif "BlurBottomBar")
![BlurBottomBar Gif](screenshot-android.gif "BlurBottomBar")


## Getting Started

Add the dependency in `pubspec.yaml`:

```yaml
dependencies:
  ...
  blur_bottom_bar: ^1.0.1
```

## Basic Usage


```dart
return Scaffold(
      appBar: AppBar(title: Text("Blur bar example")),
      body: Stack(
        children: <Widget>[
          _widgetOptions.elementAt(_selectedIndex),
          BlurBottomView(
              bottomNavigationBarItems: const <BottomNavigationBarItem>[
                BottomNavigationBarItem(
                  icon: Icon(Icons.home),
                  label: 'Home'),
                ),
                BottomNavigationBarItem(
                  icon: Icon(Icons.business),
                  label: 'Business',
                ),
                BottomNavigationBarItem(
                  icon: Icon(Icons.school),
                  label: 'School',
                )
              ],
              currentIndex: _selectedIndex,
              onIndexChange: (val) {
                _onItemTapped(val);
              }),
        ],
      ),
    );
```
