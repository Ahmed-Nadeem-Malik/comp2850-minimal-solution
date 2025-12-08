# COMP2850 HCI Assessment: Evaluation & Redesign Portfolio

**Student**: Name : Ahmed Nadeem Malik, Student Id: 201842177

**Submission date**: [DD/MM/YYYY] TODO WHEN SUBMITTED

**Academic Year**: 2025-26

---

## Privacy & Ethics Statement

- [x] I confirm all participant data is anonymous (session IDs use P1_xxxx format, not real names)
- [x] I confirm all screenshots are cropped/blurred to remove PII (no names, emails, student IDs visible)
- [x] I confirm all participants gave informed consent
- [x] I confirm this work is my own (AI tools used for code assistance are cited below)

**AI tools used**: [ChatGPT Codex used where specified below]

---

## 1. Protocol & Tasks

### Link to Needs-Finding (LO2)

## Story S1: Keeping tasks accurate

**Situation**: When I realise a task name is wrong or needs to be changed

**Motivation**: I want to edit the name of that task

**Outcome**: So that my task list is accurate and easy to understand

**Underlying need**: Because incorrect names make tasks harder to remember and manage what I need to do

**How Task 2 tests this**: Tests whether we can actually change tasks after adding

---

## Story S2: Accurate Task Counter

**Situation**: When I submit a form (add/edit/delete task)

**Motivation**: I want the task counter to update immediately without a refresh

**Outcome**: So I can trust how many tasks I actually have saved

**Underlying need**: Because uncertainty about success makes me recheck and slows me down

---

## Story S3: Keeping up to date with new tasks

**Situation**: When i want to make a new task

**Motivation**: I want it to be saved and be shown on the web page

**Outcome**: So I can know that the task I have added has been added successfully

**Underlying need**: Because uncertainty makes me recheck and feel anxious that my task may have not been added correctly

**How Task 3 tests this**: Tests whether we can actually create new tasks

---

## Story S4: No progress indication

**Situation**: When i am doing a task in the list

**Motivation**: I want to see what tasks I have completed and what other tasks i need to do

**Outcome**: So I can understand my progress when I look at it

**Underlying need**: Because without a clear sense of progress I feel disorganised and unmotivated

---

## Story S5: Finding a task faster

**Situation**: When I am doing a task in the list

**Motivation**: I want to see what tasks I have completed and what other tasks i need to do

**Outcome**: So I can understand my progress when I look at it

**Underlying need**: Because without a clear sense of progress I feel disorganised and unmotivated

**How Task 3 tests this**: Tests whether we can navigate to the task we want

---

## Story S6: Making sure old tasks are removed

**Situation**: When I finish a task in the list
    
**Motivation**: I want to remove it 

**Outcome**: So that the task list is not cluttered

**Underlying need**: Because old tasks makes it hard to tell what tasks needs to be completed

**How Task 4 tests this**: Tests whether we can remove tasks we finished off the list

---

### Evaluation Tasks 

#### Task 1 : Add Task

- **Scenario**: Add a new task to the task list

- **Action**: Navigate to "Add New Task", then under "Task Title" write the task name in the text box of the task you
  want, then click "Add Task" button

- **Success**: In the "Your Tasks" section the name of the task you added should appear as a bullet point

- **Target time**: Approximately 10 seconds

- **Linked to**: Job Story #3

#### Task 2 : Edit task

- **Scenario**: Edit task name

- **Action**: Navigate to "Your Tasks", click "Edit" on the task you want to edit, then you can press "Cancel" if you
  don't want to edit, or you can write into the text box to edit the task name, then press "Save" button in order to
  confirm changes

- **Success**: In the "Your Tasks" section the name of the task you changed has changed to the new task name

- **Target time**: Approximately 10 seconds

- **Linked to**: Job Story #1

#### Task 3 : Filter tasks

- **Scenario**: Find a task quickly

- **Action**: Navigate to "Filter Tasks", then in the text box under "Filter by title" type the text you want to filter
  by in the box, then press the "Apply Filter" button

- **Success**: In the "Your Tasks" section the tasks listed should only contain task tilts that contain your filter text

- **Target time**: Approximately 15 seconds

- **Linked to**: Job Story #5

