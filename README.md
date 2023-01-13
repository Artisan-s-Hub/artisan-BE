# Artisan-BE

### Authentication Routes
- When you login after signing up, you would get a token that authenticates you
- Add this token to bearer token to be authenticated

--- Signup
```json 
{
    "email": "ert@test.com",
    "firstname": " Ezimo",
    "lastname": "Anam",
    "password": "Ezimo123"
}
```

--- Login
```json 
{
    "email": "ert@test.com",
    "password": "Ezimo123"
}
```
| Methods | Endpoints | Description |
| --- | --- | --- |
| POST | /signup | This is the signup endpoint |
| POST | /login | Logs an existing user |

### Category Routes

```json
{
  "name": "Cleaner",
  "description": "Cleans the surrounding",
  "group": "Home Care",
}
```

| Methods | Endpoints | Description |
| --- | --- | --- |
| POST | /addCategory | this helps you to add a new category|
| GET | /getAllCategory | Gets all Categories in the database |
| GET | /getCategoryByGroup/:group | Get Categories by group (eg Beauty and Cosmetics) |
| GET | /getCategoryByName/:name| Get Categories by name (eg Hairdresser) |
| GET | /getCategoryByID/:id | Get Categories by ID |
| PUT | /updateCategory/:id | Updates the Category |
| DELETE | /deleteCategory/:id | Deletes the Category|


### Artisan Routes

```json
{
   "name" : "Lizzy Makeup",
    "description" : "I do nice make over",
    "phoneNumber": "090876785903",
    "location": "Lagos" ,
    "category_id":"63c1c58d08d6c24c22f85403",
}
```
* You can get your category id form the categories

| Methods | Endpoints | Description |
| --- | --- | --- |
| POST | /addArtisan | this helps you to add a new artisan to the database|
| GET | /getAllArtisans | Gets all Artisan in the database |
| GET | /getAnArtisan/:id | Get Artisan by ID |
| PUT | /updateArtisan/:id | Updates the Artisan |
| DELETE |/deleteArtisan/:id| Deletes the Artisan|



### Order an Artisan Routes

```json
{
   "name" : "Gina Freeman",
    "description" : "Hi, i need a good makeup artist to come to my house",
    "phoneNumber": "090876785903",
    "location": "Lagos" ,
    "category_id":"63c1c58d08d6c24c22f85403",
    "date" : "14-01-2023",
    "time" : "01:30pm"
}
```
* You can get your category id form the categories

| Methods | Endpoints | Description |
| --- | --- | --- |
| POST | /addOrder | to Book an Artisan|
| GET | /getAllOrder | Gets all Orders of Artisans in the database |
| GET | /getOrderByID/:id| Get the Order of anArtisan by ID |
| PUT | /updateOrder/:id | Updates the Artisan Order|
| DELETE |/deleteOrder/:id| Deletes the Artisan Order|
