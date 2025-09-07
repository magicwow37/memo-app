---
task_id: 07
title: JSON Export Functionality
epic: memo-app
status: pending
priority: low
estimated_hours: 1
dependencies: [06]
---

# Task 07: JSON Export Functionality

## Description
Implement JSON export feature to allow users to backup and download their memo data.

## Acceptance Criteria
- [ ] Create export route that generates JSON of all memos
- [ ] Include all memo fields in export (id, title, content, tags, date)
- [ ] Format JSON with proper structure and indentation
- [ ] Serve JSON as downloadable file with appropriate filename
- [ ] Add export button/link in main navigation or memo list
- [ ] Handle empty database case gracefully

## Implementation Details
1. Export Function:
   - Query all memos from database
   - Convert database rows to JSON format
   - Include timestamp in export filename
   - Set appropriate headers for file download

2. JSON Structure:
   ```json
   {
     "export_date": "2025-09-07T01:39:52Z",
     "memo_count": 5,
     "memos": [
       {
         "id": 1,
         "title": "Sample Memo",
         "content": "Content here...",
         "tags": ["tag1", "tag2"],
         "created_at": "2025-09-07T01:30:00Z"
       }
     ]
   }
   ```

3. UI Integration:
   - Add export button to main navigation
   - Use appropriate icon and styling
   - Show confirmation or feedback after export

## Definition of Done
- Export generates valid JSON with all memo data
- File downloads correctly with meaningful filename
- Export works with empty database
- Export button is easily accessible to users
- JSON structure is well-formatted and complete