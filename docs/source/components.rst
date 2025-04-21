Main Components
===============

**Pages**


1. Home Page
2. Search Page
3. Login Page
4. Add Recipe Page
5. Bookmarks Page
6. Meal Plan Page
7. Recipe Page
8. Shopping List Page

Each of these pages and their functionality is outlined below.

**Home Page**

The **Home Page** serves as the main dashboard for the app. It features:
- **Suggested Recipes**: A randomized list of recipes displayed to the user.
- **Navigation**: Links to other key pages in the app (Search, Bookmarks, Meal Plan, etc.).

**Code Overview**

The Home Page is built using Flutter and Dart. It uses the `HomePage.dart` file and integrates Firebase to fetch recipes. The layout is built with `ListView` for a scrollable display of recipe cards.



**Search Page**

The **Search Page** allows users to search for recipes. It supports:
- **Dynamic Filtering**: Users can add multiple filters to the search filter, and the page will display recipes containing those filters.
- **User Input**: An intuitive search bar with type-ahead functionality.

**Code Overview**

The Search Page is managed by the `SearchPage.dart` file. The app fetches recipes from Firebase based on the selected ingredients and displays them using a custom recipe card widget.



**Login Page**

The **Login Page** allows users to log in using their Google account.
- **Google Authentication**: Users can sign in via Google using Firebase Authentication.
- **Navigation**: Upon successful login, the user is redirected to the Home Page.

**Code Overview**

The login process is managed by `LoginPage.dart`, which interfaces with Firebase for user authentication.



**Add Recipe Page**

The **Add Recipe Page** allows users to submit their own recipes.
- **Form Input**: Users can add details like title, ingredients, instructions, and upload images.
- **Firebase Integration**: The recipe is stored in Firebase upon submission.

**Code Overview**

The page is built using `AddRecipePage.dart`. It allows users to submit data to Firebase, which stores the recipe information in the backend.



**Bookmarks Page**

The **Bookmarks Page** shows all the recipes a user has saved.
- **Fetch Bookmarked Recipes**: Recipes bookmarked by the user are fetched from Firebase using `getUserBookmarkedRecipes()`.
- **Dynamic Updates**: The page updates automatically after fetching or removing recipes using `setState()`.

**Code Overview**

The Bookmarks Page is managed by `BookmarksPage.dart`. It fetches the user's saved recipes from Firebase and displays them.



**Meal Plan Page**

The **Meal Plan Page** lets users plan their meals for the month.
- **Interactive Calendar**: Users can select a day and assign a bookmarked recipe to that date.
- **Dynamic Meal Assignment**: Selected recipes are stored per day and displayed directly on the calendar.

**Code Overview**

The `MealPlanPage` is built using a `StatefulWidget` to enable dynamic calendar updates. It integrates Firebase for user authentication and data fetching.



**Recipe Page**

The **Recipe Page** provides detailed information about a single recipe.
- **Ingredients & Instructions**: Displays the recipe’s ingredients, steps, and any other relevant details.
- **UI Design**: Includes a button to bookmark the recipe.

**Code Overview**

The Recipe Page is handled by `RecipePage.dart`. It fetches recipe data from Firebase and displays it in a user-friendly format.



**Shopping List Page**

The **Shopping List Page** allows users to manually create a shopping list or automatically import ingredients from the Meal Plan.
- **Manual Item Entry**: Users can type and add items to their shopping list.
- **Meal Plan Integration**: Automatically extracts and aggregates ingredients from the current month's meal plan.

**Code Overview**

The Shopping List Page is managed by `ShoppingListPage.dart`. It pulls data from the Meal Plan and displays the necessary ingredients.
