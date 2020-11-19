# UofMInfo API

## Description
UofMInfo is a tool to find out detailed information about courses and professors at the University of Manitoba. The purpose of this API is to convenience students when they are looking for courses.  

With the UofMInfo API, you can:  
- Get specific course information include syllabus, quality, etc.
- Search for a professor, and get the professor's information and rating.

## Before you start
- UofMInfo API is a REST API, which means it uses the `GET` request
- As is standard in URLs, parameters should be separated by "&"

## Endpoints
### get_course_info
Get detailed course information by providing the course code and which term.
##### Parameters
| Parameter   |  Type  | Required |        Description            |
|-------------|--------|----------|-------------------------------|
| `code`| string | YES      |  Standard UofM course code    |
| `termTimes`    |   string  | NO      | Specific class term of interest           |

##### Sample request
`https://UofMInfo/api/courseInfo?code=COMP3040&termTimes=winter`

##### Sample response
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
Get the professor's information by providing the professor's name.
##### Parameters
| Parameter   |  Type  | Required |        Description            |
|-------------|--------|----------|-------------------------------|
| `profName`| string | YES      |  Name of a UofM Professor    |
| `reviews`    |   boolean  | NO      | Review data pulled from rate my prof           |

##### Sample request
`https://UofMInfo/api/profInfo?profName=JohnSmith&reviews=true`

##### Sample response

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