#### Task 4 : Delete task

- **Scenario**: Delete task in task name

- **Action**: Navigate to "Your Tasks", then in the specific task you want to delete, click the "Delete" button, then a
  browser pop up will ask you for a confirmation message that you can press "Cancel" if you change your mind or "OK" if
  you want to confirm deletion

- **Success**: In the "Your Tasks" section the tasks listed should not contain the task deleted

- **Target time**: Approximately 6 seconds

- **Linked to**: Job Story #6

---

### Consent Script (They Read Verbatim)

**Introduction**:
"Thank you for participating in my HCI evaluation. This will take about 15 minutes. I'm testing my task management
interface, not you. There are no right or wrong answers."

**Rights**:

- [ ] "Your participation is voluntary. You can stop at any time without giving a reason."
- [ ] "Your data will be anonymous. I'll use a code (like P1) instead of your name."
- [ ] "I may take screenshots and notes. I'll remove any identifying information."
- [ ] "Do you consent to participate?" [Wait for verbal yes]

**Recorded consent timestamp**: [e.g., "P1 consented 22/11/2025 14:05"]

---

## 2. Findings Table

**Instructions**: Fill in this table with 3-5 findings from your pilots. Link each finding to data sources.

| Finding                                      | Data Source                          | Observation (Quote/Timestamp)                                                                                     | WCAG      | Impact (1-5) | Inclusion (1-5) | Effort (1-5) | Priority |
|----------------------------------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------|--------------|-----------------|--------------|----------|
| Edit button does not work without JavaScript | metrics.csv L13-17 + P2 notes Task 2 | P2: "This is not good"                                                                                            | 4.1.2 A   | 5            | 5               | 3            | 7        |
| Browser pop up to small when deleting        | P1 notes Task 4                      | P1: "My eyesight is not the best so would like the pop-up when confirming to delete to be bigger"                 | 1.4.4 AA  | 2            | 3               | 3            | 2        |
| Small cancel button when using edit          | P1 notes Worst issues                | P1: the cancel button on edit is a bit too small and would be harder press on a smaller size device like a phone" | 2.5.5 AAA | 3            | 3               | 1            | 5        |

**Priority formula**: (Impact + Inclusion) - Effort

**Top 3 priorities for redesign**:

1. Finding #1 - 7
2. Finding #2 - 2
3. Finding #3 - 5

---

## 3. Pilot Metrics (metrics.csv)

**Instructions**: Paste your raw CSV data here OR attach metrics.csv file

```csv
ts_iso,session_id,request_id,task_code,step,outcome,ms,http_status,js_mode

2025-11-28T13:27:18.202431Z,P1_67ui,r_2f599ad7,T1_add,success,ok,7,200,on
2025-11-28T13:30:20.688338Z,P1_67ui,r_0813d115,T0_list,success,ok,8,200,on
2025-11-28T13:31:51.140907Z,P1_67ui,r_bfabc67b,T3_filter,success,ok,8,200,on
2025-11-28T13:31:51.818848Z,P1_67ui,r_49a0ef3d,T3_filter,success,ok,5,200,on
2025-11-28T13:31:53.402735Z,P1_67ui,r_af2550a4,T3_filter,success,ok,5,200,on
2025-11-28T13:31:55.325946Z,P1_67ui,r_2d7ba4ab,T3_filter,success,ok,2,200,on
2025-11-28T13:33:19.865791Z,P1_67ui,r_dbe794d5,T4_delete,success,ok,3,200,on

2025-11-28T13:39:44.935198Z,P2_df5r,r_f04cdab2,T1_add,success,ok,7,200,off
2025-11-28T13:39:45.253042Z,P2_df5r,r_a878a231,T0_list,success,ok,6,200,off
2025-11-28T13:41:22.325213Z,P2_df5r,r_03de5ac5,T0_list,success,ok,6,200,off
2025-11-28T13:41:23.714382Z,P2_df5r,r_8a68a7de,T0_list,success,ok,4,200,off
2025-11-28T13:41:24.391379Z,P2_df5r,r_52d8a814,T0_list,success,ok,5,200,off
2025-11-28T13:41:27.678735Z,P2_df5r,r_bc1b9830,T0_list,success,ok,4,200,off
2025-11-28T13:41:38.947952Z,P2_df5r,r_24c6aa4f,T0_list,success,ok,7,200,off
2025-11-28T13:43:20.130818Z,P2_df5r,r_ef7bf873,T0_list,success,ok,4,200,off
2025-11-28T13:46:35.273314Z,P2_df5r,r_25ade855,T4_delete,success,ok,2,200,off
2025-11-28T13:46:35.282351Z,P2_df5r,r_ac4fea76,T0_list,success,ok,2,200,off

2025-11-28T13:55:06.410032Z,P3_77fd,r_8753ef8c,T1_add,success,ok,7,200,on
2025-11-28T13:56:58.264596Z,P3_77fd,r_8de786f1,T3_filter,success,ok,4,200,on
2025-11-28T13:56:59.333626Z,P3_77fd,r_a25f46f0,T3_filter,success,ok,4,200,on
2025-11-28T13:57:00.582544Z,P3_77fd,r_9efe0a7e,T3_filter,success,ok,5,200,on
2025-11-28T13:59:30.417768Z,P3_77fd,r_dcca6c54,T4_delete,success,ok,2,200,on
2025-11-28T13:59:30.793984Z,P3_77fd,r_b8eb0d46,T0_list,success,ok,58,200,on

```

