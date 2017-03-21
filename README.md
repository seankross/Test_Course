# Test Course

This course is meant to demonstrate some of swirl's basic features.

## Installation

```r
library(swirl)
install_course_github("seankross", "Test_Course")
swirl()
```

## HTML File Questions

The last question in the "Test Lesson" lesson shows an example of an experimental question
type called an HTML question. This question type allows a course author to
display an HTML file in the Viewer pane of RStudio. If the student is not using
RStudio then the HTML file is opened in the student's web browser. Showing the
student an HTML file allows course authors to show images, mathematical equations,
code snippets, and tables to students.

In order to create an HTML question create a Figure question and specify an
R file for the `Figure` field for the question in `lesson.yaml`. Inside of your R file (in this
case `html.R`) use the `.viewer_question()` function with the name of the HTML
file you want to show as an argument. Make sure to include that HTML file in the
swirl lesson. Copy the `initLesson.R` file from this lesson into your lesson and
be sure to change the course name and lesson name variables in the `.pathtofile()`
function. This procedure should allow you to show local static HTML files in
your swirl lessons!