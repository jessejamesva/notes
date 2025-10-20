# Quiz App Setup

1. Create database and user:

```sql
CREATE DATABASE quizgame_db;
CREATE USER 'quizuser'@'localhost' IDENTIFIED BY 'StrongPassword123!';
GRANT ALL PRIVILEGES ON quizgame_db.* TO 'quizuser'@'localhost';
FLUSH PRIVILEGES;
```

2. Create tables:

```sql
CREATE TABLE quizzes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  question TEXT NOT NULL,
  option_a VARCHAR(255),
  option_b VARCHAR(255),
  option_c VARCHAR(255),
  option_d VARCHAR(255),
  correct_option CHAR(1)
);
```

3. Insert sample data:

```sql
INSERT INTO quizzes (question, option_a, option_b, option_c, option_d, correct_option)
VALUES ('What command initializes a new Git repository?', 'git start', 'git init', 'git create', 'git new', 'B');
```

4. Test PHP connection:

```php
<?php
$servername = "localhost";
$username = "quizuser";
$password = "StrongPassword123!";
$dbname = "quizgame_db";
$conn = new mysqli($servername, $username, $password, $dbname);
if ($conn->connect_error) { die("Connection failed: " . $conn->connect_error); }
echo "✅ Connected to MariaDB successfully!<br>";
$sql = "SELECT question FROM quizzes LIMIT 1";
$result = $conn->query($sql);
while($row = $result->fetch_assoc()) { echo "Sample question: " . $row["question"]; }
$conn->close();
?>
```

_Screenshot placeholder: screenshots/dbtest-success.png_
