
main.dart
```dart
import 'dart:ui';

import 'package:flutter/material.dart';
import 'package:portfolio/portfolio_page.dart';

// void main () {

// }

void main() => runApp(PortfolioApp());

class PortfolioApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: PortfolioPage(),
    );
  }
}


```




portfolio_page.dart
```dart
import 'package:flutter/material.dart';
import 'package:recase/recase.dart';

class PortfolioPage extends StatelessWidget {
  ReCase rc = new ReCase('avengers infinity war');

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(rc.snakeCase),
        centerTitle: true,
      ),
      body: SingleChildScrollView(
        padding: EdgeInsets.all(20),
        child: Column(
          // mainAxisAlignment: MainAxisAlignment.center,
          // crossAxisAlignment: CrossAxisAlignment.center,

          children: [
            ClipRRect(
              borderRadius: BorderRadius.circular(20),
              child: Image(
                  width: MediaQuery.of(context).size.width * 4 / 7,
                  image: NetworkImage(
                      'https://pyxis.nymag.com/v1/imgs/bb2/701/c4787eccc4a76307518ae0632fb9196faa-rick-and-morty.rsquare.w700.jpg')),
            ),
            SizedBox(
              height: 10,
            ),
            Text(
              "Rick Sanchez",
              style: TextStyle(fontSize: 30),
            ),
            Card(
              shape: RoundedRectangleBorder(
                  borderRadius: BorderRadius.circular(20)),
              elevation: 10,
              // color: Colors.red,
              child: Padding(
                padding: const EdgeInsets.all(18.0),
                child: Text(
                  "Mobile App Developer",
                  style: TextStyle(fontSize: 30),
                ),
              ),
            ),
            SizedBox(
              height: 20,
            ),
            Text(
              "Lore",
              textAlign: TextAlign.justify,
              style: TextStyle(fontSize: 30),
            ),
            Container(
              margin: EdgeInsets.all(30),
              padding: EdgeInsets.all(10),
              decoration: BoxDecoration(
                border: Border.all(
                  color: Colors.red,
                  width: 5,
                ),
                borderRadius: BorderRadius.circular(10),
              ),
              child: Row(
                children: [
                  Icon(Icons.email),
                  SizedBox(
                    width: 10,
                  ),
                  Text("ricksanchez@gmail.com"),
                ],
              ),
            ),
            InkWell(
              onTap: () {},
              child: Container(
                margin: EdgeInsets.all(30),
                padding: EdgeInsets.all(10),
                decoration: BoxDecoration(
                  border: Border.all(
                    color: Colors.red,
                    width: 5,
                  ),
                  borderRadius: BorderRadius.circular(10),
                ),
                child: Row(
                  children: [
                    Icon(Icons.email),
                    SizedBox(
                      width: 10,
                    ),
                    Text("ricksanchez@gmail.com"),
                  ],
                ),
              ),
            ),
            Wrap(
              children: [
                Padding(
                  padding: EdgeInsets.all(10),
                  child: Chip(
                      backgroundColor: Colors.amber,
                      label: Container(
                          padding: EdgeInsets.all(10),
                          child: Text("Javascript"))),
                ),
                Container(
                  padding: EdgeInsets.all(10),
                  child: Chip(
                      backgroundColor: Colors.amber,
                      label: Container(
                          padding: EdgeInsets.all(10),
                          child: Text("Javascript"))),
                ),
                Padding(
                  padding: EdgeInsets.all(10),
                  child: Chip(
                      backgroundColor: Colors.amber,
                      label: Container(
                          padding: EdgeInsets.all(10),
                          child: Text("Javascript"))),
                ),
              ],
            ),
          ],
        ),
      ),
    );
  }
}


```





add the following
- ```font_awesome_flutter: ^9.0.0```
- ```url_launcher: ^6.0.2```
- ```recase: ^3.0.1```


to ```pubsec.yaml``` file
