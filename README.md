# Online Job Portal | Database Management System + Full-Stack Web Application

![PHP](https://img.shields.io/badge/PHP-7.4%2B-blue?style=flat-square&logo=php)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue?style=flat-square&logo=mysql)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow?style=flat-square&logo=javascript)
![HTML5](https://img.shields.io/badge/HTML5-Markup-orange?style=flat-square&logo=html5)
![CSS3](https://img.shields.io/badge/CSS3-Styling-blue?style=flat-square&logo=css3)
![Bootstrap](https://img.shields.io/badge/Bootstrap-Frontend-purple?style=flat-square&logo=bootstrap)
![DBMS](https://img.shields.io/badge/DBMS-Relational%20Database-green?style=flat-square)
![Full-Stack](https://img.shields.io/badge/Full--Stack-Web%20App-black?style=flat-square)

---

## 📌 Project Overview

**Online Job Portal** is a full-stack web application demonstrating comprehensive database management system design and implementation. The project showcases a complete recruitment platform where job seekers and recruiters interact through a centralized digital marketplace, backed by a properly structured relational database.

**Key Highlights:**
- ✅ **Relational Database Design**: Normalized MySQL schema with ER modeling
- ✅ **Full-Stack Architecture**: PHP backend, JavaScript frontend, Bootstrap UI
- ✅ **User Role Management**: Job seekers, recruiters, administrators
- ✅ **Database Connectivity**: Direct backend-database integration
- ✅ **CRUD Operations**: Create, Read, Update, Delete all core entities
- ✅ **Production Workflow**: Job posting → Application → Management
- ✅ **Authentication System**: Secure login for multiple user roles
- ✅ **Portfolio-Ready**: Academic excellence with professional engineering

---

## 🎯 Why This Matters

Recruitment platforms face **complex database challenges**:

- **Data Integrity**: Managing thousands of job applicants safely
- **Relationship Modeling**: Recruiters → Jobs → Applications → Candidates
- **Scalability**: Supporting concurrent users and transactions
- **Query Optimization**: Fast search across millions of job records
- **ACID Compliance**: Reliable transaction handling
- **Security**: Protecting sensitive hiring information

This project demonstrates **professional-grade database engineering** in a real-world context.

---

## 🚀 Project Objectives

The project addresses key DBMS learning outcomes:

1. **Database Schema Design**: Normalized relational model with primary/foreign keys
2. **Entity-Relationship Modeling**: Visual ER diagrams showing entity relationships
3. **Application Integration**: Backend connectivity between web app and database
4. **Workflow Implementation**: Complete user journeys from signup to job matching
5. **Documentation Excellence**: Professional technical documentation
6. **Portfolio Development**: Industry-ready engineering project

---

## 👥 System Actors & Use Cases

### Job Seeker
- **Registration/Login**: Create account with credentials
- **Profile Management**: Update skills, education, experience
- **Job Search**: Filter and browse available positions
- **Apply for Jobs**: Submit applications with documents
- **Track Applications**: Monitor submission status
- **View Recommendations**: Get personalized job suggestions

### Recruiter/Employer
- **Authentication**: Secure recruiter login
- **Company Profile**: Set up organizational information
- **Post Jobs**: Create job listings with requirements
- **Manage Postings**: Edit, update, or close jobs
- **Review Applications**: View and filter candidate submissions
- **Analytics**: Assess application metrics

### Administrator
- **System Monitoring**: Track platform statistics
- **User Management**: Manage accounts and permissions
- **Data Maintenance**: Ensure database integrity
- **Moderation**: Review content and resolve issues
- **Reporting**: Generate platform analytics

---

## 🗃️ Database Design & Architecture

### Core Entities

| Entity | Purpose | Key Attributes |
|--------|---------|-----------------|
| **Users** | Universal user base | user_id, email, password_hash, created_at |
| **JobSeekers** | Candidate profiles | seeker_id, user_id, skills, experience |
| **Recruiters** | Employer accounts | recruiter_id, user_id, company_id |
| **Companies** | Organization data | company_id, name, industry, location |
| **Jobs** | Job postings | job_id, recruiter_id, title, description |
| **Applications** | Job submissions | application_id, seeker_id, job_id, status |
| **Skills** | Skill taxonomy | skill_id, skill_name, category |
| **Admin** | Administrator accounts | admin_id, user_id, permissions |

### Relationship Diagram (Conceptual)

```
Users (1) ──── (Many) JobSeekers
  │
  ├─── (1) JobSeeker ──── (Many) Applications
  │
  ├─── (1) Recruiter ──── (Many) Jobs
  │
  └─── (1) Recruiter ──── (1) Company

JobSeeker (Many) ──── (1) Application ──── (Many) Job (1) ──── (Many) JobSeeker
```

### Database Normalization
- **1NF**: Atomic values in all fields
- **2NF**: No partial dependencies on composite keys
- **3NF**: No transitive dependencies
- **BCNF**: Proper key constraints

### Key Constraints
- **Primary Keys**: Unique identification for each entity
- **Foreign Keys**: Referential integrity between tables
- **Unique Constraints**: Email, username uniqueness
- **Check Constraints**: Valid status values, date ranges

---

## 🛠️ Tech Stack

### Frontend
- **HTML5** - Semantic markup & structure
- **CSS3** - Modern styling with flexbox/grid
- **JavaScript (ES6)** - Client-side logic & interactivity
- **Bootstrap** - Responsive UI framework
- **Form Validation** - Client & server-side validation

### Backend
- **PHP 7.4+** - Server-side scripting language
- **OOP Principles** - Object-oriented PHP code
- **Session Management** - User authentication
- **Error Handling** - Try-catch exception handling
- **Input Sanitization** - SQL injection prevention

### Database
- **MySQL** - Relational database management system
- **SQL Queries** - Select, Insert, Update, Delete operations
- **Stored Procedures** - Encapsulated database logic
- **Indexes** - Query optimization
- **Transactions** - ACID compliance

### Architecture
- **MVC Pattern** - Model-View-Controller separation
- **RESTful Principles** - Standard HTTP methods
- **Database Connectivity** - PDO/MySQLi prepared statements
- **File Structure** - Modular code organization

---

## 📊 Application Architecture

### Layered Architecture

```
┌─────────────────────────────────────────┐
│        Frontend Layer (UI)              │
│  HTML5 | CSS3 | JavaScript | Bootstrap  │
└─────────────────────────────────────────┘
                    │
                    ↓
┌─────────────────────────────────────────┐
│      Application Logic Layer            │
│  Form Validation | Session Management   │
│  Authentication | Authorization         │
└─────────────────────────────────────────┘
                    │
                    ↓
┌─────────────────────────────────────────┐
│     Database Connectivity Layer         │
│  SQL Queries | CRUD Operations          │
│  Transaction Management                 │
└─────────────────────────────────────────┘
                    │
                    ↓
┌─────────────────────────────────────────┐
│    Database Layer (Persistence)         │
│  MySQL | Tables | Indexes | Views       │
└─────────────────────────────────────────┘
```

### Data Flow

```
User Input (Form)
       ↓
JavaScript Validation
       ↓
PHP Processing
       ↓
SQL Query Construction
       ↓
Database Execution
       ↓
Result Set Processing
       ↓
HTML Response Generation
       ↓
User Output (Browser)
```

---

## 📂 Project Structure

```
Online-Job-Portal/
│
├── README.md                           # Project documentation
├── docs/                               # Documentation folder
│   ├── database-design.md              # ER diagrams & schema
│   ├── requirements.md                 # Functional requirements
│   ├── architecture.md                 # System architecture
│   └── testing-plan.md                 # Test cases & strategy
│
├── database/                           # Database-related files
│   ├── schema.sql                      # Database structure
│   ├── sample-data.sql                 # Test data
│   └── ER-diagram.pdf                  # Entity-relationship diagram
│
├── system/                             # Application code
│   ├── index.php                       # Entry point
│   ├── auth/                           # Authentication modules
│   │   ├── login.php
│   │   ├── register.php
│   │   └── logout.php
│   ├── seeker/                         # Job seeker pages
│   │   ├── dashboard.php
│   │   ├── search-jobs.php
│   │   ├── apply-job.php
│   │   └── profile.php
│   ├── recruiter/                      # Recruiter pages
│   │   ├── dashboard.php
│   │   ├── post-job.php
│   │   ├── manage-jobs.php
│   │   └── view-applications.php
│   ├── admin/                          # Admin pages
│   │   ├── dashboard.php
│   │   └── manage-users.php
│   ├── assets/                         # CSS, JS, images
│   │   ├── css/
│   │   ├── js/
│   │   └── img/
│   ├── includes/                       # Shared includes
│   │   ├── db-connection.php           # Database connectivity
│   │   ├── functions.php               # Helper functions
│   │   ├── header.php
│   │   └── footer.php
│   └── config.php                      # Configuration file
│
└── assets/                             # Screenshots & diagrams
    ├── screenshots/
    ├── erd/
    └── wireframes/
```

---

## 🚀 Installation & Setup

### Prerequisites
```bash
✓ PHP 7.4 or higher
✓ MySQL 5.7 or higher
✓ Web server (Apache, Nginx, or built-in PHP server)
✓ Git for version control
```

### Step 1: Clone Repository
```bash
git clone https://github.com/ManamoyB/Online-Job-Portal.git
cd Online-Job-Portal
```

### Step 2: Database Setup
```bash
# Create database
mysql -u root -p

# In MySQL CLI:
CREATE DATABASE job_portal;
USE job_portal;

# Import schema
SOURCE database/schema.sql;

# (Optional) Load sample data
SOURCE database/sample-data.sql;
```

### Step 3: Configure Connection
Edit `system/config.php`:
```php
<?php
// Database configuration
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', 'your_password');
define('DB_NAME', 'job_portal');
?>
```

### Step 4: Run Application
```bash
# Option 1: Built-in PHP server
php -S localhost:8000

# Option 2: Apache/Nginx
# Configure virtual host pointing to 'system/' directory
```

Visit `http://localhost:8000` in your browser.

---

## 📋 Core Features & Workflows

### Job Seeker Workflow
```
1. Register Account
   ├─ Validate email uniqueness
   ├─ Hash password
   └─ Insert into database

2. Complete Profile
   ├─ Add skills
   ├─ Upload resume/CV
   └─ List experience

3. Search Jobs
   ├─ Filter by title, location, salary
   └─ View job details

4. Apply for Job
   ├─ Validate application
   ├─ Store in database
   └─ Send confirmation

5. Track Applications
   ├─ View all submissions
   ├─ Check status updates
   └─ Download offers
```

### Recruiter Workflow
```
1. Register Company
   ├─ Create recruiter account
   ├─ Set company details
   └─ Verify credentials

2. Post Job
   ├─ Fill job details
   ├─ Set requirements
   ├─ Add salary range
   └─ Publish listing

3. Manage Applications
   ├─ View all applicants
   ├─ Filter by status
   ├─ Download resumes
   └─ Send messages

4. Analytics
   ├─ View job statistics
   ├─ Track application metrics
   └─ Generate reports
```

---

## 🧠 DBMS Concepts Demonstrated

### 1. **Relational Database Design**
- Normalized schema (3NF)
- Entity relationship modeling
- Primary and foreign key constraints
- Data integrity rules

### 2. **SQL Operations**
- SELECT queries with WHERE, JOIN, GROUP BY
- INSERT for new records
- UPDATE for modifications
- DELETE with cascading
- Transactions for data consistency

### 3. **Database Optimization**
- Indexes on frequently queried columns
- Query performance analysis
- Connection pooling
- Caching strategies

### 4. **Security**
- Prepared statements (SQL injection prevention)
- Password hashing (bcrypt, SHA-256)
- Session management
- Role-based access control

### 5. **Transaction Management**
- ACID properties
- Rollback on errors
- Concurrent access handling
- Deadlock prevention

---

## 📊 Sample Queries

### Find all jobs matching a seeker's skills
```sql
SELECT j.*, COUNT(a.application_id) as application_count
FROM jobs j
INNER JOIN job_skills js ON j.job_id = js.job_id
INNER JOIN skills s ON js.skill_id = s.skill_id
INNER JOIN seeker_skills ss ON s.skill_id = ss.skill_id
WHERE ss.seeker_id = ?
GROUP BY j.job_id
ORDER BY j.posted_date DESC;
```

### Get recruiter's applications with candidate details
```sql
SELECT a.*, js.name, js.email, j.title
FROM applications a
INNER JOIN job_seekers js ON a.seeker_id = js.seeker_id
INNER JOIN jobs j ON a.job_id = j.job_id
WHERE j.recruiter_id = ?
ORDER BY a.application_date DESC;
```

### Analyze job posting statistics
```sql
SELECT 
  c.company_name,
  COUNT(j.job_id) as total_jobs,
  COUNT(a.application_id) as total_applications,
  AVG(a.rating) as avg_rating
FROM companies c
LEFT JOIN recruiters r ON c.company_id = r.company_id
LEFT JOIN jobs j ON r.recruiter_id = j.recruiter_id
LEFT JOIN applications a ON j.job_id = a.job_id
GROUP BY c.company_id;
```

---

## 🧪 Testing & Validation

### Database Testing
- **Schema Validation**: Verify all tables created correctly
- **Constraint Testing**: Ensure foreign key relationships
- **Query Testing**: Validate SQL correctness
- **Data Integrity**: Check ACID properties

### Application Testing
- **Unit Testing**: Individual function testing
- **Integration Testing**: Database + application layer
- **User Workflow Testing**: Complete journey testing
- **Security Testing**: Input validation, SQL injection checks

---

## 📈 Development Process

### Phase 1: Requirements Analysis
- Identified stakeholders (seekers, recruiters, admins)
- Defined functional requirements
- Created use case diagrams

### Phase 2: Database Design
- Conceptual modeling (ER diagram)
- Logical schema design
- Normalization to 3NF
- Index strategy planning

### Phase 3: System Architecture
- Defined layered architecture (3-tier)
- Planned separation of concerns
- Designed module structure

### Phase 4: Frontend Development
- HTML structure creation
- CSS styling with Bootstrap
- JavaScript interactivity
- Form validation

### Phase 5: Backend Development
- PHP controller logic
- Database connectivity layer
- CRUD operation implementation
- Session management

### Phase 6: Integration & Testing
- Connected frontend to backend
- Database integration testing
- User workflow validation
- Performance optimization

### Phase 7: Documentation
- Created technical documentation
- Prepared ER diagrams
- Documented API endpoints
- Generated user guides

---

## 🎓 Key Learning Outcomes

This project teaches:

1. **Database Modeling**: Designing normalized relational schemas
2. **SQL Mastery**: Complex queries, transactions, indexing
3. **Full-Stack Development**: Frontend + backend + database
4. **Web Architecture**: MVC pattern, layered design
5. **Security**: Authentication, password hashing, input validation
6. **PHP Programming**: OOP, file handling, form processing
7. **Front-End Skills**: HTML5, CSS3, JavaScript, Bootstrap
8. **Project Management**: Documentation, version control, testing

---

## 🚀 Future Enhancements

- [ ] **Resume Upload** - PDF/DOC file management
- [ ] **Email Notifications** - Application status updates
- [ ] **AI Recommendations** - Job matching algorithm
- [ ] **Interview Scheduling** - Calendar integration
- [ ] **Skill Verification** - Skill assessment tests
- [ ] **Analytics Dashboard** - Advanced reporting
- [ ] **Payment Integration** - Premium job posting
- [ ] **Mobile App** - React Native version
- [ ] **API Development** - RESTful API for mobile
- [ ] **Microservices** - Scalable architecture
- [ ] **Real-time Chat** - Recruiter-candidate messaging
- [ ] **Video Interviews** - Built-in interviewing tool

---

## ⚠️ Important Notes

### Academic Purpose
This project is designed for **educational learning** and demonstrates:
- University-level database design
- Full-stack development practices
- Professional code organization
- Engineering documentation

### Production Readiness
For production deployment, consider:
- Upgrading to modern frameworks (Laravel, Node.js)
- Implementing caching (Redis)
- Adding microservices architecture
- Setting up CI/CD pipelines
- Cloud deployment (AWS, GCP, Azure)

---

## 💻 Technology Stack Summary

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend** | HTML5, CSS3, JavaScript, Bootstrap | User interface |
| **Backend** | PHP 7.4+ | Server-side logic |
| **Database** | MySQL | Data persistence |
| **Architecture** | MVC, 3-tier layered | Code organization |
| **Security** | PDO, hashing, sessions | Data protection |

---

## 📞 Contact & Support

**Author:** Manamoy Banerjee

**Connect:**
- **GitHub**: [@ManamoyB](https://github.com/ManamoyB)
- **LinkedIn**: [Manamoy's Profile](https://linkedin.com/in/your-profile)
- **Email**: [your.email@example.com]

**Questions or Issues:**
- Open a [GitHub Issue](https://github.com/ManamoyB/Online-Job-Portal/issues)
- Check `docs/` folder for detailed documentation
- Review database schema for data model understanding

---

## 📄 License

This is an academic/portfolio project for educational purposes.

---

## ⭐ If This Helped You

If you found this project useful:
- ⭐ **Star** this repository
- 🍴 **Fork** to build your own portal
- 💬 **Share** with your network
- 📧 **Mention** in your portfolio/resume

---

## 🙌 Credits & Acknowledgments

- **University Faculty** - Project guidelines & mentorship
- **MySQL Documentation** - Database reference
- **PHP Community** - Framework & best practices
- **Bootstrap Team** - UI framework
- **Open Source Community** - Tools & libraries

---

**Last Updated:** June 2026 | **Status:** Academic Portfolio | **PHP 7.4+** | **MySQL 5.7+**
