# Release Note

A new version (1.1.0) of the VPD case surveillance tracker has been released with new indicators, configuration fixes and improvements. These are summarized below.

## New Content

* New **program indicators** for visualizing measles cases by age band and vaccination status. These program indicators are used in the complementary Immunity Gaps dashboard (released as a separate package), designed to triangulate immunization and surveillance data.
* New **indicators** for measles/rubella laboratory specimen adequacy and sensitivity indicators
  * CBS - Measles/rubella discard rate (/100000) `Neerc3YIske`
  * CBS - Proportion of Measles/Rubella specimen adequacy received by National laboratory (%) `MKzrxSTNuGe`
  * CBS - Proportion of Measles/Rubella specimen adequacy (%) `rg1o94xciwp`

## Fixes & Improvements

* Object **names** and **codes** have been updated to fix spelling errors and align with for consistency with DHIS2-recommended metadata coding practices.

* The following fixes were made to **program indicator** expressions:
  * Updated and fixed age-based PIs to accurately calculate age-based PIs whether date of birth was entered manually or estimated based on age given during the case enrollment. The added condition in PI expressions checks for estimated 'Age (Months)' or estimated 'Age (Years)' or age based on 'date of birth' attribute value
  * Fixed PI expressions based on TEI enrollment to count based on *enrollment* vs. *event*
  * Fixed PI expressions where integer 1 was used in place of the proper code 'YES' from core HIS Yes/No option set. PIs affected: `x0n3BxFa6SC`, `1X9hhSxGrU`, `fy6f9KZgAJV`.
* Fixed several **dashboard visualizations** (analytics objects) using 'fixed' periods to export with 'relative' periods
