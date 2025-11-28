# MyFavorites – iOS UITableView Demo

MyFavorites is a small UIKit-based iOS application that displays my favorite items across four categories (movies, music, books, and university courses) using a multi-section `UITableView` with a custom cell.

This project was created as part of the **“My Favorites TableView”** iOS development assignment.

---

## Features

- **UIKit + Storyboard** (no SwiftUI)
- `UITableView` with **4 sections** and **5 rows** per section:
  - 🎬 Favorite Movies  
  - 🎵 Favorite Music  
  - 📚 Favorite Books  
  - 💻 Favorite University Courses
- **Custom `UITableViewCell`** with:
  - Cover **Image View** (poster/cover/icon)
  - **Title label** (main name)
  - **Subtitle label** (author/director/year)
  - **Review label** with 2–3 lines of personal review
- **Auto Layout** with dynamic cell height using
  - `UITableView.automaticDimension`
  - Proper constraints for image and all labels
- **Custom section headers** with emoji icons (bonus)

---

## Architecture

- **Model**
  - `FavoriteItem` – simple struct that holds `imageName`, `title`, `subtitle` and `review`.
  - `FavoritesSection` – `enum` with 4 cases (`movies`, `music`, `books`, `courses`) and a computed `title` property.

- **View**
  - Storyboard with a single `UIViewController` and a full-screen `UITableView`.
  - Prototype cell with:
    - `UIImageView` (`coverImageView`)
    - `UILabel` for title (`titleLabel`)
    - `UILabel` for subtitle (`subtitleLabel`)
    - `UILabel` for review (`reviewLabel`)

- **Controller**
  - `ViewController`:
    - Holds the 2D array `data: [[FavoriteItem]]`.
    - Implements `UITableViewDataSource` and `UITableViewDelegate`.
    - Configures cells in `tableView(_:cellForRowAt:)`.
    - Provides section titles / custom headers.

---

## Technologies Used

- iOS 15.0+
- Xcode (UIKit project template with Storyboard)
- Swift
- `UITableView`, `UITableViewCell`
- Auto Layout & Dynamic Type
- SF Symbols / asset images

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/MyFavorites.git
