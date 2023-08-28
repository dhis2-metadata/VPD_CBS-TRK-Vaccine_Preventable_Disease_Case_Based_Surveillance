# Release Note { #vpd-cs-release-note }

## 1.1.1

Version 1.1.1 of the VPD case surveillance tracker is a compatibility release for DHIS2 versions 2.38 and 2.39, which also includes minor fixes described below.

### Known issues

Due to a [bug](https://dhis2.atlassian.net/browse/DHIS2-14159) in 2.39.2.1 and 2.38.4.3 certain visualizations are not functioning as expected. A fix for this bug is currently (August 2023) in testing, and is scheduled to be included in the next DHIS2 software patch release. 


### Fixes and improvements

**Program indicators** for cases/deaths by _age_ have received two modifications:

* the program indicator description has been updated to specify that the various PIs that calculate cases and deaths by age bands include cases where the date of birth is estimated and the case/death can be reasonably attributed to the correct age band;
* the program indicator filter for the "age unknown" PIs has been updated to check for whether the date of birth attribute has been entered, instead of whether the 'date of birth is unknown' checkbox is ticked;

New program indicator added:

* VPD CS - No lumbar puncture_enrBounds `psGiPlDUjYJ`

**Tracked entity attributes**

New tracked entity attribute included

* GEN - National ID `Ewi7FUfcHAD`

**Visualizations**

Some visualizations on the Yellow fever dashboard have been updated.

New: 
* CBSURV-YF-1 Suspected and confirmed cases `u607ipMtUJe`
* CBSURV-YF-2 Cases by age `d7xQJgR8bs0`
* CBSURV-YF-6 Deaths by vacci status `Kt3JoTMaPEH`
* CBSURV-YF-5 Cases by vacci status `KIyP6R1oCBF`
* CBSURV-YF-3 Deaths by age `FrssprmRhns`

Deleted: 
* VPD-CS-062 `BkKrL1tnoUp`
* VPD-CS-063 `dtC9HaSt15H`
* VPD-CS-064 `sOVKabM1vnH`


## 1.1.0

A new version (1.1.0) of the VPD case surveillance tracker has been released with new indicators, configuration fixes and improvements. These are summarized below.

### New Content

* New **program indicators** for visualizing measles cases by age band and vaccination status. These program indicators are used in the complementary Immunity Gaps dashboard (released as a separate package), designed to triangulate immunization and surveillance data.
* New **indicators** for measles/rubella laboratory specimen adequacy and sensitivity indicators
  * CBS - Measles/rubella discard rate (/100000) `Neerc3YIske`
  * CBS - Proportion of Measles/Rubella specimen adequacy received by National laboratory (%) `MKzrxSTNuGe`
  * CBS - Proportion of Measles/Rubella specimen adequacy (%) `rg1o94xciwp`

### Fixes & Improvements

* Object **names** and **codes** have been updated to fix spelling errors and align with for consistency with DHIS2-recommended metadata coding practices.

* The following fixes were made to **program indicator** expressions:
  * Updated and fixed age-based PIs to accurately calculate age-based PIs whether date of birth was entered manually or estimated based on age given during the case enrollment. The added condition in PI expressions checks for estimated 'Age (Months)' or estimated 'Age (Years)' or age based on 'date of birth' attribute value
  * Fixed PI expressions based on TEI enrollment to count based on *enrollment* vs. *event*
  * Fixed PI expressions where integer 1 was used in place of the proper code 'YES' from core HIS Yes/No option set. PIs affected: `x0n3BxFa6SC`, `1X9hhSxGrU`, `fy6f9KZgAJV`.
* Fixed several **dashboard visualizations** (analytics objects) using 'fixed' periods to export with 'relative' periods