**Participant summary**:

- **P1**: Keyboard-only + HTMX
- **P2**: Standard Mouse + No-JS
- **P3** Standard Mouse + HTMX

**Total participants**: n = 3

---

## 4. Implementation Diffs

**Instructions**: Show before/after code for 1-3 fixes. Link each to findings table.

### Fix 1: Make Cancel button bigger

**Addresses finding**: Finding #3

**Before**

(Path: src/main/resources/static/css/custom.css Line Number: ~206 ):

```kotlin
.task - actions {
    display: flex;
    gap: 0.5rem;
    flex - shrink: 0;
}

    .task - actions button {
    margin: 0;
    padding: 0.5rem 1rem;
    font - size: 0.875rem;
}

    .task - edit button {
    width: 100%;
}

    .task - edit button +button {
    margin - top: 0.5rem;
}
```

(Path: src/main/resources/templates/tasks/_edit.peb Line Number: ~27 ):

```pebble
<a href="/tasks"
    hx-get="/tasks/{{ task.id }}/view"
    hx-target="#task-{{ task.id }}"
    hx-swap="outerHTML"
    role="button">Cancel</a>
```

**After**

(Path: src/main/resources/static/css/custom.css Line Number: ~218 ):

AI: Used ChatGPT codex to help with sizing for padding, font, width and margin

```kotlin
.task - actions {
    display: flex;
    gap: 0.5rem;
    flex - shrink: 0;
}

    .task - actions button {
    margin: 0;
    padding: 0.5rem 1rem;
    font - size: 0.875rem;
}

    .task - edit button {
    width: 100%;
}

    .task - edit button +button {
    margin - top: 0.5rem;
}
```

(Path: src/main/resources/templates/tasks/_edit.peb Line Number: ~27 ):

AI: Used ChatGPT to help me think of changing it from an "a" tag to a button

```pebble
<button type="button"
        hx-get="/tasks/{{ task.id }}/view"
        hx-target="#task-{{ task.id }}"
        hx-swap="outerHTML">
  Cancel
</button>
```

**What changed**: Changed the Cancel "a" HTML tag to a real button then applied styling with the custom.css

**Why**: Fixes WCAG 2.5.5 by making the button bigger which makes it easier to press

**Impact**: Those with visual impairment can much easily see the button, also those who use devices like phones have an
easier time pressing the button on a smaller screen.

---

### Fix 2: No-JS edit implementation

**Addresses finding**: Finding #1

**Before**:

(Path: src/main/resources/templates/tasks/_edit.peb Line Number: ~26 ):

```pebble    
    <button type="button"
            hx-get="/tasks/{{ task.id }}/view"
            hx-target="#task-{{ task.id }}"
            hx-swap="outerHTML">
      Cancel
    </button>
  </form>
</li>
```

(Path: src/main/resources/templates/tasks/_edit_page.peb Line Number: ~0 ):

```pebble
Was not made yet
```

