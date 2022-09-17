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

<h1 align="center">

[![MasterHead](https://media.giphy.com/media/E89xxATM4iZoPdr6Tb/giphy.gif)](https://pub.dev/packages/duo_rating_dialog)
</h1>

# Duo Rating Dialog🌠
## A Custom Rating Dialog which allows developers to ask users for two ratings at once

A custom rating dialog which allows developers to ask users for two ratings.

<p align='center'>
    <img src="https://user-images.githubusercontent.com/63138398/190869012-103a414d-16ce-40b2-a7d8-25511e982ffc.png" />
    <img src="https://user-images.githubusercontent.com/63138398/190869633-995fbd78-9c1c-4d97-8ee6-548402ecd702.png" />
</p>


## Features

Enhanced [rating_dialog](https://pub.dev/packages/rating_dialog)

| Parameter                 | Type         |      Description                                           |
| -----------               | -------         |      -----------                                           |
| title                     | Text         |The dialog's title                 
| ratingicon                | Icon         |To add any Specific Logo/Icon
| messageOne                | Text     |The dialog's first message/description text
| messageTwo                | Text         |The dialog's second message/description text
| starColor                 | Color         |The rating bar (star icon & glow) color
| starSize                  | double         |The size of the star
| force                     | bool         |Disables the cancel button and forces the user to leave a rating
| showCloseButton           | bool         |Show or hide the close button
| initialRatingOne          | double         |The initial first rating of the rating bar
| initialRatingTwo          | double         |The initial second rating of the rating bar
| submitButtonText          | String         |The submit button's label/text
| submitButtonTextStyle     | TextStyle         | The submit button's label/text                                  
| Function(RatingDialogResponse) |Function    | Returns a RatingDialogResponse with user's rating and comment values                 

## Usage


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
                    }
                    );
```

# Acknowledgments

This package was created by [Vipin Kumar Kashyap](https://github.com/vipinkashyap) [![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/Vipinkashyup) 

# Contributors 
[Deepraj Baidya](https://github.com/Deepraj02)  [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/deeprajbaidya) [![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/deepraj022) 
# Bugs or Requests

If you encounter any problems feel free to open an [issue](https://github.com/vipinkashyap/duo_rating_dialog/issues/new). Pull request are also welcome.