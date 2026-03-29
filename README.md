# 📊 Social Media Analytics Dashboard (Flask + MySQL)

A web-based **Social Media Analytics Dashboard** built using **Flask, MySQL, and HTML** that allows users to manage social media data and analyze engagement metrics like likes, comments, and shares.

---

## 🚀 Features

* 👤 Add new users
* 📝 Create posts
* ❤️ Track engagement (likes, comments, shares)
* 📊 Dashboard with analytics:

  * Total users
  * Total posts
  * Average engagement
* 🗄️ MySQL database integration

---

## 🧠 How It Works

1. Users submit data via web forms
2. Flask processes requests and updates database
3. Data is stored in MySQL tables
4. Dashboard dynamically displays analytics

---

## 📂 Project Structure

```id="w82lq1"
📁 Social-Media-Dashboard
│── app.py                 # Main Flask application
│── templates/             # HTML files
│    ├── index.html
│── static/                # CSS / JS (optional)
│── README.md
```

---

## ⚙️ Requirements

Install dependencies:

```bash id="q2k9sd"
pip install flask pymysql
```

---

## 🗄️ Database Setup (MySQL)

Create database:

```sql id="x7d3ks"
CREATE DATABASE socialmedia;
USE socialmedia;
```

---

### 📌 Create Tables

```sql id="c8d2ks"
CREATE TABLE users (
    user_id INT PRIMARY KEY,
    username VARCHAR(100),
    email VARCHAR(100),
    country VARCHAR(50),
    join_date DATE
);

CREATE TABLE posts (
    post_id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT,
    content TEXT,
    post_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    hashtags VARCHAR(255)
);

CREATE TABLE engagement (
    id INT AUTO_INCREMENT PRIMARY KEY,
    post_id INT,
    likes INT,
    comments INT,
    shares INT
);
```

---

## ▶️ Run the Project

```bash id="r6p2ks"
python app.py
```

Then open:

```id="t4o9ks"
http://127.0.0.1:5000/
```

---

## 📊 Dashboard Metrics

* 👤 Total Users
* 📝 Total Posts
* 📈 Average Engagement

  * Calculated as:
    `(likes + comments + shares) / total entries`

---

## ⚠️ Notes

* MySQL server must be running
* Update database credentials in `app.py` if needed
* Basic validation implemented
* For learning/demo purposes

---

## 🔧 Future Improvements

* User authentication system
* Data visualization charts (graphs)
* REST API support
* Responsive UI (Bootstrap)
* Deployment on cloud

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a branch
3. Make changes
4. Submit a pull request

---

## 📜 License

This project is licensed under the MIT License.

---

## 💡 Author

**Pavan Gopi Nadh Ganapathi**
🔗 GitHub: https://github.com/Pavangopi931

---

## 🙌 Acknowledgements

* Flask for backend framework
* MySQL for database
* HTML/CSS for frontend

---
