
{
    "teacherId": "T123",
    "studentId": "S456",
    "lessonId": "L789"
}


{
    "assignmentId": "A001",
    "status": "assigned",
    "message": "Lesson L789 assigned to student S456 successfully."
}



[
  {
    "assignmentId": "A001",
    "lessonId": "L789",
    "lessonTitle": "Introduction to AI",
    "status": "incomplete"
  }
]


{
  "completedAt": "2025-09-19T10:30:00Z"
}

Response (JSON):

{
  "assignmentId": "A001",
  "status": "completed",
  "message": "Assignment marked as complete."
}


[
  {
    "studentId": "S456",
    "lessonId": "L789",
    "status": "completed"
  },
  {
    "studentId": "S456",
    "lessonId": "L790",
    "status": "incomplete"
  }
]
