# Species Identifer App Concept & Purpose

## Description
Our app allows users to take and upload images of plants or animals, which are then analyzed using the [Google GenAI API](https://aistudio.google.com/prompts/new_chat) to identify the species, and see a map of all of their previous uploads. Users open the app, take a photo in real-time, and see a map of the location of the sighting (defaults to users’ current location). The app integrates [Google Maps](https://developers.google.com/maps) to display markers showing where each image was uploaded. Clicking on the marker will bring up the species name. The goal is to help users identify local plants and animals and record a collection of their encounters.

## Selected Database, API, and Sensor
- **Database**: Firebase Firestore (for storing image metadata, user submissions, and location data)
  - **Create**: upon uploading an image, a history of that submission will be stored within the database
  - **Read**: users can select a past submission from the history panel to view
  - **Update**: users can add notes to past/current submissions
  - **Delete**: users will be able to delete past submissions from the history panel
- **API**: Google GenAI API (for species identification from images)
- **Sensors**: Camera (for taking pictures of plants and animals) and GPS (for identifying location of the sighting)

## Target Device Types for Testing
- **Smartphone**: primary device with one-column layout
- **Tablet**: secondary device with multi-pane layout

## Initial Wireframes
1. **Login Screen**: Users can login using Firebase's OAuth
2. **Home Screen**: Buttons for "Take Photo" and then "Upload Photo"
3. **Identification Screen**: Displays uploaded image and species result
4. **Map View**: Shows markers for all past uploads, clickable with species details
