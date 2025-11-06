# OpenRes

OpenRes is modeled after OpenTable. Like OpenTable, OpenRes is a web application that primarily features searching for and making reservations at restaurants using a wide range of search parameters: 
* Date
* Time
* Party Size
* Location (i.e. city, state, etc.)
* Cuisine
* Restaurant Name

Other features include:
* Writing reviews
* Saving a restaurant to your favorites

Live Site: https://git.heroku.com/open-res.git



## Architecture and Technologies:
* JavaScript 9
* React 16.8.6
* Redux 4.0.1
* Ruby on Rails 5.2.3
* PostgreSQL 2.2.2
* Webpack 4.32.2

# Features:
## Restaurant Search:
Users can search for multiple `keyword`s against multiple restaurant data columns. This feature implements the gem `PgSearch`. 

<img src="./readme_images/search.gif">

## User-Authorization:
OpenRes features backend auth using BCrypt for password hashing purposes. Logged in user state is persisted via cookies unless deliberately signed out. Email addresses used to sign up are saved to the rails backend with associated password digests where uniqueness is ensured by database and model restraints.

## Reservations:
Users can select date, time, and party size and OpenRes will generate a list of restaurants with available reservations closest to the selected options.

<img src="./readme_images/reservation.gif">

## Favorites:
Accessing a favorite restaurant is made easy. Once the user has saved a restaurant, it is accessible through the drop down menu in the top-right corner via "Saved Restaurants".

<img src="./readme_images/favorites.gif">

## Reviews:
Once logged in, OpenRes allows users to leave a single review per restaurant. Reviews require 1-5 star ratings of 4 categories, 1-4 rating for noise level, and a description.

<img src="./readme_images/reviews.gif">
