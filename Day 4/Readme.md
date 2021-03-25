
main.dart
```dart

import 'package:flutter/material.dart';
import 'package:mantras/mantras.dart';

void main() {
  runApp(MantrasApp());
}


class MantrasApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      
      home: HomePageMantra(),
    );
  }
}

class HomePageMantra extends StatefulWidget {
  @override
  _HomePageMantraState createState() => _HomePageMantraState();
}

class _HomePageMantraState extends State<HomePageMantra> {

 String meraMantra = Mantras().getMantra();

void updateMantra() {
  setState(() {
      meraMantra = Mantras().getMantra();
    });
} 


  

 

  @override
  Widget build(BuildContext context) {
    
    
    return Scaffold(
      appBar: AppBar(

        centerTitle: true,
        title: Text("Mantras App"),
      ),
  floatingActionButton: FloatingActionButton(
    
    onPressed: updateMantra,
    child: Icon(Icons.refresh),
    
    
    ),
      body: Center(child: Text("$meraMantra", style: TextStyle(fontSize: 40),)),
    );
  }
}


```




add ```mantras: ^0.0.3 ``` to ```pubsec.yaml``` file
