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