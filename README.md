# passing_state

A new Flutter project.

## Getting Started

Objective:
Build a Flutter application to manage a list of favorite products using the Provider package for state management.
Steps:
Create a New Flutter Project: Start by creating a new Flutter project that will serve as the foundation for the app.
Add the Provider Package:
Open your pubspec.yaml file and add the following dependency:
yaml
dependencies:
  provider: ^6.0.5
Run flutter pub get to install the package.
Create a Favorites Model:
In the lib directory, create a new file named favorites.dart.
Define a Favorites class that extends ChangeNotifier:
Use a List<String> to store favorite product items.
Implement methods such as addItem(String item) and removeItem(String item) to manage the list of favorites.
Ensure that the notifyListeners() method is called after modifying the list so the UI is updated.
Create the Product List UI:
In main.dart, wrap the MaterialApp widget with ChangeNotifierProvider to provide the Favorites class to the widget tree.
Use a Scaffold widget with an AppBar titled "Product List".
Inside the body of the Scaffold, use ListView.builder to display a list of product items.
For each product:
Use a Card widget to display product details.
Add an IconButton to allow users to add products to the favorites list.
Favorites Screen:
Add a FloatingActionButton in the product list screen that navigates to the favorites screen.
On the favorites screen, create a new ListView.builder to display the list of favorite products.
Wrap the ListView.builder with a Consumer<Favorites> widget to automatically update the list when items are added or removed.
Make It Interactive:
On the favorites screen, allow users to remove items from the favorites list by adding an IconButton with a delete icon.
Use the removeItem method to remove a product from the favorites list.
Test Your App:
Verify that users can add items to the favorites list and manage them by removing items or viewing them on the favorites screen.
Ensure that the UI updates in real time when changes are made to the list of favorites.