(Path: src/main/kotlin/routes/TaskRoutes.kt Line Number: ~297 ):

```kotlin
    } else {
// No-JS: redirect to list (would need edit mode support in index)
respondRedirect("/tasks")
}
```

(Path: src/main/kotlin/routes/TaskRoutes.kt Line Number: ~330 ):

```kotlin
    } else {
// No-JS: redirect back (would need error handling)
respondRedirect("/tasks")
}
```

**After**:

(Path: src/main/resources/templates/tasks/_edit.peb Line Number: ~26 ):

AI: Used ChatGPT to help me find the proper tag for "noscript"

```pebble    
    <button type="button"
            hx-get="/tasks/{{ task.id }}/view"
            hx-target="#task-{{ task.id }}"
            hx-swap="outerHTML">
      Cancel
    </button>
    <noscript>
      <p><a href="/tasks">Cancel and return to the list</a></p>
    </noscript>
  </form>
</li>
```

(Path: src/main/resources/templates/tasks/_edit_page.peb Line Number: ~1 ):

```pebble
{% extends "_layout/base.peb" %}

    {% block title %}Edit Task | COMP2850{% endblock %}

{% block content %}
<article>
  <header>
    <h1>Edit Task</h1>
    <p>Update the task title and save your changes.</p>
  </header>

  <ul class="task-list">
    {% include "tasks/_edit.peb" %}
  </ul>

  <p>
    <a href="/tasks">Back to task list</a>
  </p>
</article>
{% endblock %}
```

(Path: src/main/kotlin/routes/TaskRoutes.kt Line Number: ~297 ):

```kotlin
    } else {
val html = renderTemplate("tasks/edit_page.peb", mapOf("task" to task.toPebbleContext()))
respondText(html, ContentType.Text.Html)
}
```

(Path: src/main/kotlin/routes/TaskRoutes.kt Line Number: ~330 ):

```kotlin
    } else {
val html = renderTemplate(
"tasks/edit_page.peb", mapOf(
"task" to task.toPebbleContext(), "error" to validation.message
)
)
respondText(html, ContentType.Text.Html)
}
```

**What changed**: Implemented the actual route for the edit path when not using JavaScript

**Why**: Fix for no JavaScript but also links in with WCAG 4.1.2

**Impact**: If your browser doesn't support JS, edit actually works also if you use a screen reader this fix will
actually work and will correctly direct them to edit a task

---

## 5. Metrics Breakdown

| Task | Target Time(seconds) | Mean Time(seconds) | Median Time(seconds) | Range of Times(seconds) | Target-Mean(seconds) |
|------|----------------------|--------------------|----------------------|-------------------------|----------------------|
| #1   | ~9                   | ~6.3               | 7                    | 4 to 8                  | ~2.7                 | 
| #2   | ~14                  | 12                 | 14                   | 4 to 18                 | ~2                   | 
| #3   | ~10                  | ~6.6               | 5                    | 4 to 11                 | ~3.7                 | 
| #4   | ~4                   | ~2                 | 2                    | 1 to 3                  | ~2                   | 

### Reflection / Initial Thoughts

We did overestimate the time it takes for a user to complete tasks so the way we evaluate target time needs to be
evaluated. P3 mean time overall was the fastest to complete all tasks.
Even though P2 used a keyboard they didn't have significant impact on the time it takes for them to do tasks except task
#2 which did take longer than expected.
---

## 6. Verification Results

### Part A: Regression Checklist (20 checks)

**Instructions**: Test all 20 criteria. Mark pass/fail/n/a + add notes.

