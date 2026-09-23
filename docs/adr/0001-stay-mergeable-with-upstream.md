# Stay mergeable with upstream

This fork keeps merging iSoron/uhabits, which is still actively developed, so we get its fixes and features for free. To keep those merges cheap, our changes live in the presentation layer (themes, layouts, views, and the view-state code in `uhabits-core/.../ui`), and we avoid changing the database schema or the core models (`Entry`, `Frequency`, `EntryList`, score and streak logic). A change that needs to break this rule should get its own ADR first.
