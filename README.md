# 

## Description
Supply detailed information about courses and professors at the U of M.

## Endpoints
2 endpoint something like  
`get_course_info` -> returns syllabus, course quality rating, difficulty rating, the terms it is offered(with modification)

### Parameters
- code(string): Standard UofM course code. Required
- term(string): Specific class term of interest. Optional


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


`get_prof_info` -> return courses teach/taught, course diffculty, optional (reviews)

### Parameters
- profName(string): Name of a UofM Professor. Required
- reviews(boolean): Review data pulled from rate my prof. Optional

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
  "hours": "T1300"
  "rateMyProfRating": "3.6"
}
```

## Sample Request

