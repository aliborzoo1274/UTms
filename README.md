# UTms - University Management System

A command-line based university of Tehran management system implemented in C++ that simulates academic operations including course management, user authentication, and social networking features for students and professors.

## 📋 Overview

UTms is a comprehensive system designed to manage university operations with support for multiple user roles, course offerings, notifications, and social interactions. This project was developed as part of an Advanced Programming course (Assignment 6).

## ✨ Features

### User Management
- **Multiple User Types**: Support for Students, Professors, and Admins
- **Authentication System**: Secure login/logout functionality
- **User Profiles**: Personal pages with profile photos and posts
- **Social Connections**: Users can connect with each other

### Course Management
- **Course Offerings**: Professors can offer courses
- **Course Enrollment**:  Students can register for courses
- **Course Channels**: Communication channels for each course
- **Course Posts**: Dedicated posting system for course-related content
- **TA Management**: 
  - TA form creation and management
  - TA request submission
  - TA form closure

### Communication & Notifications
- **Post System**: Users can create and delete posts
- **Notifications**: Real-time notification system
- **Course Channels**: Dedicated communication channels per course

## 🏗️ Project Structure

```
UTms/
├── include/           # Header files
│   ├── admin.hpp
│   ├── course.hpp
│   ├── global.hpp
│   ├── major. hpp
│   ├── person.hpp
│   ├── professor.hpp
│   ├── read_files.hpp
│   ├── student.hpp
│   ├── system.hpp
│   └── user.hpp
├── src/              # Source files
│   ├── admin.cpp
│   ├── course.cpp
│   ├── delete. cpp
│   ├── get. cpp
│   ├── main.cpp
│   ├── major.cpp
│   ├── person.cpp
│   ├── post.cpp
│   ├── professor.cpp
│   ├── put.cpp
│   ├── read_files.cpp
│   ├── student.cpp
│   ├── system.cpp
│   └── user.cpp
├── build/            # Build output directory
├── files/            # Data files (CSV/text inputs)
├── Makefile          # Build configuration
└── README.md
```

## 🛠️ Technologies

- **Language**: C++ (C++17 standard)
- **Compiler**: g++
- **Build System**: Makefile
- **Architecture**: Object-Oriented Programming with inheritance

## 📦 Installation & Building

### Prerequisites
- g++ compiler with C++17 support
- Make utility

### Building the Project

1. Clone the repository: 
```bash
git clone https://github.com/aliborzoo1274/UTms.git
cd UTms
```

2. Build using Make:
```bash
make
```

3. Run the executable:
```bash
./utms.exe
```

### Clean Build Files
```bash
make clean
```

## 🎮 Usage

The system operates through command-line interface with REST-like commands: 

### Available Commands

#### GET Methods
- `GET courses` - View all available courses
- `GET personal_page ? id <user_id>` - View a user's profile
- `GET post ?id <user_id> ? post_id <post_id>` - View a specific post
- `GET notification` - Check notifications
- `GET my_courses` - View enrolled courses
- `GET course_channel ?id <course_id>` - Access course channel
- `GET course_post ?id <course_id> ?post_id <post_id>` - View course post

#### POST Methods
- `POST login ? id <id> ?password <password>` - User login
- `POST logout` - User logout
- `POST post ?title <title> ?message <message>` - Create a post
- `POST connect ?id <user_id>` - Connect with another user
- `POST course_offer ?course_id <id> ... ` - Offer a course (Professor)
- `POST profile_photo ?photo <path>` - Update profile photo
- `POST course_post ?id <course_id> ... ` - Create course post
- `POST ta_form ?course_id <id> ?message <msg>` - Create TA form
- `POST ta_request ?course_id <id> ?professor_id <id>` - Request TA position
- `POST close_ta_form ?course_id <id>` - Close TA form

#### PUT Methods
- `PUT my_courses ? id <course_id>` - Enroll in a course

#### DELETE Methods
- `DELETE post ?id <post_id>` - Delete a post
- `DELETE my_courses ?id <course_id>` - Drop a course

## 🏛️ System Architecture

### Class Hierarchy
```
Person (Base Class)
├── User
│   ├── Student
│   ├── Professor
│   └── Admin
├── Major
└── Course
```

### Key Components
- **System**: Main controller managing all operations
- **File Reading**: CSV/text file parsing for initial data
- **Authentication**: Login/logout with session management
- **Course Management**:  Offering, enrollment, and TA systems
- **Social Features**: Posts, connections, and notifications

## 📄 Documentation

Detailed project specifications are available in: 
- `APS03-A6.1-Description.pdf` - Phase 1 specifications
- `APS03-A6.2-Description.pdf` - Phase 2 specifications

## 👨‍💻 Author

**aliborzoo1274**
- GitHub: [@aliborzoo1274](https://github.com/aliborzoo1274)

---

*This project was developed as part of the Advanced Programming Course (Assignment 6)*