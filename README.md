# UofMInfo API

## Description
UofMInfo is a tool to find out detailed information about courses and professors at the University of Manitoba. The purpose of this API is to convenience students when they are registering for courses.

## Endpoints
### get_course_info
Supplies information on a given course.
#### Parameters
| Parameter   |  Type  | Required |        Description            |
|-------------|--------|----------|-------------------------------|
| `code`| string | YES      |  Standard UofM course code    |
| `term`    |   string  | NO      | Specific class term of interest           |

`https://UofMInfo/api/courseInfo?code=COMP3040&timeTimes=winter`

Result is formatted as a JSON. Here's an example:
``` json
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
Supplies additional information on a specific professor.
#### Parameters
| Parameter   |  Type  | Required |        Description            |
|-------------|--------|----------|-------------------------------|
| `profName`| string | YES      |  Name of a UofM Professor    |
| `reviews`    |   boolean  | NO      | Review data pulled from rate my prof           |


`https://UofMInfo/api/profInfo?profName=JohnSmith&reviews=true`

Result is formatted as JSON. Here's an example:

``` json
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
