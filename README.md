# Hysen Labs weekly GitHub star-growth data

This repository contains the data behind Hysen Labs' weekly GitHub star-growth ranking.

The full ranking and methodology are published at:

https://hysenlabs.com/en/weekly

The latest complete week:

https://hysenlabs.com/en/weekly/2026-09-21

## Files

- `data/weekly_top10.csv`: the 10 projects in each complete week, with week and rank.
- - `data/weekly_overlap.csv`: how many projects stayed on the list from the previous week.
  - - `data/summary.json`: aggregate counts and the current overlap series.
   
    - The current snapshot covers nine complete weeks, from 2026-07-27 through 2026-09-21.
   
    - ## What the current data shows
   
    - - 90 ranking slots were filled by 47 distinct projects.
      - - 30 projects, or 64%, appeared exactly once.
        - - The mean overlap between consecutive weeks was 4.9 out of 10.
          - - The overlap ranged from 2 to 6.
            - - Three projects had the longest run at seven weeks: `mattpocock/skills`, `stablyai/orca`, and `DietrichGebert/ponytail`.
              - - All three dropped out in the week of 2026-09-14. `stablyai/orca` returned on 2026-09-21.
               
                - ## Method
               
                - Each week compares two daily snapshots: the one nearest the Monday boundary and the one nearest the Sunday boundary. Both snapshots must fall within 36 hours of the boundary. If either one is missing, the project is dropped for that week rather than estimated.
               
                - Archived, mirrored, and unlisted repositories are excluded. A week only enters the archive when it has ten projects. The first week in the source data had seven, so it is excluded.
               
                - The source corpus contains roughly 19,000 projects and leans toward AI and developer tooling. It is not a random sample of GitHub. Star counts are also noisy, and the ranking measures attention rather than maintenance, code quality, or long-term adoption.
               
                - ## Source and updates
               
                - The files are generated from publicly readable weekly pages. The numbers can be regenerated from the published pages using the logic described in the main site's `scripts/weekly-stats.mjs`.
               
                - If you use this data, cite:
               
                - Hysen Labs. "Weekly GitHub star-growth ranking." https://hysenlabs.com/en/weekly
               
                - ## License
               
                - The data files in this repository are available under the Creative Commons Attribution 4.0 International license (CC BY 4.0):
               
                - https://creativecommons.org/licenses/by/4.0/
                - 
