---
task_id: 02
title: Database Schema and CRUD Operations
epic: memo-app
status: pending
priority: high
estimated_hours: 2
dependencies: [01]
---

# Task 02: Database Schema and CRUD Operations

## Description
Create SQLite database schema and implement CRUD operations for memo management.

## Acceptance Criteria
- [ ] Design and create SQLite database schema
- [ ] Implement database connection handling
- [ ] Create memo data model/class
- [ ] Implement Create operation (insert memo)
- [ ] Implement Read operations (get all, get by id)
- [ ] Implement Update operation (modify memo)
- [ ] Implement Delete operation (remove memo)
- [ ] Add error handling for database operations

## Implementation Details
1. Database Schema:
   ```sql
   CREATE TABLE memos (
       id INTEGER PRIMARY KEY AUTOINCREMENT,
       title TEXT NOT NULL,
       content TEXT NOT NULL,
       tags TEXT, -- JSON string for tag array
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
   ```

2. Database Functions:
   - `init_db()` - Initialize database and create tables
   - `get_db_connection()` - Handle database connections
   - `create_memo(title, content, tags)` - Insert new memo
   - `get_all_memos()` - Retrieve all memos
   - `get_memo_by_id(id)` - Retrieve specific memo
   - `update_memo(id, title, content, tags)` - Update existing memo
   - `delete_memo(id)` - Remove memo

## Definition of Done
- Database schema is created successfully
- All CRUD operations work without errors
- Database connection is properly managed
- Error handling prevents application crashes