| Check            | Criterion                             | Level | Result      | Notes                                                                                                                  |
|------------------|---------------------------------------|-------|-------------|------------------------------------------------------------------------------------------------------------------------|
| **Keyboard (5)** |                                       |       |             |                                                                                                                        |
| K1               | 2.1.1 All actions keyboard accessible | A     | pass        | Tested with P1, and all features were available                                                                        |
| K2               | 2.4.7 Focus visible                   | AA    | pass        | Went through all the interactive elements and how a outline both in JS and No-JS                                       |
| K3               | No keyboard traps                     | A     | pass        | When running through the pilot with P1 and solo testing, no keyboard taps                                              |
| K4               | Logical tab order                     | A     | pass        | P1 had no issues with the tab order and when tested seemed intuitive                                                   |
| K5               | Skip links present                    | AA    | pass        | The skip link button shows up straight away when you first tab onto the web page                                       |
| **Forms (3)**    |                                       |       |             |                                                                                                                        |
| F1               | 3.3.2 Labels present                  | A     | pass        | Pebble templates contain labels properly describing features                                                           |
| F2               | 3.3.1 Errors identified               | A     | pass        | We use aria-live like assertive for screen readers to easily identify erros and we also get text at the top for errors |
| F3               | 4.1.2 Name/role/value                 | A     | pass        | All names are quite simple and do what they are supposed to do                                                         |
| **Dynamic (3)**  |                                       |       |             |                                                                                                                        |
| D1               | 4.1.3 Status messages                 | AA    | pass        | Errors are shown up at the top of the page in text and are announced                                                   |
| D2               | Live regions work                     | AA    | fail        | Does not explicitly say with VoiceOver on mac that a task has been successfully added, edited, filtered or delted      |
| D3               | Focus management                      | A     | pass        | When trying to press submit on a empty add task field we are redicted back to the input field                          |
| **No-JS (3)**    |                                       |       |             |                                                                                                                        |
| N1               | Full feature parity                   | —     | fail        | After implementing the edit button fix for no javascript, the save button works but the cancel button does not         |
| N2               | POST-Redirect-GET                     | —     | pass        | We dont have to double submit, implemented for the edit No-JS route asdwell                                            |
| N3               | Errors visible                        | A     | pass        | When trying to add a empty task into the task field, we get a message saying that the field is empty                   |
| **Visual (3)**   |                                       |       |             |                                                                                                                        |
| V1               | 1.4.3 Contrast minimum                | AA    | pass        | I have mild colour blindness and the text was easily identifiable                                                      |
| V2               | 1.4.4 Resize text                     | AA    | pass        | Even when zoomed in 500% it worked well also works well on a phone format when tested                                  |
| V3               | 1.4.11 Non-text contrast              | AA    | [pass/fail] | [e.g., "Focus indicator 4.5:1"]                                                                                        |
| **Semantic (3)** |                                       |       |             |                                                                                                                        |
| S1               | 1.3.1 Headings hierarchy              | A     | [pass/fail] | [e.g., "h1 → h2 → h3, no skips"]                                                                                       |
| S2               | 2.4.1 Bypass blocks                   | A     | [pass/fail] | [e.g., "<main> landmark, <nav> for filter"]                                                                            |
| S3               | 1.1.1 Alt text                        | A     | [pass/fail] | [e.g., "No images in interface OR all have alt"]                                                                       |

**Summary**: [X/20 pass], [Y/20 fail]
**Critical failures** (if any): [List any Level A fails]

---

### Part B: Before/After Comparison

**Instructions**: Compare Week 9 baseline (pre-fix) to Week 10 (post-fix). Show improvement.

| Metric                | Before (Week 9, n=X) | After (Week 10, n=Y) | Change         | Target Met? |
|-----------------------|----------------------|----------------------|----------------|-------------|
| SR error detection    | [e.g., 0/2 (0%)]     | [e.g., 2/2 (100%)]   | [e.g., +100%]  | [✅/❌]       |
| Validation error rate | [e.g., 33%]          | [e.g., 0%]           | [e.g., -33%]   | [✅/❌]       |
| Median time [Task X]  | [e.g., 1400ms]       | [e.g., 1150ms]       | [e.g., -250ms] | [✅/❌]       |
| WCAG [criterion] pass | [fail]               | [pass]               | [— ]           | [✅/❌]       |

**Re-pilot details**:

- **P5** (post-fix): [Variant - e.g., "Screen reader user, NVDA + keyboard"] - [Date piloted]
- **P6** (if applicable): [Variant] - [Date]

