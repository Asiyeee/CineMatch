# CineMatch 🎬

A dark, streaming-app styled Android movie discovery app built with Kotlin.

## Setup

### 1. Get a TMDB API Key
1. Go to https://www.themdb.org/settings/api
2. Create a free account and request an API key
3. Copy your API key

### 2. Add Your API Key
Open `app/build.gradle` and replace `YOUR_TMDB_API_KEY_HERE`:
```gradle
buildConfigField "String", "TMDB_API_KEY", "\"YOUR_ACTUAL_KEY_HERE\""
```

### 3. Open in Android Studio
- File → Open → Select the `CineMatch` folder
- Wait for Gradle sync
- Run on emulator or device (min SDK 24 / Android 7.0)

---

## Architecture

```
com.cinematch.app/
├── activities/
│   ├── MainActivity.kt          # Home: genre/mood/rating selection
│   ├── MovieResultActivity.kt   # Grid of matching movies
│   ├── MovieDetailActivity.kt   # Full movie detail + favorites
│   └── FavoritesActivity.kt     # Saved favorites list
├── adapters/
│   └── MovieAdapter.kt          # RecyclerView adapter (ListAdapter + DiffUtil)
├── model/
│   └── Movie.kt                 # Data classes (Movie, MovieResponse)
├── network/
│   ├── TmdbApiService.kt        # Retrofit interface
│   └── RetrofitClient.kt        # OkHttp + Retrofit singleton
└── utils/
    ├── FavoritesManager.kt      # SharedPreferences CRUD for favorites
    └── GenreMapper.kt           # Genre IDs + Mood→Genre mapping
```

## Features

| Feature | Implementation |
|---|---|
| Movie discovery | TMDB `/discover/movie` API |
| Genre filter | 7 genres via Material Chips |
| Mood filter | 5 moods, mapped to genres |
| Rating filter | 5+, 6+, 7+, 8+ minimum |
| Movie list | RecyclerView 2-col grid + Load More |
| Movie detail | Collapsing toolbar + backdrop + poster |
| Favorites | SharedPreferences + Gson serialization |
| Images | Glide with placeholder |
| UI | Dark theme, Material Design 3 |

## Tech Stack

- **Language**: Kotlin
- **UI**: ViewBinding, Material Design 3, RecyclerView
- **Network**: Retrofit 2 + Gson + OkHttp
- **Images**: Glide 4
- **Storage**: SharedPreferences
- **Async**: Kotlin Coroutines (lifecycleScope)
