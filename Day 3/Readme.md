
App Code

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MeraApp());
}



class MeraApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
     

      home: MeraHome(),
    );
  }
}

class MeraHome extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(


      appBar: AppBar(
        leading: Icon(Icons.menu, color: Colors.black,),
        title: Text("Techdrill is awesome"),
        centerTitle: true,
        elevation: 10,
        backgroundColor: Colors.red,
      ),

      backgroundColor: Colors.green,


      body: Center(
        child: Container(
          child: Icon(Icons.star_rate)
        ),
      ),


      // drawer: Drawer(

      //   child: Text("sdfdsfdfdsfdsfd", style: TextStyle(

      //       fontSize: 50,
      //       color: Colors.red,

      //   ),),


      // ),

      

      bottomNavigationBar: BottomNavigationBar(
        items: const <BottomNavigationBarItem>[
          BottomNavigationBarItem(
            icon: Icon(Icons.home),
            label: 'Home',
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.business),
            label: 'Business',
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.school),
            label: 'School',
          ),
        ],
        )
      );
 }
}


```
