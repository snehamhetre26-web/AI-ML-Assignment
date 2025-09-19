Q1 — REST API Endpoints

1) Assign Lesson

POST /api/assignments

Request (JSON):

{
    "teacherId": "T123",
    "studentId": "S456",
    "lessonId": "L789"
}

Response (JSON):

{
    "assignmentId": "A001",
    "status": "assigned",
    "message": "Lesson L789 assigned to student S456 successfully."
}




2) View Incomplete Lessons

GET /api/students/{studentId}/assignments?status=incomplete

Response (JSON):

[
  {
    "assignmentId": "A001",
    "lessonId": "L789",
    "lessonTitle": "Introduction to AI",
    "status": "incomplete"
  }
]




3) Mark Lesson as Complete

PUT /api/assignments/{assignmentId}/complete

Request (JSON):

{
  "completedAt": "2025-09-19T10:30:00Z"
}

Response (JSON):

{
  "assignmentId": "A001",
  "status": "completed",
  "message": "Assignment marked as complete."
}




4) Teacher Views Completion Status

GET /api/teachers/{teacherId}/assignments/status

Response (JSON):

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
