# ICONS WIDGET PRESENTATION ASSIGNMENT

## Introduction

This is a flutter project that showcases how to use the Icon widget

Date of presentation

Icons are graphical symbols that can be used for different things. And that is the same in Flutter. You can use buttons to show something.

## Syntax

Icons in Flutter are easy to make. This is the syntax for making Icons in Flutter:

Icon(Icons.home, color: Colors.blue, size: 50)

The Icon widget is defined using Icon().

To define the icon shape or type you should use 'Icons.' and then add the type of icon you want. There are many icons that can be found in the Material Icons Library.

To define the colors you should use 'color: Colors.' and then add any color name you want.

To define the size you should use the 'size:' and add a value like '50' which is measured in pixels.

## Where to use

Icons can be used in different scenarios when making the frontend of an application. Let's say for example on a navigation bar where people don't need to be seeing text of a certain screen.

## Code explanation

import 'package:flutter/material.dart'; <- Importing material fom flutter

void main() {
  runApp(const MyApp()); <- Entry point for the application
}

class MyApp extends StatelessWidget { <- The first widget of the app called MyApp
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(    
      title: 'Flutter Demo',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
      ),
      home: MyHomePage(), <- Calling the MyHomePage widget that contains the icons.
    );
  }
}

class MyHomePage extends StatelessWidget { <- MyHomePage widget that contains all the icons.
  const MyHomePage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold( <- Scaffold widget which helps in layouts of Flutter applications.
      appBar: AppBar(
        title: Text('Icons bro!'), 
        backgroundColor: Colors.green,
        centerTitle: true,
      ),
      body: Row( <- Displaying the icons in a row
        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
        children: <Widget>[
          Icon(Icons.hail, color: Colors.blue, size: 75), <- Displaying all the icons.
          Icon(Icons.favorite, color: Colors.green, size: 75),
          Icon(Icons.thumb_down, color: Colors.yellow, size: 75),
          ]
        ),
    );
  }
}

