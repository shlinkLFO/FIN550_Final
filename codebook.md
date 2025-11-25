# Property Data Codebook

This codebook describes the variables in the Cook County property assessment dataset. Variables are organized by type and include property characteristics, economic factors, geographic information, metadata, and temporal features.

## Table of Contents

- [Property Characteristics (char)](#property-characteristics-char)
- [Economic Variables (econ)](#economic-variables-econ)
- [Geographic Variables (geo)](#geographic-variables-geo)
- [Indicator Variables (ind)](#indicator-variables-ind)
- [Metadata (meta)](#metadata-meta)
- [Time Variables (time)](#time-variables-time)

---

## Property Characteristics (char)

Physical and structural characteristics of residential properties.

### Age
- **Variable Name:** `char_age`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Age of the property

### Central Air Conditioning
- **Variable Name:** `char_air`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Central A/C (YES)
  - `2` - No Central A/C (NO)

### Apartments
- **Variable Name:** `char_apts`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Two (TWO)
  - `2` - Three (THREE)
  - `3` - Four (FOUR)
  - `4` - Five (FIVE)
  - `5` - Six (SIX)
  - `6` - None (NONE)

### Attic Finish
- **Variable Name:** `char_attic_fnsh`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Living Area (LAR)
  - `2` - Partial (PT)
  - `3` - None (UNF)

### Attic Type
- **Variable Name:** `char_attic_type`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Full (FL)
  - `2` - Partial (PT)
  - `3` - None (NO)

### Bedrooms
- **Variable Name:** `char_beds`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Number of bedrooms in the property, defined based on building square footage and the judgement of the person in the field.

### Building Square Feet
- **Variable Name:** `char_bldg_sf`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** As measured from the exterior of the building.

### Basement
- **Variable Name:** `char_bsmt`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Full (FL)
  - `2` - Slab (SL)
  - `3` - Partial (PT)
  - `4` - Crawl (CR)

### Basement Finish
- **Variable Name:** `char_bsmt_fin`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Formal Rec Room (REC)
  - `2` - Apartment (APT)
  - `3` - Unfinished (UNF)

### Construction Quality
- **Variable Name:** `char_cnst_qlty`
- **Data Type:** Categorical
- **Predictor:** No
- **Note:** In general, this field is not used consistently and is therefore not useful for analytical purposes
- **Values:**
  - `1` - Deluxe (DLXE)
  - `2` - Average (AVG)
  - `3` - Poor (POOR)

### Wall Material
- **Variable Name:** `char_ext_wall`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Frame (FRAM)
  - `2` - Masonry (MASR)
  - `3` - Frame + Masonry (FRMA)
  - `4` - Stucco (STUC)

### Full Baths
- **Variable Name:** `char_fbath`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Number of full bathrooms, defined as having a bath or shower. If this value is missing, the default value is set to 1.

### Fireplaces
- **Variable Name:** `char_frpl`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Number of fireplaces, counted as the number of flues one can see from the outside of the building.

### Garage 1 Area
- **Variable Name:** `char_gar1_area`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Description:** Is Garage 1 physically including within the building area? If yes, the garage area is subtracted from the building square feet calculation by the field agent.
- **Values:**
  - `1` - Yes (YES)
  - `2` - No (NO)

### Garage 1 Attached
- **Variable Name:** `char_gar1_att`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Yes (YES)
  - `2` - No (NO)

### Garage 1 Material
- **Variable Name:** `char_gar1_cnst`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Frame (FRAM)
  - `2` - Masonry (MASR)
  - `3` - Frame + Masonry (FRMA)
  - `4` - Stucco (STUC)

### Garage 1 Size
- **Variable Name:** `char_gar1_size`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - 1 cars (1CAR)
  - `2` - 1.5 cars (1.5CAR)
  - `3` - 2 cars (2CAR)
  - `4` - 2.5 cars (2.5CAR)
  - `5` - 3 cars (3CAR)
  - `6` - 3.5 cars (3.5CAR)
  - `7` - 0 cars (0CAR)
  - `8` - 4 cars (4CAR)

### Half Baths
- **Variable Name:** `char_hbath`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Number of half baths, defined as bathrooms without a shower or bathtub.

### Land Square Feet
- **Variable Name:** `char_hd_sf`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Square feet of the land (not just the building) of the property. Note that land is divided into 'plots' and 'parcels' - this field applies to parcels, identified by PIN.

### Central Heating
- **Variable Name:** `char_heat`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Warm Air Furnace (FURN)
  - `2` - Hot Water Steam (STM)
  - `3` - Electric Heater (ELEC)
  - `4` - None (NONE)

### Number of Commercial Units
- **Variable Name:** `char_ncu`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Number of commercial units (the vast majority are for properties with class 212).

### Other Heating
- **Variable Name:** `char_oheat`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Floor Furnace (FURN)
  - `2` - Unit Heater (UNIT)
  - `3` - Stove (STVE)
  - `4` - Solar (SOLR)
  - `5` - None (NONE)

### Other Improvements
- **Variable Name:** `char_ot_impr`
- **Data Type:** Numeric
- **Predictor:** No

### Porch
- **Variable Name:** `char_porch`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Frame Enclosed (FRAM)
  - `2` - Masonry Enclosed (MSRY)
  - `3` - None (NONE)

### Renovation
- **Variable Name:** `char_renovation`
- **Data Type:** Categorical
- **Predictor:** No
- **Values:**
  - `1` - Yes (YES)
  - `2` - No (NO)

### Repair Condition
- **Variable Name:** `char_repair_cnd`
- **Data Type:** Categorical
- **Predictor:** No
- **Note:** This field is subjective and contains little variation. As such, it is not used for modeling.
- **Values:**
  - `1` - Above Average (GOOD)
  - `2` - Average (AVG)
  - `3` - Below Average (POOR)

### Roof Material
- **Variable Name:** `char_roof_cnst`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Shingle + Asphalt (SHAS)
  - `2` - Tar + Gravel (TRGR)
  - `3` - Slate (SLTE)
  - `4` - Shake (SHKE)
  - `5` - Tile (TILE)
  - `6` - Other (OTHR)

### Rooms
- **Variable Name:** `char_rooms`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Number of rooms in the property (excluding baths). Not to be confused with bedrooms

### Site Desirability
- **Variable Name:** `char_site`
- **Data Type:** Categorical
- **Predictor:** No
- **Note:** This field lacks sufficient variation to be useful for modeling.
- **Values:**
  - `1` - Beneficial To Value (BTV)
  - `2` - Not Relevant To Value (NRTV)
  - `3` - Detracts From Value (DFV)

### Cathedral Ceiling
- **Variable Name:** `char_tp_dsgn`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Note:** This field name comes from a variable that is no longer used, but the field name was not changed to reflect Cathedral Ceiling
- **Values:**
  - `1` - Yes (YES)
  - `2` - No (NO)

### Design Plan
- **Variable Name:** `char_tp_plan`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Architect (ARCT)
  - `2` - Stock Plan (STCK)

### Type of Residence
- **Variable Name:** `char_type_resd`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Note:** Residences with 1.5 - 1.9 stories are one story and have partial livable attics and are classified based on the square footage of the attic compared to the first floor of the house. So, 1.5 story houses have an attic that is 50% of the area of the first floor, 1.6 story houses are 60%, 1.7 are 70%, etc.
- **Values:**
  - `1` - 1 Story (1STRY)
  - `2` - 2 Story (2STRY)
  - `3` - 3 Story + (3STRY+)
  - `4` - Split Level (SPLT)
  - `5` - 1.5 Story (1.5STRY)
  - `6` - 1.6 Story (1.6STRY)
  - `7` - 1.7 Story (1.7STRY)
  - `8` - 1.8 Story (1.8STRY)
  - `9` - 1.9 Story (1.9STRY)

### Use
- **Variable Name:** `char_use`
- **Data Type:** Categorical
- **Predictor:** Yes
- **Values:**
  - `1` - Single-Family (SF)
  - `2` - Multi-Family (MF)

### Volume
- **Variable Name:** `char_volume`
- **Data Type:** Numeric
- **Predictor:** No
- **Note:** Need to clarify definition.

---

## Economic Variables (econ)

Economic and financial characteristics related to the property and surrounding area.

### Tract Median Income
- **Variable Name:** `econ_midincome`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Median income of the census tract containing the property centroid.

### Tax Amount Paid
- **Variable Name:** `econ_tax_amt_paid`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Tax amount paid by the property owner. Taken from Cook County Treasurer's Office.

### Tax Location Code
- **Variable Name:** `econ_tax_cd`
- **Data Type:** Character
- **Predictor:** No

### Tax Rate
- **Variable Name:** `econ_tax_rate`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Tax rate paid by the property owner. Taken from Cook County Treasurer's Office.

### Number of Foreclosures in Town Per Month
- **Variable Name:** `econ_foreclosures_month_town`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** The number of foreclosures in the property's township during the month the sale occurred in

### Number of Foreclosures in Town Per Quarter
- **Variable Name:** `econ_foreclosures_quarter_town`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** The number of foreclosures in the property's township during the quarter the sale occurred in

---

## Geographic Variables (geo)

Location and geographic characteristics of properties.

### Tract Percent Pop. Black
- **Variable Name:** `geo_black_perc`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Black population percentage of the census tract containing the property centroid.

### Tract Percent Pop. Asian
- **Variable Name:** `geo_asian_perc`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Asian population percentage of the census tract containing the property centroid.

### Tract Percent Pop. Hispanic
- **Variable Name:** `geo_his_perc`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Hispanic population percentage of the census tract containing the property centroid.

### Tract Percent Pop. White
- **Variable Name:** `geo_white_perc`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** White population percentage of the census tract containing the property centroid.

### Tract Percent Pop. Other
- **Variable Name:** `geo_other_perc`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Other population percentage of the census tract containing the property centroid.

### Tract Population
- **Variable Name:** `geo_tract_pop`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Total population of the Census tract containing the property centroid.

### Census Tract
- **Variable Name:** `geo_census_tract`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Last 6 digits of GEOID for matched census tract (tract ID only).

### Tract GEOID
- **Variable Name:** `geo_geoid`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Full 11-digit GEOID for matched census tract.

### Longitude
- **Variable Name:** `geo_longitude`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Longitude coordinate of the property's location, as defined by the centroid of the parcel shape in GIS.

### Latitude
- **Variable Name:** `geo_latitude`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Latitude coordinate of the property's location, as defined by the centroid of the parcel shape in GIS.

### Cook County Commissioner District
- **Variable Name:** `geo_commissioner_dist`
- **Data Type:** Character
- **Predictor:** No

### Municipality FIPS Code
- **Variable Name:** `geo_fips`
- **Data Type:** Character
- **Predictor:** No
- **Description:** FIPS code of the municipality containing the property.

### Municipality Name
- **Variable Name:** `geo_municipality`
- **Data Type:** Character
- **Predictor:** No

### FEMA Floodplain
- **Variable Name:** `geo_floodplain`
- **Data Type:** Logical
- **Predictor:** Yes
- **Description:** Indicator for whether property lies within a FEMA-defined floodplain.

### O'Hare Noise Indicator
- **Variable Name:** `geo_ohare_noise`
- **Data Type:** Logical
- **Predictor:** Yes

### Road Proximity < 100 Feet
- **Variable Name:** `geo_withinmr100`
- **Data Type:** Logical
- **Predictor:** Yes
- **Description:** Indicates whether the property is within 100 feet of a major road.

### Road Proximity 101 - 300 Feet
- **Variable Name:** `geo_withinmr101300`
- **Data Type:** Logical
- **Predictor:** Yes
- **Description:** Indicates whether the property is between 101 and 300 feet of a major road.

### Flood Risk Direction
- **Variable Name:** `geo_fs_flood_risk_direction`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** The property's flood risk direction represented in a numeric value based on the change in risk for the location from 2020 to 2050 for the climate model realization of the RCP 4.5 mid emissions scenario. -1 = descreasing, 0 = stationary, 1 = increasing. Data provided by First Street and academics at UPenn.

### Flood Risk Factor
- **Variable Name:** `geo_fs_flood_factor`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** The property's First Street Flood Factor, a numeric integer from 1-10 (where 1 = minimal and 10 = extreme) based on flooding risk to the building footprint. Flood risk is defined as a combination of cumulative risk over 30 years and flood depth. Flood depth is calculated at the lowest elevation of the building footprint (largest if more than 1 exists, or property centroid where footprint does not exist. Data provided by First Street and academics at UPenn.

### Elementary/Middle School District
- **Variable Name:** `geo_school_elem_district`
- **Data Type:** Character
- **Predictor:** Yes
- **Description:** Elementary and middle school district boundaries for Cook County and CPS.

### High School District
- **Variable Name:** `geo_school_hs_district`
- **Data Type:** Character
- **Predictor:** Yes
- **Description:** High school district boundaries for Cook County and CPS.

### Property Address
- **Variable Name:** `geo_property_address`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Property street address, not the address of the taxpayer.

### Property Apartment Num.
- **Variable Name:** `geo_property_apt_no`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Property street address, not the address of the taxpayer.

### Property City
- **Variable Name:** `geo_property_city`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Property street address, not the address of the taxpayer.

### Property Zip Code
- **Variable Name:** `geo_property_zip`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Property street address, not the address of the taxpayer.

### Mailing Address
- **Variable Name:** `geo_mailing_address`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Mailing address of the property owner.

### Mailing State
- **Variable Name:** `geo_mailing_state`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Mailing state of the property owner.

### Mailing City
- **Variable Name:** `geo_mailing_city`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Mailing city of the property owner.

### Mailing Zip Code
- **Variable Name:** `geo_mailing_zip`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Mailing zip code of the property owner.

### Public Use Microdata Area
- **Variable Name:** `geo_puma`
- **Data Type:** Character
- **Predictor:** No

### Illinois State Representative District
- **Variable Name:** `geo_reps_dist`
- **Data Type:** Character
- **Predictor:** No

### Illinois State Senate District
- **Variable Name:** `geo_senate_dist`
- **Data Type:** Character
- **Predictor:** No

### TIF Agency Number
- **Variable Name:** `geo_tif_agencynum`
- **Data Type:** Character
- **Predictor:** No

### City of Chicago Ward
- **Variable Name:** `geo_ward`
- **Data Type:** Character
- **Predictor:** No

### Special Service Area Name
- **Variable Name:** `geo_ssa_name`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Name of the City of Chicago Special Service Area the property lies within.

### Special Service Area Number
- **Variable Name:** `geo_ssa_no`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Number of the City of Chicago Special Service Area the property lies within.

---

## Indicator Variables (ind)

Binary indicators for property characteristics and sale conditions.

### Multi Code Indicator
- **Variable Name:** `ind_multi_code`
- **Data Type:** Logical
- **Predictor:** No
- **Description:** Indicates a property with multiple improvements on one PIN, e.g. a main house and a coach house. NOT to be confused with a property which was part of a multi-pin sale.

### Large Home Indicator
- **Variable Name:** `ind_large_home`
- **Data Type:** Logical
- **Predictor:** No
- **Description:** If true, property class is either 208 or 209.

### Class Code Error Indicator
- **Variable Name:** `ind_class_error`
- **Data Type:** Logical
- **Predictor:** No
- **Description:** If true, the recorded characteristics do not align with the recorded class. See chars_check_class() function in CCAO package for details.

### Large Lot Indicator
- **Variable Name:** `ind_large_lot`
- **Data Type:** Logical
- **Predictor:** Yes
- **Description:** Large lot factor variable, where 1 acre of land (land square feet > 43559) is defined as a large lot. 1 = large lot, 0 = not a large lot.

### Garage Indicator
- **Variable Name:** `ind_garage`
- **Data Type:** Logical
- **Predictor:** Yes
- **Description:** Indicates presence of a garage of any size.

### Pure Market Indicator
- **Variable Name:** `ind_pure_market`
- **Data Type:** Logical
- **Predictor:** No
- **Description:** Indicates whether a sale has pure market/arms length characteristics.

---

## Metadata (meta)

Administrative and assessment-related information about properties.

### Condition, Desirability, and Utility
- **Variable Name:** `meta_cdu`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Dozens of codes attached to face sheet that denote a number of seemingly unrelated characteristics associated with a PIN, ranging from condition to types of subsidies. This field does not match across the SQL server/AS-400.

### Property Class
- **Variable Name:** `meta_class`
- **Data Type:** Character
- **Predictor:** No

### Sale Document Number
- **Variable Name:** `meta_document_num`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Document number of a property sale, as recorded by the Clerk's office.

### Key PIN
- **Variable Name:** `meta_key_pin`
- **Data Type:** Character
- **Predictor:** No
- **Note:** Need to clarify definition.

### Multi Code
- **Variable Name:** `meta_multi_code`
- **Data Type:** Character/Categorical
- **Predictor:** No
- **Description:** Field that serves as a key when multiple buildings or improvements exist on the same PIN. Numeric values do not necessary correspond to number of buildings. Can also represent improvements added through Home Improvement Exemptions (288s).

### Modeling Group
- **Variable Name:** `meta_modeling_group`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Modeling group, as defined by the property class. Properties with class 200, 201, 241, 299 is defined as "NCHARS", short for "no characteristics", which are condos and vacant land classes. Properties with class 202, 203, 204, 205, 206, 207, 208, 209, 210, 235, 278, and 295 are "SF", short for "single-family." Properties with class 211 and 212 are "MF", short for "multi-family." Properties with class 218 and 219 are "BB", short for "bed and breakfast."

### Neighborhood Code
- **Variable Name:** `meta_nbhd`
- **Data Type:** Character
- **Predictor:** Yes
- **Description:** Assessor neighborhood. First 2 digits are township code, last 3 digits are neighborhood code.

### Percent Assessed
- **Variable Name:** `meta_per_ass`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Percent assessed for prorated properties. Percent of ownership of a condo building for a unit as defined by the condominium declaration. If missing, default is 1/n_units.

### Property Index Number
- **Variable Name:** `meta_pin`
- **Data Type:** Character
- **Predictor:** No
- **Description:** All PINs are 14 digits: 2 digits for area + 2 digits for sub area + 2 digits for block + 2 digits for parcel + 4 digits for the multicode

### 2 Years Prior BoR Estimate (Building)
- **Variable Name:** `meta_2yr_pri_board_est_bldg`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Board of Review final estimated market value of building from 2 years prior to observation year.

### 2 Years Prior BoR Estimate (Land)
- **Variable Name:** `meta_2yr_pri_board_est_land`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Board of Review final estimated market value of land from 2 years prior to observation year.

### 1 Year Prior BoR Estimate (Building)
- **Variable Name:** `meta_1yr_pri_board_est_bldg`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Board of Review final estimated market value of building from 1 year prior to observation year.

### 1 Year Prior BoR Estimate (Land)
- **Variable Name:** `meta_1yr_pri_board_est_land`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Board of Review final estimated market value of land from 1 year prior to observation year.

### Assessor Mailed Estimate (Building)
- **Variable Name:** `meta_mailed_est_bldg`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Assessor mailed estimated market value of building from observation year.

### Assessor Mailed Estimate (Land)
- **Variable Name:** `meta_mailed_est_land`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Assessor mailed estimated market value of land from observation year.

### Assessor Certified Estimate (Building)
- **Variable Name:** `meta_certified_est_bldg`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Assessor certified estimated market value of building from observation year.

### Assessor Certified Estimate (Land)
- **Variable Name:** `meta_certified_est_land`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Assessor certified estimated market value of land from observation year.

### Sale Date
- **Variable Name:** `meta_sale_date`
- **Data Type:** Date
- **Predictor:** No
- **Description:** Date of sale.

### Sale Price
- **Variable Name:** `meta_sale_price`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Market price of sale.

### Year
- **Variable Name:** `meta_year`
- **Data Type:** Numeric
- **Predictor:** No

### Township Name
- **Variable Name:** `meta_town_name`
- **Data Type:** Character
- **Predictor:** No

### Township Code
- **Variable Name:** `meta_town_code`
- **Data Type:** Character
- **Predictor:** Yes

### Sale Deed Type
- **Variable Name:** `meta_deed_type`
- **Data Type:** Character
- **Predictor:** No
- **Description:** Deed type of a property sale.

### Number of Active 288s (HIEs)
- **Variable Name:** `meta_num_288s_active`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Number of 288s (Home Improvement Exemptions) active for this property in the given year.

### Number of Ended 288s (HIEs)
- **Variable Name:** `meta_num_288s_ended`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Number of 288s (Home Improvement Exemptions) that ended in the given year. This is effectively an indicator for properties that have updated characteristics due to a 288 expiring.

### Neighborhood Mean Sale Price
- **Variable Name:** `meta_nbhd_avg`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Mean sale price of a given neighborhood. Can be used in lieu of neighborhood dummy variables in order to reduce sparsity.

### Neighborhood Median Sale Price
- **Variable Name:** `meta_nbhd_med`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Median sale price of a given neighborhood. Can be used in lieu of neighborhood dummy variables in order to reduce sparsity.

---

## Time Variables (time)

Temporal features derived from sale dates.

### Sale Year
- **Variable Name:** `time_sale_year`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Sale year calculated as the number of years since 0 B.C.E.

### Sale Quarter
- **Variable Name:** `time_sale_quarter`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Sale quarter calculated as the number of quarters since January 1997.

### Sale Month
- **Variable Name:** `time_sale_month`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Sale month calculated as the number of months since January 1997.

### Sale Week
- **Variable Name:** `time_sale_week`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Sale week calculated as the number of weeks since January 1st, 1997.

### Sale Day
- **Variable Name:** `time_sale_day`
- **Data Type:** Numeric
- **Predictor:** No
- **Description:** Sale day calculated as the number of days since January 1st, 1997.

### Sale Quarter of Year
- **Variable Name:** `time_sale_quarter_of_year`
- **Data Type:** Character
- **Predictor:** Yes
- **Description:** Character encoding of quarter of year (Q1 - Q4).

### Sale Month of Year
- **Variable Name:** `time_sale_month_of_year`
- **Data Type:** Character
- **Predictor:** Yes
- **Description:** Character encoding of month of year (Jan - Dec).

### Sale Week of Year
- **Variable Name:** `time_sale_week_of_year`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Numeric encoding of week of year (1 - 52).

### Sale Day of Year
- **Variable Name:** `time_sale_day_of_year`
- **Data Type:** Numeric
- **Predictor:** Yes
- **Description:** Numeric encoding of day of year (1 - 365).

### Sale During School Year
- **Variable Name:** `time_sale_during_school_year`
- **Data Type:** Logical
- **Predictor:** Yes
- **Description:** Indicator for whether sale occurred during usual school year (September - May).

### Sale During Holidays
- **Variable Name:** `time_sale_during_holidays`
- **Data Type:** Logical
- **Predictor:** Yes
- **Description:** Indicator for whether sale occurred during holiday season (November - January).

---

## Notes

- **Predictor:** Indicates whether the variable is used as a predictor in modeling
- **NA values:** Many categorical variables may have missing values
- **Data Source:** Cook County Assessor's Office (CCAO) property data

