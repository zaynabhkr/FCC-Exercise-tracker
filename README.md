This boilerplate provides a foundation for creating an API to manage user exercises and logs. Users can submit exercise and user information via forms, and the API will respond with structured data.

Data Models and API Responses
Exercise
When a user submits an exercise entry, the API will respond with the following structure:
```
{
  "username": "fcc_test",
  "description": "test",
  "duration": 60,
  "date": "Mon Jan 01 1990",
  "_id": "5fb5853f734231456ccb3b05"
}
```
## Properties:
```
username (string): The name of the user who performed the exercise.
description (string): A brief description of the exercise.
duration (number): Duration of the exercise in minutes.
date (string): The date the exercise was performed, formatted as "Mon Jan 01 1990". Use the toDateString method of the Date API to achieve this format.
_id (string): Unique identifier for the exercise entry.
User
When a user submits their information, the API will respond with the following structure:
```
```
{
  "username": "fcc_test",
  "_id": "5fb5853f734231456ccb3b05"
}
```
## Properties:

- username (string): The name of the user.
- _id (string): Unique identifier for the user.
- Log
To retrieve a user's exercise log, the API will respond with

```
{
  "username": "fcc_test",
  "count": 1,
  "_id": "5fb5853f734231456ccb3b05",
  "log": [{
    "description": "test",
    "duration": 60,
    "date": "Mon Jan 01 1990"
  }]
}
```
## Properties:

- username (string): The name of the user.
- count (number): The total number of exercise entries for the user.
- _id (string): Unique identifier for the user.
- log (array): An array of exercise entries for the user. Each entry has:
- description (string): Description of the exercise.
- duration (number): Duration of the exercise in minutes.
- date (string): The date the exercise was performed, formatted as "Mon Jan 01 1990".
