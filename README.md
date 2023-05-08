# Hive Notes App 📝

Hive Notes App is a simple note-taking application built using Flutter framework and the Hive database. It allows users to create, edit, and delete notes, which are stored locally using Hive.

## Features ✨

- ✏️ Create a new note with a title and description
- 📋 View a list of all notes, with the ability to edit or delete each note
- ✏️ Edit an existing note and save the changes
- 🗑️ Delete a note from the list
- 💾 Store notes locally using Hive database

## Getting Started 🚀

To get started with the Hive Notes App, follow these instructions:

### Prerequisites 📋

- Flutter SDK: Make sure you have Flutter SDK installed on your machine. You can download it from the official Flutter website: [https://flutter.dev](https://flutter.dev)
- Flutter IDE: Choose your preferred IDE for Flutter development, such as Visual Studio Code or Android Studio.
- Hive Package: The Hive Flutter package is required for using Hive in your Flutter project. Make sure to include it in your `pubspec.yaml` file.

### Installation ⚙️

1. Clone the repository: 

        https://github.com/Ganeshshinde-2003/Flutter-Notes-Taking-App-Using-Hive-DataBase.git
        

2. Install dependencies:

        flutter pub get
        

3. Run the app:

        flutter run

### Usage 📱

- Launch the Hive Notes App on your device or emulator.
- The home screen will display a list of all the notes stored in the database.
- To create a new note, tap on the floating action button (the "+" icon) at the bottom right corner of the screen. Enter the title and description for the note, and tap the green checkmark icon to save it.
- To edit a note, tap on the edit icon (pencil) next to the note. Modify the title or description, and tap the green checkmark icon to save the changes.
- To delete a note, tap on the delete icon (trash bin) next to the note.
- The notes are displayed in reverse order, with the latest note appearing at the top of the list.

### How Hive Works 🐝

Hive is a lightweight, yet powerful NoSQL database for Flutter and Dart. It offers fast and efficient storage of structured data by using key-value pairs and provides excellent performance, even with large datasets.

In this project, Hive is used to store and retrieve the notes. Here's how it works:

1. Data Model 📦: The `NotesModel` class represents a single note and defines its properties (title and description). It extends the `HiveObject` class to enable persistence.

2. Hive Box 🗃️: Hive organizes data into boxes. The `Boxes` class provides a static method `getData()` to get the Hive box instance for storing the notes. The box is obtained using `Hive.box('notes')`, where 'notes' is the box name.

3. Creating and Saving Notes ✏️: When a new note is created, an instance of `NotesModel` is created with the provided title and description. The note is then added to the Hive box using `box.add(data)`. The changes are saved using `data.save()`.

4. Retrieving and Displaying Notes 📋: The `ValueListenableBuilder` widget is used to listen to changes in the Hive box and rebuild the UI whenever the
