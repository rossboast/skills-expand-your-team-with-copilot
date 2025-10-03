# How to Request Changes

As a teacher at Mergington High School, you can request changes to the activities management system without needing to modify code directly. This guide explains how to use issue templates to submit clear, actionable requests.

## Available Issue Templates

When you create a new issue on GitHub, you'll see several templates to choose from. Each template is designed for a specific type of request.

### 1. Add New Activity/Club

**Use this when:** You want to add a new extracurricular activity or club to the system.

**What you'll provide:**
- Activity name (e.g., "Drama Club", "Yoga Class")
- Description of what students will do
- Days it will meet (Monday-Sunday)
- Start and end times (in 24-hour format)
- Maximum number of participants
- Any additional information (materials, prerequisites, etc.)

**Example:** Adding a new "Creative Writing Workshop" that meets on Wednesdays from 3:30-5:00 PM with a capacity of 15 students.

### 2. Update Existing Activity

**Use this when:** You need to change details of an activity that already exists.

**What you'll provide:**
- Which activity to update
- What needs to change (description, schedule, capacity, etc.)
- New values for the fields being updated
- Reason for the change

**Example:** Changing Chess Club's schedule from Monday/Friday to Tuesday/Thursday because of a room conflict.

### 3. Bug Report

**Use this when:** Something isn't working correctly in the system.

**What you'll provide:**
- Description of what's not working
- What should happen instead
- Steps to reproduce the problem
- Which part of the system is affected
- How severe the issue is
- Any error messages you see

**Example:** "Students can't register for Soccer Team even though spots are available - clicking Register Student shows an error."

### 4. Feature Request

**Use this when:** You want to suggest a new feature or capability.

**What you'll provide:**
- Description of the feature
- Problem it would solve
- Area of the system it affects
- Who would benefit
- How you envision it working
- How important it is

**Example:** "Add a print-friendly roster view so teachers can print class lists for each activity."

### 5. UI/UX Improvement

**Use this when:** You want to suggest improvements to how the system looks or works.

**What you'll provide:**
- Type of improvement (visual, layout, navigation, etc.)
- Current experience
- Proposed improvement
- Which pages are affected
- Who is affected
- Why it's important

**Example:** "Make activity cards easier to read by increasing font size and improving color contrast."

## Time Format Guide

When entering times in templates, use 24-hour format (HH:MM):

- 7:00 AM = `07:00`
- 8:30 AM = `08:30`
- 12:00 PM = `12:00`
- 3:30 PM = `15:30`
- 5:00 PM = `17:00`
- 8:00 PM = `20:00`

## Tips for Writing Good Issue Requests

1. **Be specific:** Instead of "Make Chess Club better", say "Increase Chess Club capacity from 12 to 20 students"

2. **Provide context:** Explain why the change is needed - "We have a waiting list of 15 students"

3. **Include examples:** If requesting a new feature, describe exactly how you'd use it

4. **One issue per request:** Don't combine multiple unrelated requests in one issue

5. **Fill in all required fields:** This helps the Copilot coding agent understand exactly what you need

## What Happens After You Submit

1. Your issue will be automatically labeled based on the template you used
2. The issue will include acceptance criteria (how we'll know it's done correctly)
3. The issue will include implementation guidance for developers
4. A developer or Copilot coding agent can be assigned to complete the work
5. You'll be notified when the issue is completed

## Need Help?

- Check the [Development Guide](./how-to-develop.md) for technical information about the system
- Not sure which template to use? Start with the Bug Report or Feature Request template and describe your need - someone can help categorize it
- For urgent issues, contact the system administrator directly

## Examples

### Good Issue Title Examples
- ✅ "[New Activity]: Add Robotics Club - Saturdays 9:00-12:00"
- ✅ "[Update Activity]: Change Drama Club schedule to Thursdays"
- ✅ "[Bug]: Can't unregister students from Basketball Team"
- ✅ "[Feature]: Add email notifications for activity updates"
- ✅ "[UI/UX]: Improve mobile view of activity filters"

### Poor Issue Title Examples
- ❌ "Problem with activities"
- ❌ "Need help"
- ❌ "Change things"
- ❌ "Bug"

The more detail you provide, the faster and more accurately your request can be implemented!
