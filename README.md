# 

## Description
Supply detailed information about courses and professors at the U of M.

## Endpoints
2 endpoint something like  
`get_course_info` -> returns syllabus, course quality rating, difficulty rating, the terms it is offered(with modification)
- Course name/code. Ex: COMP3040
- specific_time_slots

`get_prof_info` -> return courses teach/taught, course diffculty, optional (reviews)
- Professor name
- reviews

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

