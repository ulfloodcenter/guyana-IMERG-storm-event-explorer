# Storm Event Explorer — Region 4, Guyana

**IMERG Rainfall Event Catalogue | 2020–2023**

An interactive catalogue and rainfall visualization resource for storm events in **Region 4, Guyana**, developed in connection with research at the **University of Louisiana at Lafayette / Louisiana Watershed Flood Center**.

The explorer provides a browser-based interface to examine screened rainfall events, inspect summary statistics, view spatial rainfall patterns through time, and access event-specific NetCDF files.

## Explore the dashboard

**Interactive website:** https://ulfloodcenter.github.io/guyana-IMERG-storm-event-explorer/

The site is hosted with GitHub Pages. If the link is unavailable, use the repository's GitHub Pages settings to confirm the current deployment address.

## Rainfall data source

The catalogue is based on **NASA Global Precipitation Measurement (GPM) Integrated Multi-satellitE Retrievals for GPM (IMERG), Final Run, Version 07 (V07)**, as confirmed by the research team. IMERG Final Run is a research-oriented, gridded satellite precipitation product incorporating monthly gauge-based adjustments. The native product provides precipitation estimates at **0.1° spatial resolution (approximately 10 km)** and **30-minute temporal resolution**.

**Important distinction:** These are the *native product specifications*. The supplied catalogue and dashboard do not establish whether the student aggregated the data in time, resampled it in space, or otherwise transformed it before constructing the event files. The exact source variable and granule identifiers have not been independently checked.

Product information: [NASA GPM IMERG](https://gpm.nasa.gov/data/imerg).

## Catalogue overview

The accompanying `Storm_Event_Catalogue_2020-2023.csv` contains **145 selected storm events**:

| Year | Events |
| --- | ---: |
| 2020 | 38 |
| 2021 | 34 |
| 2022 | 41 |
| 2023 | 32 |
| **Total** | **145** |

The catalogue records the event year and identifier, start and end times, duration, rainfall statistics, screening-related metrics, and relative paths to each event's interactive viewer and NetCDF dataset. The event dates in the dashboard are presented in **UTC**; rainfall amounts are reported in **millimeters**.

## Features

- Search, filter, and select events by year and other catalogue attributes.
- Examine event duration, mean and maximum rainfall, peak wet-area percentage, and boundary-share percentage.
- Explore spatial rainfall patterns using interactive maps and time-step playback.
- Switch between full-event accumulation, rolling 3-hour rainfall, 30-minute rainfall, and cumulative rainfall up to the selected time.
- Open an individual event viewer or download its NetCDF dataset.
- Download the complete CSV event catalogue.

## Repository contents

```text
index.html
Storm_Event_Catalogue_2020-2023.csv
assets/
2020/
2021/
2022/
2023/
README.md
```

Each annual folder contains event-specific HTML viewer resources and NetCDF files. **Keep the folder hierarchy unchanged:** the dashboard uses relative links to reach these files.

## Catalogue fields

| Field | Description |
| --- | --- |
| `year` | Event year |
| `event` | Event identifier within that year |
| `start`, `end` | Event start and end timestamps (UTC in the dashboard) |
| `duration` | Event duration, hours |
| `mean`, `max` | Event rainfall summary statistics, millimeters |
| `wet` | Wet-area metric, displayed as a percentage |
| `boundary` | Boundary-share metric, displayed as a percentage |
| `viewer` | Relative path to event-specific HTML viewer |
| `netcdf` | Relative path to event-specific NetCDF file |
| `iso` | Machine-readable event start time |
| `month` | Month number |

**Interpretation note:** The precise spatial and temporal definitions of `mean`, `max`, `wet`, and `boundary` should be verified against the original processing workflow before using these metrics in a scientific analysis.

## Event selection and methodology

The dashboard describes the selected events as having passed screening for **temporal completeness, spatial penetration, and minimum rainfall magnitude**. It also indicates that the event-map time windows correspond to those of the associated NetCDF files.

The rainfall source has been identified as **IMERG Final Run V07**, but the supplied dashboard and catalogue do **not** fully document the numerical thresholds, event-identification algorithm, processing steps, or exact study-area boundary used to identify and screen events. These details are not inferred here. They can be added in a future version when processing documentation becomes available. The catalogue can be shared as a documented data product in the meantime; users should not treat its event-selection procedure as fully reproducible from this README alone.

## Data use and limitations

This catalogue is a selection of screened rainfall events, **not necessarily a complete inventory of every rainfall event** during 2020–2023. IMERG Final Run includes gauge adjustment, but that does not establish local validation of the extracted events in Region 4. Satellite-derived rainfall estimates and event-selection procedures can introduce uncertainties. Users should not assume that the displayed rainfall is ground-validated or suitable for design, operational warning, or regulatory decisions without additional evaluation.

## Funding and attribution

This work is associated with the University of Louisiana at Lafayette and the Louisiana Watershed Flood Center.

**Funding:** National Science Foundation, Award **2426270**, as acknowledged in the dashboard.

**Contributors:** See the dashboard's research-team credits. Contributor names, roles, and preferred affiliations should be confirmed before formal publication.

## Citation and archiving

A formal citation and DOI can be added when the research team archives and formally publishes a specific version of the dataset in **CUAHSI HydroShare**. The current documentation explicitly identifies methodological details that have not been verified.

Until then, cite the GitHub repository and its release/version or commit date, and acknowledge the research team and NSF funding as appropriate. The interactive website may be updated independently of an archived release.

## Reuse and licensing

**No reuse license is specified here.** The research team should choose a suitable code license and data-use terms after confirming rights to the underlying data, software, logos, and third-party basemap services. Public accessibility alone does not grant permission for unrestricted reuse.

## Questions and updates

For corrections, issues, and updates, use the GitHub repository's **Issues** section if enabled, or contact the research team through its institutional channels.
