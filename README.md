# ContactsMa# Contacts Manager Application

**Contacts Manager Application** is an Android app that allows users to manage contacts by adding, deleting, and viewing a list of contacts. The app is built using **Room Database** for persistent data storage and **Android ViewModel** to manage UI-related data lifecycle-aware.

## Features
- **Add Contact**: Users can add a new contact with a name and email. The contact is stored in the Room database.
- **View Contacts**: A list of all saved contacts is displayed using a RecyclerView.
- **Delete Contact**: Swipe left on a contact to delete it from the database.
- **Data Persistence**: The app uses Room Database to store and retrieve contacts persistently.
- **LiveData and ViewModel**: The app implements LiveData and ViewModel to manage data efficiently and update the UI in response to data changes.

## Technical Details
- **Architecture Components**:
  - **Room Database**: Used for local data storage.
  - **ViewModel**: Ensures UI-related data survives configuration changes.
  - **LiveData**: Observes data changes in the database and updates the UI automatically.
- **Data Binding**: Used for connecting UI components in layouts to data sources using declarative format rather than programmatically.
- **RecyclerView**: Displays the list of contacts with support for swipe-to-delete functionality.
- **ExecutorService**: Ensures database operations run on a background thread to avoid blocking the UI thread.

## Core Classes
- `AddNewContactActivity`: Activity for adding new contacts. It binds user input to the `Contacts` entity using data binding.
- `MainActivity`: Displays a list of all saved contacts and supports swipe-to-delete functionality.
- `ContactDAO`: Data Access Object (DAO) interface with methods for inserting, deleting, and querying contacts.
- `ContactDatabase`: Singleton class that provides access to the Room database.
- `Contacts`: Entity class representing the contact with fields for `name`, `email`, and a primary key `id`.
- `MyViewModel`: Handles interaction with the repository and provides data to the UI.
- `Repository`: Manages data operations and ensures tasks like database access run off the main thread.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/username/contacts-manager-app.git
2. Open the project in Android Studio.
3. Build and run the project on an Android emulator or physical device.

## Future Enhancements
Add functionality to update existing contacts.
Implement search functionality for contacts.
