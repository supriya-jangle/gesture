import 'package:flutter/material.dart';
void main() => runApp(MyApp());
class MyApp extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
 return MaterialApp(
 home: GestureDemo(),
 );
 }
}
class GestureDemo extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
 return Scaffold(
 appBar: AppBar(title: Text('GestureDetector Example')),
 body: Center(
 child: GestureDetector(
 onTap: () {
 print('Tapped!');
 },
 onDoubleTap: () {
 print('Double Tapped!');
 },
 onLongPress: () {
 print('Long Pressed!');
 },
 onPanUpdate: (details) {
 print('Dragging at position: ${details.localPosition}');
 },
 child: Container(
 color: Colors.blue,
 width: 200,
 height: 200,
 child: Center(
 child: Text(
 'Tap Me!',
 style: TextStyle(color: Colors.white, fontSize: 20),
 ),
 ),
 ),
 ),
 ),
 );
 }
}
