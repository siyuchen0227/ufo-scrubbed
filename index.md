
# UFO Sighting Data Visualization Analysis

## Dataset Overview

- Data Source: UIUC iSchool DataViz
- Time Range: {df['datetime'].min().year} to {df['datetime'].max().year}
- Total Records: {len(df)}
- Geographic Coverage: UFO sighting records from multiple countries

## Visualization 1: Geographic Distribution Heat Map

- **Description**: Displays the global geographic distribution of UFO sightings

- **Design Choices**:

  - Uses circle markers (mark_circle) to intuitively show event locations
  - Implements viridis color scheme, suitable for quantity variation and colorblind-friendly
  - Circle size (size) encodes sighting count, range 50-1000
  - Color intensity (color) encodes sighting frequency

- **Interactive Features**:

  - Year slider: Filter data for specific years
  - Hover tooltip: Shows state/region, sighting count, UFO shape, and other details

- **Data Transformation**:

  - Latitude/longitude numerical processing
  - Outlier and missing value cleaning

## Visualization 2: Temporal Trend Analysis

- **Description**: Analyzes temporal distribution patterns of different UFO shapes

- **Design Choices**:

  - Uses line chart (mark_line) to show temporal trends, facilitating pattern observation
  - Multi-color scheme to distinguish different UFO shapes
  - X-axis uses time scale, Y-axis shows sighting counts

- **Interactive Features**:

  - UFO shape selector: Filter historical records by specific shapes
  - Dynamic tooltip: Displays year, shape, and exact counts

- **Data Aggregation**:

  - Grouping statistics by year and shape
  - Time series data standardization

## Data Processing Pipeline

1. Data Cleaning:

   - Standardize datetime format
   - Handle missing values (fill shapes with 'unknown')
   - Validate geographic coordinate validity

2. Feature Extraction:

   - Extract year and month from datetime
   - Convert latitude/longitude to numeric type
   - Standardize UFO shape categories

3. Data Transformation:

   - Create time series aggregations
   - Calculate geographic distribution density
   - Generate data structures for interactivity

## Visualization Objectives

- Demonstrate spatial-temporal patterns of UFO sightings
- Discover temporal patterns of different UFO shapes
- Provide intuitive interactive data exploration experience

### Final Chart Composition

The final chart is created by vertically concatenating the geographic distribution chart (`chart1`) and the temporal trend analysis chart (`chart2`). This combined visualization allows users to explore both the spatial distribution of UFO sightings and the temporal trends in a cohesive manner, facilitating a comprehensive understanding of the data.


