# UofMInfo API

## Description
Supply detailed information about courses and professors at the U of M.

## Endpoints
### get_course_info
Supplies information on a given course. Returns a link to the syllabus, the course quality, difficulty rating, terms the course is offered in, and an optional parameter for what times the course is offered for a given term.
#### Parameters
- code(string): Standard UofM course code. Required
- term(string): Specific class term of interest. Optional

`https://UofMInfo/api/courseInfo?code=COMP3040&timeSlots=winter`

Result is formatted as a JSON. Here's an example:
```JSON
{
  "results":
  {
    "courseName":"COMP3040",
    "syllabus":"link",
    "courseQuality":"4.5",
    "difficultyRating":"3.2",
    "termsOffered":[
      "Winter",
      "Fall"
    ],
    "termTimes":[
      "time1 MWF",
      "time2 TR"
    ]
}
```



### get_prof_info

#### Parameters
- profName(string): Name of a UofM Professor. Required
- reviews(boolean): Review data pulled from rate my prof. Optional

`https://UofMInfo/api/profInfo?profName=JohnSmith&reviews=true`

Result is formatted as JSON. Here's an example:

```JSON
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 27,
  "courses": {
    "course1": "COMP2130",
    "course2": "COMP3040",
  },
  "email": "jsmith@umanitoba.ca",
  "office": "114 Allen",
  "hours": "T1300",
  "rateMyProfRating": "3.6",
  "rateMyProfReview": "link"
}
```

## Sample Request
