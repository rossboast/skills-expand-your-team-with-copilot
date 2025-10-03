# Issue Template Examples

This document shows examples of what teachers will see when using the issue templates.

## What Teachers See

When a teacher clicks "New Issue" in GitHub, they will see a list of template options:

```
Choose a template:
├─ 🎯 Add New Activity/Club
│  Request a new extracurricular activity or club to be added to the system
│
├─ ✏️ Update Existing Activity
│  Request changes to an existing activity's details (schedule, description, capacity, etc.)
│
├─ 🐛 Bug Report
│  Report a problem with the activities management system
│
├─ ✨ Feature Request
│  Suggest a new feature or enhancement for the activities management system
│
└─ 🎨 UI/UX Improvement
   Suggest improvements to the user interface or user experience
```

## Example 1: Adding a New Activity

**Template:** Add New Activity/Club

**What the teacher fills in:**
- **Activity/Club Name:** "Creative Writing Workshop"
- **Activity Description:** "Students explore creative writing techniques, work on short stories and poetry, and share their work with peers in a supportive environment."
- **Days:** [Wednesday] (from dropdown)
- **Start Time:** "15:30"
- **End Time:** "17:00"
- **Maximum Participants:** "15"
- **Additional Information:** "Students should bring a notebook. All skill levels welcome."

**What gets created:**
```markdown
## Activity/Club Name
Creative Writing Workshop

## Activity Description
Students explore creative writing techniques, work on short stories and poetry, 
and share their work with peers in a supportive environment.

## Which days will this activity meet?
Wednesday

## Start Time
15:30

## End Time
17:00

## Maximum Participants
15

## Additional Information
Students should bring a notebook. All skill levels welcome.

---
## Acceptance Criteria

When this issue is completed:
- The new activity should appear in the activities list on the website
- Students should be able to register for the activity
- The activity should have the correct schedule, description, and participant limit
- The activity should be filterable by day and time

## Implementation Notes

For developers: Add the new activity to the `initial_activities` dictionary in 
`src/backend/database.py`. Ensure:
- The activity name is used as the key
- Include all required fields: `description`, `schedule`, `schedule_details`, 
  `max_participants`, and `participants` (initially empty list)
- The `schedule_details` object must include `days` (array), `start_time`, and `end_time`
- Format times in 24-hour format (HH:MM)
```

**Labels added:** `enhancement`, `activity`

---

## Example 2: Reporting a Bug

**Template:** Bug Report

**What the teacher fills in:**
- **What's not working?:** "Students cannot register for Basketball Team even though there are 5 spots available"
- **What should happen instead?:** "Teachers should be able to click 'Register Student', enter a student email, and successfully add them to the team"
- **Steps to Reproduce:**
  ```
  1. Log in as a teacher (username: mchen)
  2. Scroll to Basketball Team activity
  3. Click 'Register Student' button
  4. Enter email: newstudent@mergington.edu
  5. Click Submit
  6. See error message "Failed to sign up"
  ```
- **Affected Area:** "Student Registration" (from dropdown)
- **Severity:** "High - Major feature is broken" (from dropdown)
- **Affected Activity:** "Basketball Team"
- **Error Messages:** "Failed to sign up. Please try again."
- **Browser:** "Chrome"

**What gets created includes:**
```markdown
## What's not working?
Students cannot register for Basketball Team even though there are 5 spots available

## What should happen instead?
Teachers should be able to click 'Register Student', enter a student email, 
and successfully add them to the team

## Steps to Reproduce
1. Log in as a teacher (username: mchen)
2. Scroll to Basketball Team activity
3. Click 'Register Student' button
4. Enter email: newstudent@mergington.edu
5. Click Submit
6. See error message "Failed to sign up"

## What part of the system is affected?
Student Registration

## How severe is this bug?
High - Major feature is broken

[... more fields ...]

---
## Acceptance Criteria

When this issue is resolved:
- The described problem should no longer occur
- All related functionality should work as expected
- The fix should not break any existing features
- Similar edge cases should be considered and tested

## Investigation Tips

For developers:
- Check browser console for JavaScript errors
- Review API responses in the Network tab
- Test with the FastAPI interactive docs at `/docs`
- Review relevant backend logs
- Check database state if data-related
- Consider authentication/authorization issues
- Look for similar issues in the codebase
```

**Labels added:** `bug`

---

## Example 3: Updating an Activity

**Template:** Update Existing Activity

**What the teacher fills in:**
- **Activity Name:** "Chess Club" (from dropdown)
- **What needs to be updated?:** 
  - ☑️ Schedule (days)
  - ☑️ Maximum participant capacity
- **New Schedule Days:** [Tuesday, Thursday]
- **New Maximum Participants:** "20"
- **Reason for Change:** "We have acquired a larger room and can accommodate more students. Moving to Tuesday/Thursday to avoid conflicts with other clubs."