**Limitations / Honest reporting**:
[If metrics didn't improve or only modestly: explain why. Small sample size? Wrong fix? Needs more iteration? Be honest - valued over perfect results.]

---

## 7. Evidence Folder Contents

**Instructions**: List all files in your evidence/ folder. Provide context.

### Screenshots

| Filename                  | What it shows                         | Context/Link to finding              |
|---------------------------|---------------------------------------|--------------------------------------|
| before-sr-error.png       | Error message without role="alert"    | Finding #1 - SR errors not announced |
| after-sr-error.png        | Error message WITH role="alert" added | Fix #1 verification                  |
| regression-axe-report.png | axe DevTools showing 0 violations     | Verification Part A                  |
| [your-screenshot-3.png]   | [Description]                         | [Which finding/fix this supports]    |

**PII check**:

- [ ] All screenshots cropped to show only relevant UI
- [ ] Browser bookmarks/tabs not visible
- [ ] Participant names/emails blurred or not visible

---

### Pilot Notes

**Instructions**: Attach pilot notes as separate files (P1-notes.md, P2-notes.md, etc.). Summarize key observations
here.

**P1** ([ Variant - e.g., "Standard mouse + HTMX"]):

- **Key observation 1**: [Quote + timestamp - e.g., "Struggled with filter button (09:47)"]
- **Key observation 2**: [Quote + timestamp]

**P2** ([Variant]):

- **Key observation 1**: [Quote + timestamp]
- **Key observation 2**: [Quote + timestamp]

[Repeat for P3, P4 if applicable]
11 47 35
11 50 05 5
11 51 05 4
11 51 40 5
11 52 15 5
**most condusioisung** task names were small
**edit** apply filter was nice an convientinet
**accessiblity** No-JS
---

## Evidence Chain Example (Full Trace)

**Instructions**: Pick ONE finding and show complete evidence trail from data → fix → verification.

**Finding selected**: Edit button in No-JS mode does not work

**Evidence trail**:

1. **Data**: metrics.csv lines 13-17 shows the user attempting to edit multiple times, however it just redirects to
   the "/tasks" endpoint
2. **Observation**: P2 pilot notes Task #2 - quotes "This is not good" as they repeatedly clicked the edit button
3. **Screenshot**: before-sr-error.png shows error message has no role="alert" or aria-live
4. **WCAG**: 3.3.1 Error Identification (Level A) violation - errors not programmatically announced
5. **Prioritisation**: findings-table.csv row 1 - Priority score 7 (Impact 5 + Inclusion 5 - Effort 3)
6. **Fix**: Implemented fix in diffs above in Fix #2 to make a new page
7. **Verification**: Self testing when going to click edit with No-JS, routes to a new page that allows editing
8. **Before/after**: Before would just reroute to "/task", After would route to a new page then allows the user to edit
9. **Re-pilot**: P5 (SR user) pilot notes - "Heard error announcement immediately, corrected and succeeded"

**Complete chain**: Data → Observation → Interpretation → Fix → Verification ✅

---

## Submission Checklist

Before submitting, verify:

**Files**:

- [ ] This completed template (submission-template.md)
- [ ] metrics.csv (or pasted into Section 3)
- [ ] Pilot notes (P1-notes.md, P2-notes.md, etc. OR summarised in Section 6)
- [ ] Screenshots folder (all images referenced above)
- [ ] Privacy statement signed (top of document)

**Evidence chains**:

- [ ] findings-table.csv links to metrics.csv lines AND/OR pilot notes timestamps
- [ ] implementation-diffs.md references findings from table
- [ ] verification.csv Part B shows before/after for fixes

**Quality**:

- [ ] No PII in screenshots (checked twice!)
- [ ] Session IDs anonymous (P1_xxxx format, not real names)
- [ ] Honest reporting (limitations acknowledged if metrics didn't improve)
- [ ] WCAG criteria cited specifically (e.g., "3.3.1" not just "accessibility")

**Pass criteria met**:

- [ ] n=2+ participants (metrics.csv has 2+ session IDs)
- [ ] 3+ findings with evidence (findings-table.csv complete)
- [ ] 1-3 fixes implemented (implementation-diffs.md shows code)
- [ ] Regression complete (verification.csv has 20 checks)
- [ ] Before/after shown (verification.csv Part B has data)

---

**Ready to submit?** Upload this file + evidence folder to Gradescope by end of Week 10.

**Estimated completion time**: 12-15 hours across Weeks 9-10

**Good luck!** 🎯
