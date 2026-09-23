# Loop Habit Tracker

A fork of Loop Habit Tracker (iSoron/uhabits): a simple app where people answer one question per habit per day and watch their consistency over time.

## Language

### Habits

**Habit**:
Something the person wants to do regularly, tracked one day at a time.

**Question**:
The per-habit prompt the person answers each day, e.g. "Did you exercise today?".

**Yes/No habit**:
A habit whose daily answer is Yes, No or Skip.
_Avoid_: Boolean habit

**Measurable habit**:
A habit whose daily answer is a number compared against a target.
_Avoid_: Numerical habit

**Frequency**:
How often a habit is expected, expressed as "N times in D days" over a sliding window; there is no fixed schedule or start date.
_Avoid_: Schedule, recurrence, repeat interval

**Rest day**:
A day on which the habit is not expected because earlier Yes answers already satisfy its Frequency. Counts toward streaks.
_Avoid_: Auto-yes, free day, off day, unplanned day

**Due day**:
Any day that is not a Rest day: the habit is expected, or still open to be done, that day.
_Avoid_: Target day, planned day, scheduled day

### Answers

**Entry**:
The answer recorded for one habit on one day.
_Avoid_: Checkmark, repetition, check-in

**Yes**:
An Entry stating the person did the habit that day.

**No**:
An Entry stating the person did not do the habit that day.
_Avoid_: Lapse, miss

**Skip**:
An Entry stating the habit did not apply that day; it neither helps nor hurts.

**Unanswered**:
A day with no Entry: the Question was never answered. Distinct from No everywhere it is shown, but counts as No for the score.
_Avoid_: Unknown, missing data, unset, empty

### Views

**Calendar**:
The day-by-day grid on a habit's page, from the habit's first Entry through the week after today, showing each day's answer and which days are Rest days.
_Avoid_: History (that is the separate bar chart of totals per period)
