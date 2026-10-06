# CineMatch

CineMatch is an Android movie recommendation application developed with **Kotlin**. The app helps users discover movies based on their preferences by retrieving movie data from **The Movie Database (TMDB) API**.

The project was built as part of a mobile application programming course and focuses on Android development, API integration, data handling, and user interface implementation.

## Features

- Browse and discover movies
- Retrieve real-time movie information from the TMDB API
- Display movie posters, titles, ratings, and other details
- Recommend movies based on user preferences
- Save user preferences locally
- Smooth image loading and movie list display

## Tech Stack

- **Kotlin**
- **Android Studio**
- **Retrofit** – API communication
- **Gson** – JSON parsing
- **Glide** – image loading
- **RecyclerView** – movie list display
- **SharedPreferences** – local preference storage
- **TMDB API** – movie data

## How It Works

1. The application connects to the TMDB API using Retrofit.
2. Movie data is retrieved and converted into Kotlin objects using Gson.
3. Movies are displayed through RecyclerView.
4. Glide is used to load movie posters efficiently.
5. User preferences are stored locally with SharedPreferences.
6. The application uses these preferences to provide a more personalized movie discovery experience.

## Project Structure

The project follows a modular Android application structure, separating:

- API communication
- Data models
- UI components
- User preference management
- Movie recommendation functionality

## What I Learned

Through this project, I gained practical experience with:

- Building Android applications with Kotlin
- Integrating external REST APIs
- Handling JSON data
- Managing asynchronous API requests
- Designing RecyclerView-based interfaces
- Storing user data locally
- Debugging and structuring a complete mobile application

## API

This project uses the **TMDB API** for movie data.

To run the application, you will need your own TMDB API key.

> Do not commit your API key directly to a public repository. Store it securely in your local configuration.

## Author

**Asiye Baran**

Computer Science and Engineering  
Sungkyunkwan University

GitHub: [Asiyeee](https://github.com/Asiyeee)
