# Issue Templates Overview

This document provides an overview of the issue templates available for the Mergington High School Activities Management System.

## Purpose

These templates simplify the process for teachers to request changes without needing to modify code directly. Each template ensures that sufficient details are collected so that the Copilot coding agent can easily understand and complete the task without further explanation.

## Templates Available

### 1. Add New Activity/Club (`add-activity.yml`)

**Purpose:** Request a new extracurricular activity or club

**Required Information:**
- Activity/Club Name
- Activity Description
- Days of the week (multi-select)
- Start Time (24-hour format)
- End Time (24-hour format)
- Maximum Participants

**Optional Information:**
- Additional details (materials, prerequisites, location)

**Labels:** `enhancement`, `activity`

**Key Features:**
- Clear acceptance criteria for completion
- Implementation guidance pointing to `src/backend/database.py`
- Specific field requirements for the database structure

### 2. Update Existing Activity (`update-activity.yml`)

**Purpose:** Modify existing activity details

**Required Information:**
- Activity name (dropdown of existing activities)
- What needs updating (checkboxes)
- Reason for change

**Optional Information:**
- New description
- New schedule days
- New start/end times
- New max participants
- Other changes

**Labels:** `enhancement`, `activity`

**Key Features:**
- Dropdown pre-populated with known activities
- Preserves existing participant data
- Clear guidance on partial updates

### 3. Bug Report (`bug-report.yml`)

**Purpose:** Report system issues

**Required Information:**
- Problem description
- Expected behavior
- Steps to reproduce
- Affected area (dropdown)
- Severity level (dropdown)

**Optional Information:**
- Affected activity name
- Error messages
- Browser information
- Additional context

**Labels:** `bug`

**Key Features:**
- Severity classification (Critical, High, Medium, Low)
- Structured reproduction steps
- Investigation tips for developers
- Browser and environment details

### 4. Feature Request (`feature-request.yml`)

**Purpose:** Suggest new features or enhancements

**Required Information:**
- Feature description
- Problem it solves
- Feature area (dropdown)
- User role that benefits
- Proposed solution
- Priority level

**Optional Information:**
- Alternative solutions
- Success criteria
- Additional context

**Labels:** `enhancement`

**Key Features:**
- Priority levels (Critical, High, Medium, Low)
- User role identification (Teachers, Students, Administrators)
- Comprehensive implementation guidance
- Backward compatibility considerations

### 5. UI/UX Improvement (`ui-ux-improvement.yml`)

**Purpose:** Suggest interface and usability improvements

**Required Information:**
- Improvement type (dropdown)
- Current experience
- Proposed improvement
- Affected page/component
- User impact
- Device type
- Why it's important

**Optional Information:**
- Specific design suggestions
- Accessibility notes
- Examples or references

**Labels:** `enhancement`, `ui/ux`

**Key Features:**
- Focus on user experience impact
- Accessibility considerations
- Device-specific concerns
- CSS and design specifics
- WCAG 2.1 guidelines reference

## Configuration (`config.yml`)

**Purpose:** Organize issue templates and provide helpful links

**Features:**
- Allows blank issues to be created
- Links to Development Guide
- Contact links for additional resources

## Template Design Principles

All templates follow these principles:

### 1. Clear Problem Description
- Structured input fields (text, textarea, dropdown, checkboxes)
- Required vs. optional fields clearly marked
- Helpful placeholders with examples
- Descriptive labels and help text

### 2. Clear Acceptance Criteria
- Every template includes an "Acceptance Criteria" section
- Defines what "done" looks like
- Specifies expected outcomes
- Mentions testing considerations

### 3. Implementation Guidance
- "Implementation Notes" section for developers
- Specific file references (e.g., `src/backend/database.py`)
- Technical requirements and constraints
- Code structure guidance
- Edge cases to consider

### 4. Context and Limitations
- Examples throughout the form
- Time format guides (24-hour format)
- Dropdown options for common choices
- Links to related documentation
- Severity/priority classifications

## Usage Flow

1. Teacher clicks "New Issue" on GitHub
2. Selects appropriate template from the list
3. Fills in the structured form
4. GitHub creates issue with:
   - Appropriate labels
   - Pre-filled title prefix
   - All collected information formatted consistently
5. Issue can be assigned to Copilot coding agent
6. Agent has all necessary context to complete the work

## Benefits

- **For Teachers:** No need to know technical details or write code
- **For Developers:** Consistent, complete information in every issue
- **For Copilot:** Structured data with clear acceptance criteria and implementation hints
- **For Everyone:** Less back-and-forth clarification needed

## File Locations

```
.github/
└── ISSUE_TEMPLATE/
    ├── config.yml                    # Configuration
    ├── add-activity.yml              # Add new activity template
    ├── update-activity.yml           # Update activity template
    ├── bug-report.yml                # Bug report template
    ├── feature-request.yml           # Feature request template
    └── ui-ux-improvement.yml         # UI/UX improvement template
```

## Documentation

- **For Teachers:** [How to Request Changes](./how-to-request-changes.md)
- **For Developers:** [Development Guide](./how-to-develop.md)

## YAML Validation

All templates have been validated as correct YAML syntax and follow GitHub's issue form schema.
