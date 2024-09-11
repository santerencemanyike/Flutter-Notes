# Flutter Notes
## Dart
### Variables
* Like javascript, Dart will also set the data type based on the assigned value.
* All initially assigned variables will remain constants unless explicitly stated that they are dynamic.
* Dart variable assignment:
  1. var x_var = 'something';
  2. String y_var = 'string'; //String variable
  3. int z_var = 10; //Integer variable
  4. bool j_var = true; //Bolean variable
  5. dynamic k_var = 'anything'; //Changing variable

**Flutter is a React insired framework for UI customization using widgets.**  
Here is the architecture or design pattern Flutter uses.  
```Dart
import 'package:flutter/material.dart';

void main() {
  runApp(
    const Center(
      child: Text(
        'Hello, world!',
        textDirection: TextDirection.ltr,
      ),
    ),
  );
}
```

* In the above code, the runApp() method is the root tree for this widget.
* The child is the property of this app.
* Text is a widget but can also be a value based on ui requirements.

## Some Widgets
### Scaffold widget properties

1. AppBar widget //Navbar  
  appBar properties :
     * title (Text)
     * centerTitle (Boolean)
  
2. Center widget //Body of the app
   * child

3. FloatingActionButton widget //Bottom right button
   * child

4. Text widget //just text
   * 'String text'
   * style

5. TextStyle widget
   * fontSize
   * fontWeigth (e.g. Fontweight.bold)
   * letterSpacing
   * color, backgroundColor, etc....  (e.g. Colors.grey[600])

6. Image widget
   * image (AssetImage(path))

```Dart
void main() => runApp(MaterialApp(
    home: Scaffold(
        appBar: AppBar(
            title: Text("My test title"),
            centerTitle: true,
        ),
        body: Center(
          child: Text("Centered body text"),
        ),
        floatingActionButton: FloatingActionButton(
          child: Text("Scroll"),
          onPressed: () {
            // Action to perform when the button is pressed
            print("FloatingActionButton pressed!");
          },
        ),
    )
));
```
## 

## Hot Reload, Hot Restart, Full Restart
1. _Hot reload_ will rebuild all the widget trees without a rerun on the main() and initState() thus preserving it's app state.
2. _Hot restart_ will restart the Flutter app and loose it's app state.
3. _Full restart_ Recompiles the whole app thus taking more time to finish executing. 
   
## Stateless widget
Stateless widgets are for handling final data which never changes in the app.  
Below is a snipet of an implimentation of a stateless widget.
```Dart
class MyWidget extends StatelessWidget {
  // const MyWidget({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(
          "My test title",
          style: TextStyle(fontFamily: 'indiFlower'),
        ),
        centerTitle: true,
      ),
      body: Center(
        child: Text(
          'Centered body text',
          style: TextStyle(fontFamily: 'indiFlower'),
        ),
      ),
      floatingActionButton: FloatingActionButton(
        child: Text(
          'Scroll',
          style: TextStyle(fontFamily: 'indiFlower'),
        ),
        onPressed: () {
          // Action to perform when the button is pressed
          print('FloatingActionButton pressed!');
        }
      ),
    );
  }
}
```
