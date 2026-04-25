## Cricinfo Management System (OOP-Based Cricket Application)

### Overview

This project is a console-based Cricinfo Management System developed using Object-Oriented Programming principles. It simulates a real-world cricket information platform where users can manage players, teams, matches, rankings, and cricket-related news.

The system is designed to mimic how professional cricket databases operate, including live match tracking, player statistics updates, team management, and tournament scheduling.

Everything is implemented in a single codebase (single file), keeping the structure simple but functionally rich.

---

### Purpose

The goal of this project is to apply advanced OOP concepts in a meaningful way while building a system that manages cricket data dynamically. It demonstrates how real-world sports applications handle complex data like player stats, match results, rankings, and scheduling.

It is not just a CRUD system—it behaves like a mini cricket information engine.

---

### Core Features

* Player management system (add, update, delete, search)
* Team management with admin authentication
* Match scheduling and simulation
* Tournament handling
* Live updates of player and team statistics
* ICC ranking updates
* World record tracking
* News browsing for matches and tournaments
* File handling for persistent data storage

---

### Technologies Used

* C++ (Object-Oriented Programming)
* File Handling (for persistent storage)
* Pointers and Dynamic Memory Allocation
* OOP Concepts: Inheritance, Composition, Aggregation, Encapsulation, Abstraction
* Single-file implementation (all code integrated in one source file)

---

### System Design (OOP Structure)

#### 1. Player Class (Abstract Base Class)

This class represents a cricket player and serves as the foundation of the system.

**Attributes:**

* Name
* Shirt Number
* Average
* ICC Ranking (different formats like T20, ODI, etc.)
* Total Runs
* Matches Played
* Total Wickets
* Additional identification attributes (customized)

**Functions:**

* addPlayer()
* removePlayer()
* searchPlayer()
* updatePlayer()

This class focuses on individual performance tracking and serves as the base for team-level operations.

---

#### 2. Team Class (Inherits Player Class)

The Team class extends player-related functionality and manages team-level operations.

**Attributes:**

* Team Name
* ICC Ranking
* Number of Players
* Matches Won / Lost
* Captain
* Coach
* Admin Username / Password
* Additional team-specific attributes

**Functions:**

* addPlayer()
* removePlayer()
* searchPlayer()
* updatePlayer()
* displayMatches()
* updateCaptain()
* updateCoach()
* displayTeam()

**Key Idea:**
The team class can access player details and analyze performance across matches and tournaments.

Also includes admin login system before performing operations. No login, no control.

---

#### 3. Match Class

This class manages all match-related operations including scheduling, conducting, and updating records.

**Attributes:**

* Team 1
* Team 2
* Date
* Venue
* Match Type (ODI, T20, etc.)
* Tournament Name
* Commentators
* Umpires
* Match Status (upcoming / recent)
* Additional match metadata

**Functions:**

* conductMatch()
* scheduleMatch()
* updateWorldRecords()
* updateTeamRanking()
* updatePlayerRanking()
* displayUpcomingMatches()
* displayRecentMatches()

---

### Project Flow

#### 1. System Start

The application starts from a main menu where the user selects between:

* Player Management
* Team Management
* Match Management
* News and Rankings

---

#### 2. Player Module

* Users can add new players
* Search existing players
* Update stats like runs, wickets, and rankings
* Remove players if required
* All updates are stored using file handling

Basically, this module behaves like a live cricket database for individual performance.

---

#### 3. Team Module

* Requires admin login (username + password)
* After authentication, full control is granted
* Admin can manage players inside the team
* Update captain and coach
* View team details and performance
* Analyze match history

This is where inheritance and aggregation are heavily used.

---

#### 4. Match Module

Two possible flows:

##### A. Conduct Existing Match

* System shows scheduled matches
* User selects a match
* Match is conducted
* Results are generated
* Player and team stats are updated automatically

##### B. Schedule New Match

* System shows available teams
* User selects at least two teams
* Match details are entered (venue, date, type, tournament)
* Match is stored as upcoming

For tournaments:

* Multiple teams are selected
* Matches are organized under a tournament name

---

#### 5. Post-Match Processing

After every match:

* Player stats are updated
* Team rankings are recalculated
* ICC rankings are adjusted
* World records are checked and updated

Records tracked include:

* Most runs
* Highest score
* Most sixes and fours
* Centuries
* Batting average
* Bowling performance

---

#### 6. News & Information System

Users can:

* View recent match summaries
* Check upcoming schedules
* Access cricket-related updates
* Search ICC rankings by team or player

This module acts like a simplified Cricinfo news feed.

---

### File Handling System

All major data is stored using file handling:

* Player records
* Team data
* Match history
* Rankings

This ensures data persistence even after program restart.

---

### Key OOP Concepts Used

* **Inheritance:** Team inherits Player functionality
* **Encapsulation:** Data protected inside classes
* **Abstraction:** Complex match logic hidden from user
* **Composition:** Teams composed of multiple players
* **Aggregation:** Matches linked with teams and players
* **Pointers & DMA:** Used for dynamic memory handling
* **File Handling:** Persistent storage system

---

### Project Structure Note

All code is implemented in a **single source file**, as per requirement. While this is not ideal for large-scale systems, it keeps the project compact and easy to compile and test.

Yes, it’s one file—but it behaves like a mini cricket universe.

---

### Challenges Faced

* Managing synchronization between players, teams, and matches
* Updating rankings dynamically after every match
* Designing realistic match flow logic
* Handling file consistency
* Keeping OOP structure clean in a single file

---

### Future Improvements

* Convert into multi-file modular project
* Add GUI interface
* Integrate real cricket API data
* Add authentication system with encryption
* Implement live match simulation engine
* Add database instead of file handling

---

### Conclusion

This project demonstrates a strong application of Object-Oriented Programming concepts in a real-world inspired system. It successfully simulates core functionalities of a cricket management platform including players, teams, matches, rankings, and news updates.
