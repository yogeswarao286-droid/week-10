import 'package:flutter/material.dart';
void main() {
runApp(MyApp());
}
class MyApp extends StatelessWidget {
// Debug Tip: If this is not const and UI rebuilds, re-run will be slower.
@override
Widget build(BuildContext context) {
return MaterialApp(
showPerformanceOverlay: true,
title: 'Flutter Debugging Demo',
debugShowCheckedModeBanner: false,
home: DebugDemoScreen(),
);
}
}
class DebugDemoScreen extends StatefulWidget {
@override
_DebugDemoScreenState createState() => _DebugDemoScreenState();
}
class _DebugDemoScreenState extends State<DebugDemoScreen> {
int counter = 0;
String? message;
void _incrementCounter() {
setState(() {
counter++;
debugPrint("Counter value updated to: $counter");
// Intentional Bug: Message should update, but not set.
if (counter % 2 == 0) {
message = "Even number clicked";
} else {
message = "No message yet";
}
});
}
@override
Widget build(BuildContext context) {
// Layout Debug Tip: Using Column without proper spacing or overflow handling.
return Scaffold(
appBar: AppBar(title: const Text('Debugging Tools Example')),
body: Center(
child: Column(
mainAxisAlignment: MainAxisAlignment.center,
children: [
const Text('You pressed the button this many times:'),
Text(
'$counter',
style: Theme.of(context).textTheme.headlineMedium,
),
if (message != null)
Text(
message!,
style: const TextStyle(color: Colors.green),
)
else
const Text(
"No message yet",
style: TextStyle(color: Colors.red),
),
],
),
),
floatingActionButton: FloatingActionButton(
onPressed: _incrementCounter,
tooltip: 'Increment',
child: const Icon(Icons.add),
),
);
}
}


