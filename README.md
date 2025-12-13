# ESS Electives Survey Analysis

Comprehensive publication-ready analysis of ESS electives student feedback data.

## Overview

This repository contains a Jupyter notebook that performs an extensive analysis of student feedback on ESS elective courses, including:

- ✅ **Data Quality Assessment** - Comprehensive validation and filtering
- ✅ **Descriptive Statistics** - Full statistical analysis of all metrics
- ✅ **10+ Publication-Quality Visualizations** - High-resolution (300 DPI) figures
- ✅ **Correlation Analysis** - Relationships between metrics
- ✅ **Comparative Analysis** - Module II A vs Module II B comparisons
- ✅ **Key Insights** - Automated identification of top/bottom performers
- ✅ **Text Analysis** - Word frequency and word clouds for open-ended feedback
- ✅ **Actionable Recommendations** - Evidence-based suggestions

## Notebook Features

The enhanced `ESS_electives.ipynb` notebook includes **57 cells** organized into 11 major sections:

1. **Executive Summary** - Overview of key findings
2. **Setup & Configuration** - Package installation and environment setup
3. **Data Loading & Validation** - Quality checks and filtering
4. **Data Processing** - Course mapping and transformation to long format
5. **Descriptive Statistics** - Comprehensive statistical overview
6. **Statistical Analysis** - Correlations, significance tests, outlier identification
7. **Comprehensive Visualizations** - 10+ publication-ready figures
8. **Key Insights** - Automated insight generation
9. **Text Analysis** - Qualitative feedback analysis
10. **Recommendations** - Actionable improvement suggestions
11. **Exports** - Summary of all generated outputs

## Generated Outputs

When the notebook is run, it generates:

### Data Files (in `outputs/`)
- `data_dictionary.csv` - Mapping of courses to question columns
- `processed_course_feedback.csv` - Long-format analysis dataset
- `course_summary_statistics.csv` - Comprehensive course statistics
- `correlation_matrix.csv` - Correlation matrix between metrics
- `top_courses_summary.csv` - Summary of top courses
- `key_insights.json` - Automatically generated insights

### Visualizations (in `figures/`)
1. Response distribution bar chart
2. Course metrics heatmap
3. Difficulty box plots
4. Difficulty vs alignment scatter plot (bubble chart)
5. Correlation matrix heatmap
6. Re-enrolment intent distribution (stacked bars)
7. Difficulty violin plots
8. Module comparison (4-panel)
9. Pairwise scatter matrix
10. Positive feedback word cloud
11. Improvement feedback word cloud

All figures are exported at 300 DPI for publication quality.

## Usage

### Running in Google Colab
Click the "Open in Colab" badge at the top of the notebook, or visit:
[Open in Colab](https://colab.research.google.com/github/stfgrz/ESS_electives_report/blob/main/ESS_electives.ipynb)

### Running Locally

```bash
# Install required packages
pip install pandas numpy matplotlib seaborn scipy plotly wordcloud tabulate jupyter

# Start Jupyter
jupyter notebook ESS_electives.ipynb
```

Then run all cells in order.

## Requirements

- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- plotly (optional, for interactive visualizations)
- wordcloud (optional, for text analysis)
- tabulate

## Data Structure

The input CSV (`data/ESS_electives_op_DEC2025.csv`) has a special structure:
- **Row 0:** Question text
- **Row 1:** ImportId mappings
- **Rows 2+:** Survey responses

The notebook automatically handles this structure and provides:
- Filtering of preview/test responses
- Exclusion of incomplete surveys
- Proper handling of multi-select questions
- Text-to-numeric conversion for Likert scales

## Key Features

### Automated Insights
The notebook automatically identifies:
- Most/least difficult courses
- Best/worst exam alignment
- Highest/lowest re-enrolment intent
- "Hidden gems" (high satisfaction, lower difficulty)
- "Challenging but rewarding" courses
- Courses needing attention

### Statistical Rigor
- Minimum response thresholds (configurable, default: 3)
- Correlation analysis (Pearson)
- Statistical significance testing (t-tests, Mann-Whitney U)
- Variance analysis for polarizing courses
- Module comparison with significance tests

### Code Quality
- Comprehensive docstrings
- Reusable utility functions
- Error handling and validation
- Configuration variables for easy adjustments
- Clear markdown documentation
- Professional formatting

## Configuration

Key configuration variables (in Setup section):
```python
DATA_PATH = 'data/ESS_electives_op_DEC2025.csv'
OUTPUT_DIR = 'outputs'
FIGURE_DIR = 'figures'
MIN_RESPONSES = 3      # Minimum responses for course analysis
FIGURE_DPI = 300       # Resolution for publication-ready figures
RANDOM_SEED = 42       # For reproducibility
```

## Contributing

This analysis can be extended to include:
- Time-series analysis across semesters
- Predictive modeling for course difficulty
- Interactive dashboards with Plotly
- Advanced NLP for qualitative feedback
- Comparison with previous years' data

## License

This project is part of the ESS program analysis toolkit.

## Contact

For questions or suggestions about this analysis, please open an issue on GitHub.