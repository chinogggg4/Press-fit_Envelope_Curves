# Press-Fit Envelope Curves Calculator

## Project Overview
The Press-Fit Envelope Curves Calculator is a Python-based web application developed to automate the generation of process control envelopes for Press-Fit manufacturing operations. The tool was designed to run directly in Google Colab, eliminating the need for software installation and enabling easy deployment across manufacturing and quality teams.

The application imports Press-Fit force-displacement curve data from Excel (.xlsx) or CSV files, preprocesses and standardizes the datasets, calculates statistical envelope limits, and provides an interactive environment for curve validation and analysis.

By automating a traditionally manual and time-consuming task, the application improves consistency, reduces engineering effort, and facilitates data-driven process validation.

## Objectives

- Automate the generation of Press-Fit envelope curves.
- Standardize curve processing and analysis.
- Reduce manual calculations and engineering lead time.
- Improve process validation consistency across production lines.
- Provide a user-friendly interface that requires no programming knowledge.

## Key Features

### Data Import

The application supports:

- Excel files (.xlsx)
- CSV files (.csv)

Data can be uploaded directly from a local computer through the graphical interface.

### Data Preprocessing

Once the files are loaded, the software:

- Extracts force and displacement measurements.
- Converts and formats raw data into a standardized structure.
- Validates data integrity before processing.

### Curve Interpolation

Since individual Press-Fit curves often contain different numbers of measurement points, the software performs interpolation to align all curves onto a common distance scale.

This enables accurate point-by-point statistical analysis across the entire dataset.

### Envelope Curve Calculation

The application calculates upper and lower envelope limits based on a user-defined sigma level.

The user can adjust:

- Resolution: Number of interpolation points used for each curve.
- Sigma Value: Standard deviation multiplier used to generate the envelope limits.
- Envelope Point Count: Number of points included in the final envelope table.

### Interactive Visualization

An interactive plot allows users to:

- Visualize all imported curves.
- Review the calculated envelope limits.
- Dynamically update calculation parameters.
- Evaluate process behavior before exporting results.

### Curve Filtering

To improve envelope quality, users can:

- Remove individual curves identified as non-representative or generated from unsuccessful assemblies.
- Automatically remove the final point from all curves to eliminate measurement noise commonly observed at the end of Press-Fit cycles.

### Exportable Results

Once the analysis is complete, users can copy the generated envelope point table for implementation in production equipment or process validation documentation.

## Technical Implementation

### Development Environment

- Python
- Google Colab
- Pandas
- NumPy
- SciPy
- Plotly

### Processing Workflow
1. Import curve data from Excel or CSV files.
2. Extract force and displacement information.
3. Standardize and clean datasets.
4. Interpolate all curves to a common distance axis.
5. Calculate mean and standard deviation at each interpolation point.
6. Generate upper and lower envelope limits using the selected sigma level.
7. Display interactive visualizations.
8. Allow user-driven curve filtering and parameter adjustment.
9. Generate final envelope point tables.

### Design Considerations

To simplify usage for production and quality personnel, the entire application was implemented within a single executable code block in Google Colab. This design prevents execution-order errors and ensures that users only need to run the notebook once to access all functionalities.

## User Guide
### Running the Application
1. Open the Google Colab notebook.
2. Execute the main code cell by clicking the Run (▶) button or pressing Ctrl + Enter.
3. Scroll to the final section of the notebook.
4. Select whether the data corresponds to:
    - Production Curves
    - Minimum/Maximum Curves
5. Select the Press-Fit system type:
    - Kistler
    - Promess
6. Click Upload Files.
7. Select the corresponding Excel or CSV file.
8. Wait for the upload and processing to complete.
9. Review the interactive graph.
10. Adjust parameters as needed:
    - Resolution
    - Sigma value
    - Envelope point count
11. Optionally:
    - Remove invalid curves.
    - Remove the final point from all curves.
12. Copy the generated envelope table for use in process validation.
13. To perform a new analysis, restart the workflow from Step 1.

## Benefits
- Reduces manual engineering effort.
- Standardizes Press-Fit envelope generation.
- Improves repeatability and consistency.
- Supports data-driven process validation.
- Provides rapid analysis of large datasets.
- Enables interactive quality assessment and outlier identification.

## Contact Information

**Juan Pablo Ramírez Guerra**

 Process Engineer | Data Scientist

📧 juan.2.ramirez.guerra@aumovio.com

 📞 +52 33 3455 0363
