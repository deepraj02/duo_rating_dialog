<!-- 
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/guides/libraries/writing-package-pages). 

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-library-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/developing-packages). 
-->

A custom rating dialog for developers who want to ask users for two ratings


## Features

Enhanced [rating_dialog](https://pub.dev/packages/rating_dialog)

## Usage

![duo_rating_dialog](https://user-images.githubusercontent.com/16275252/175461987-e45b0dcb-2cc7-4cff-91ba-3cfc94004018.gif)

```dart
DuoRatingDialog(
    title: const Text('How was the experience'),
    submitButtonText: 'Submit',
    submitButtonTextStyle:
        const TextStyle(color: Colors.orangeAccent),
    onSubmitted: (resp) => log(
    'Resp one : ${resp.ratingOne}, Resp two: ${resp.ratingTwo}',
    ),
)
```

## Additional information

This is my first package. Feel free to flag any issues you might have
