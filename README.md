NHS Hospital Episode Statistics (HES) — Power BI Dashboard
An interactive, four-page Power BI report analysing NHS hospital activity across England from 2018–2026, covering appointment volumes, Did Not Attend (DNA) performance, emergency activity, referral patterns, and demographic and specialty-level breakdowns.

Purpose: A self-directed analytics project built to demonstrate end-to-end BI skills — data modelling, DAX, and dashboard design — using publicly available NHS data.


Business Problem
NHS hospital services generate enormous volumes of activity data, but raw figures alone don't tell decision-makers where problems concentrate. Two questions matter operationally:

Where is capacity being lost? Missed appointments (DNAs) waste clinical time and lengthen waiting lists.
Who and where is most affected? Understanding DNA and activity patterns by region, trust, age group, and specialty allows targeted intervention rather than blanket policy.

This dashboard turns national HES data into a navigable story — from the national picture down to individual specialties — so a non-technical stakeholder can spot the high-risk areas in seconds.

Data Source

Dataset: NHS Hospital Episode Statistics (HES) — publicly available NHS activity data.
Coverage: Financial years 2018–19 through 2025–26.
Granularity: National, regional (commissioning region), trust/organisation, patient age band, and treatment specialty.


Scope note (important): Each page draws from its own pre-aggregated source table, and these tables count at different grains (for example, national appointment activity vs. attendances by age band vs. specialty-coded activity). As a result, headline totals legitimately differ between pages — they are measuring different things, not the same metric inconsistently. Each page is labelled with its specific scope. See Notes on Totals below.


Tools & Skills Demonstrated
AreaDetailToolMicrosoft Power BI DesktopData modellingMultiple fact tables, relationships, star-style designDAXCalculated measures for DNA Rate %, Trust Share %, First Attendance %, Follow-Up %, Emergency Share %Visual designKPI cards, trend lines, stacked bars, scatter (activity vs. risk), conditional-formatted tablesInteractivitySlicers (Financial Year, Region, Organisation), cross-filteringAnalytical framingNational → Trust → Demographic → Specialty drill-down narrative

Dashboard Structure
1. National Overview (2018–2026)
National activity, DNA performance, and regional comparison. Headline KPIs (total appointments, elective vs. non-elective activity, DNA rate), trend lines over time, and a region-by-region performance table with conditional formatting on DNA rate.
2. Trust Overview
Trust-level activity, DNA performance, and referral comparison. Ranks organisations by appointment volume, compares GP vs. other referral routes, and plots DNA risk against activity volume by trust.
3. Age Group Demographics
Age-based appointment demand, DNA rate, and emergency activity. Breaks attendance and DNA behaviour down by patient age band, with an emergency-activity profile and a month-ending hospital activity trend.
4. Specialty Performance
Specialty-level appointment volume, DNA rate, emergency activity, and follow-up analysis. Identifies the highest-volume specialties, the highest-DNA-risk specialties, and the relationship between activity and DNA risk.

Key Insights

The COVID-19 shock is clearly visible. Activity collapses to a sharp trough in 2020–21 before recovering, with elective activity rebounding to record levels by 2024–26.
DNA rates vary almost two-fold by region. London commissioning region shows the highest DNA rate (~9.1%) against the South East's ~5.6% — a meaningful operational gap and a candidate for targeted intervention.
The national DNA trend is improving. After peaking at ~7.7% in 2022–23, the DNA rate has fallen steadily toward ~6.6% in 2025–26.
Younger working-age patients miss appointments the most. DNA rate climbs with younger age bands (highest among 17–18 year-olds at ~11–13%) and is lowest among older patients — a clear behavioural pattern for reminder/engagement strategy.
Some specialties carry disproportionate DNA risk. Infectious Diseases (~13.5%) and Adult Mental Illness (~12.3%) show the highest DNA rates among higher-volume specialties — clinically significant, as missed care in these areas carries higher downstream cost.


Notes on Totals
The headline appointment total differs between pages because each page is built from a separate source table aggregated at a different grain:

National Overview — national appointment activity.
Age Group Demographics — attendances aggregated by patient age band.
Specialty Performance — specialty-coded appointment activity.

A single underlying event can appear under multiple categories (e.g. across age bands or specialties), so totals are not expected to be identical across pages. Each page should be read against its own labelled scope, not compared like-for-like.
