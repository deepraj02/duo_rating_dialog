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

![duo_rating_updated](https://user-images.githubusercontent.com/16275252/175483893-32a8445e-846e-4f71-bdb8-733e8d55db84.gif)


```dart
  return DuoRatingDialog(
                    title: const Text('How was your session?'),
                    submitButtonText: 'SUBMIT',
                    submitButtonTextStyle: const TextStyle(color: Colors.black),
                    onSubmitted: (value) {
                      // Passing data to a new page as an example

                      Map<String, dynamic> ratingsOneMap = {
                        "rating": value.ratingOne,
                        "status": value.getRatingOneStatus
                      };
                      Map<String, dynamic> ratingsTwoMap = {
                        "rating": value.ratingTwo,
                        "status": value.getRatingTwoStatus
                      };
                      List<Map<String, dynamic>> ratingsData = [
                        ratingsOneMap,
                        ratingsTwoMap
                      ];

                      Navigator.push(
                          context,
                          MaterialPageRoute(
                              builder: ((context) =>
                                  ResultsPage(ratingsData: ratingsData))));
                    });
```

## Additional information

This is my first package. Feel free to flag any issues you might have
