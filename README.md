# Response to Resistence

This data package collects multiple years of the Response to Resistance dataset
from the Austin, TX Police department. It includes each of the four source
files and a fifth file that combines the four source files.

## Processing & Caveats

The source files, one year of data per file, have slightly different columns,
so in the combined file there are some columns which will not have data across
all years. These columns are:

* census_tract
* county
* location_1
* zip
* county_description

The combined file also has a set of dummy variables for each of the values of
the `subject_resistance` variable. The categories for `subject_resistance`
change from year to year, and some codes from earlier years are "expired" in
later years. The expiration tags have been removed, so the dummy variables mix
expired and unexpired codes. This is because there are many
`subject_resistance` values that only have expired codes in them. The original
values etained in `subject_resistance`

It appears that the earlier two years used a wide range of detailed codes, such
as "firearm" or "edged weapon" which the later years have collapsed into
"agressive_resistance", "defensive resistance" and "passive resistance", with
out a definite cutoffdate for the transition. The image below shows True values for the dummy variables in yellow. 

<img src="http://library.metatab.org/austintexas.gov-response_to_resistance-1.1.2/docs/sr_dummy_coverage.png" width='800'>

## Police Data Collection

This package is part of the [San Diego Data Library's Police Data Collection](https://github.com/metatab-packages/policedata-collection)