**What gets created includes:**
```markdown
## Activity/Club Name
Chess Club

## What needs to be updated?
- Schedule (days)
- Maximum participant capacity

## New Schedule Days (if applicable)
Tuesday, Thursday

## New Maximum Participants (if applicable)
20

## Reason for Change
We have acquired a larger room and can accommodate more students. Moving to 
Tuesday/Thursday to avoid conflicts with other clubs.

---
## Acceptance Criteria

When this issue is completed:
- The activity should display the updated information on the website
- All existing student registrations should be preserved
- The activity should still be filterable and searchable correctly
- Updated schedule times should be reflected in filters

## Implementation Notes

For developers: Update the activity in the `initial_activities` dictionary in 
`src/backend/database.py`. Make sure to:
- Only modify the specific fields mentioned in the request
- Preserve the existing `participants` array
- Update both the human-readable `schedule` string and the `schedule_details` object
- Format times consistently in 24-hour format (HH:MM)
```

**Labels added:** `enhancement`, `activity`

---

## Example 4: Feature Request

**Template:** Feature Request

**What the teacher fills in:**
- **Feature Description:** "Add ability to export student rosters to CSV format"
- **Problem it solves:** "Teachers need to print attendance sheets and currently have to manually copy student names"
- **Feature Area:** "Data Export/Import"
- **Who benefits:** [Teachers]
- **Proposed Solution:**
  ```
  1. Add an "Export Roster" button on each activity card
  2. Generate CSV file with columns: Student Email, Activity Name, Date Registered
  3. Auto-download the file to teacher's computer
  ```
- **Priority:** "Medium - Nice to have, would be useful"

**What gets created includes:**
```markdown
## Feature Description
Add ability to export student rosters to CSV format

## What problem does this solve?
Teachers need to print attendance sheets and currently have to manually copy student names

## What area of the system is this for?
Data Export/Import

## Who would benefit from this feature?
Teachers

## Proposed Solution
1. Add an "Export Roster" button on each activity card
2. Generate CSV file with columns: Student Email, Activity Name, Date Registered
3. Auto-download the file to teacher's computer

## How important is this feature?
Medium - Nice to have, would be useful

---
## Acceptance Criteria

For developers, when implementing this feature:
- The feature should work as described in the proposed solution
- It should integrate seamlessly with existing functionality
- The user experience should be intuitive and require minimal training
- The feature should be responsive and work on different screen sizes
[... more criteria ...]
```

**Labels added:** `enhancement`

---

## Example 5: UI/UX Improvement

**Template:** UI/UX Improvement

**What the teacher fills in:**
- **Type:** "Visual Design (colors, fonts, spacing)"
- **Current Experience:** "Activity card text is too small and hard to read, especially the participant count"
- **Proposed Improvement:** "Increase base font size from 14px to 16px, make participant count more prominent with bold text"
- **Affected Pages:** [Activity Details Cards]
- **User Impact:** [All users]
- **Device Type:** [All devices]
- **Why Important:** "Better readability reduces eye strain and makes information easier to scan quickly"
- **Design Suggestions:**
  ```
  .activity-card {
    font-size: 16px; /* currently 14px */
  }
  .activity-card .participants {
    font-weight: bold;
    font-size: 18px;
  }
  ```

**What gets created includes:**
```markdown
## Type of Improvement
Visual Design (colors, fonts, spacing)

## Current Experience
Activity card text is too small and hard to read, especially the participant count

## Proposed Improvement
Increase base font size from 14px to 16px, make participant count more prominent 
with bold text

[... more fields ...]

## Specific Design Suggestions
.activity-card {
  font-size: 16px; /* currently 14px */
}
.activity-card .participants {
  font-weight: bold;
  font-size: 18px;
}

---
## Acceptance Criteria

When this improvement is implemented:
- The visual change should be consistent across all relevant pages
- The improvement should enhance usability without breaking existing functionality
- The design should remain consistent with the overall site aesthetic
[... more criteria ...]
```

**Labels added:** `enhancement`, `ui/ux`

---

## Key Benefits

### For Teachers
- ✅ No need to know technical details
- ✅ Clear, structured forms with examples
- ✅ Helpful placeholders guide input
- ✅ Can't forget important details (required fields)

### For Developers
- ✅ Consistent information structure
- ✅ All necessary details provided upfront
- ✅ Clear acceptance criteria
- ✅ Implementation guidance included

### For Copilot Coding Agent
- ✅ Structured data easy to parse
- ✅ Specific file locations referenced
- ✅ Clear success criteria
- ✅ Context and constraints provided

## How to Use

1. Go to the repository Issues tab
2. Click "New Issue"
3. Select the appropriate template
4. Fill in the form (required fields marked with asterisk)
5. Click "Submit new issue"
6. Issue can be assigned to Copilot or a developer

For detailed guidance, see [How to Request Changes](./how-to-request-changes.md).
