# Frequency stays a sliding window, not a fixed schedule

We wanted the Calendar to show which days a habit is actually expected. We kept Frequency as "N times in D days" over a sliding window: once Yes answers satisfy the Frequency, the days after them become Rest days, and every other day is a Due day. For "every 2 days" this settles into an every-other-day rhythm as long as the person keeps up, and it shifts when they miss a day. The Calendar makes this visible by showing Rest days and future Due days, including the week after today.

## Considered Options

- **Fixed schedule with a start date** ("every 2 days" always means Mon, Wed, Fri, …, whenever the habit was actually done). Rejected because it needs new stored data, changes how score and streaks are computed, breaks [ADR-0001](./0001-stay-mergeable-with-upstream.md), and would need a weekday picker before "3 times per week" could behave the same way. It would also change what existing habits mean for current users.
