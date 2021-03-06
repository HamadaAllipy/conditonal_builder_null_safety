# conditional_builder_null_safety

This is package its purpose show UI elements according for conditional type and supports null safety

## Getting Started

```yaml
dependencies:
  conditional_builder_null_safety: ^0.0.6
```

## import this package
```dart
import 'package:conditional_builder_null_safety/conditional_builder_null_safety.dart';
```
## Example
*If the condition is ***true***, will be ***builder*** executed*
```dart
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        body: ConditionalBuilder(
          condition: true,
          builder: (context) => Center(child: Text('this is true')),
          fallback: (context) => Center(child: Text('this is not true')),
        ),
      ),
    );
  }
```

<img src="screenshot/Screenshot_2.jpg" width="200"/>

*If the condition is ***not true*** or ***false***, will be ***fallback*** executed*
```dart
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: ConditionalBuilder(
        condition: false,
        builder: (context) => Center(child: Text('this is true')),
        fallback: (context) => Center(child: Text('this is not true')),
      ),
    );
  }
```

<img src="screenshot/Screenshot_3.jpg" width="200"/>

*you can set ***fallback is null*** don't worry it is return a empty container*
```dart
@override
  Widget build(BuildContext context) {
    return Scaffold(
      body: ConditionalBuilder(
        condition: false,
        builder: (context) => Center(child: Text('this is true')),
        fallback: null,
      ),
    );
  }
```
<img src="https://github.com/HamadaAllipy/conditonal_builder_null_safety/blob/version_0.0.3/Screenshot_1.jpg" width="200"/>


 add a new function **generateRandom(int min, int max);** its return int , create random number between minimum and maximum
 ```dart
 int random = generateRandom(10 , 100);
//output 99 or 47 or 11 or else number 
 ```


This project is a starting point for a Dart
[package](https://flutter.dev/developing-packages/),
a library module containing code that can be shared easily across
multiple Flutter or Dart projects.

For help getting started with Flutter, view our 
[online documentation](https://flutter.dev/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.
