# insight_timer_capstone
An analysis of guided meditations and teachers on the Insight Timer app for my NSS Data Analytics capstone project

Teacher Columns
- alpha_index (string): The teacher's category in the Teachers Directory, based on the first character in the teacher's name as it appears in the directory (dir_teacher_name). The url for the directory page that contains the teacher is the concatenation of https://insighttimer.com/dir/meditation-teachers/ and the alpha_index.
Possible values for alpha_index include:
  - 'a' through 'z' for teacher names that start with a letter used in English
  - 'hash' for teacher names that start with a number
  - 'more' for teacher names that start with non-standard characters such as punctuation marks or letters from languages other than English
- teacher_name (string): The teacher's name as it appears on their individual page on Insight Timer's website. Although most teachers simply use their first and last name, this column has great variation in its contents. Examples include first name only, credentials or titles, and alternative teaching or organization names such as 'Blossoming Heart Meditations'.
- dir_teacher_name (string): The teacher's name as it appears in the Teacher Directory. A teacher's teacher_name and dir_teacher_name usually match, but there are teachers for which they do not match. For example, as of December 8, 2022. one teacher's name appears as 'Adam Chalmers' on their individual page (https://insighttimer.com/pleasurewellness) and 'Adam Lion Chalmers' in the Teachers Directory (https://insighttimer.com/dir/meditation-teachers/a). A possible cause would be if the Teacher Directory has not been updated since that teacher changed their name.
- teacher_href (string): A unique value for each teacher than can be used as an identifier. A concatenation of https://insighttimer.com/ and teacher_href results in the complete url for the teacher's page on Insight Timer.
- location (string): The teacher's primary location, including the city and country. May include state or province. Elements are usually separated by columns, but not always.
- followers (int): Number of teacher's followers on Insight Timer
- languages (string): A comma separated list of languages known by the teacher. Language names are [usually? always?] taken from the language and not from English. For example, a teacher that knows English, French, and Greek would have languages = 'English, Français and Ελληνική'.
- date_joined (date_time): Month and year the teacher joined Insight Timer, with the first day of the month used to convert the data type to date_time.
- about (string): Description of the teacher. [longest length allowed?]
- image_url (string): Full web address for the teacher's image. [Are they always hosted on Insight Timer's website?]
- scrape_date (date_time): The date the teacher's information was scraped from their individual page on Insight Timer's website.