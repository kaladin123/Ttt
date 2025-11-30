Here's a tailored prompt for converting an ETL Jupyter notebook into organized, maintainable Python code:

```
Convert this ETL Jupyter notebook into production-ready Python code following ETL best practices:

## ETL Architecture
- Separate Extract, Transform, and Load logic into distinct modules
- Implement proper error handling and data validation at each stage
- Add logging for monitoring data flow and debugging
- Make the pipeline configurable and reusable for different data sources

## Project Structure
```
etl_project/
├── src/
│   ├── __init__.py
│   ├── config.py              # Configuration, connections, paths
│   ├── extractors/
│   │   ├── __init__.py
│   │   └── data_extractor.py  # Data extraction logic
│   ├── transformers/
│   │   ├── __init__.py
│   │   ├── data_cleaner.py    # Data cleaning operations
│   │   ├── data_validator.py  # Data validation rules
│   │   └── data_transformer.py # Transformation logic
│   ├── loaders/
│   │   ├── __init__.py
│   │   └── data_loader.py     # Load to destination
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── logger.py          # Logging configuration
│   │   └── helpers.py         # Helper functions
│   └── pipeline.py            # Orchestrate ETL pipeline
├── tests/
│   └── test_*.py
├── config/
│   └── pipeline_config.yaml   # Pipeline configurations
├── logs/                      # Log files
├── main.py                    # Entry point
└── requirements.txt
```

## Code Quality Requirements
- Add type hints for all function parameters and returns
- Include docstrings explaining what each ETL step does
- Implement data quality checks and validation rules
- Add proper exception handling with meaningful error messages
- Use context managers for database/file connections
- Make database credentials and file paths configurable (not hardcoded)

## ETL-Specific Features
- Implement incremental loading capabilities where applicable
- Add data profiling/summary statistics logging
- Create checkpoint/restart functionality for long-running processes
- Track record counts at each stage (extracted, transformed, loaded)
- Implement data quality metrics and validation checks
- Add transaction handling for database operations

## Configuration Management
- Extract all connection strings, file paths, and parameters to config files
- Support different environments (dev, staging, prod)
- Use environment variables for sensitive information

## Logging & Monitoring
- Log start/end times for each ETL stage
- Log record counts and data volumes processed
- Log any data quality issues or validation failures
- Create summary reports after pipeline execution

## Testing
- Add unit tests for transformation logic
- Include data validation test cases
- Test error handling scenarios

## CLI Interface
- Make the pipeline runnable from command line
- Support arguments for: --config, --env, --source, --destination
- Add options for running specific stages only (extract/transform/load)
- Include dry-run mode for testing

## Performance Considerations
- Use batch processing for large datasets where appropriate
- Implement connection pooling for database operations
- Add progress indicators for long-running operations

Please ensure the code is modular, testable, and follows data engineering best practices while maintaining all original ETL functionality.
```

This prompt is specifically designed for ETL workflows and will help Copilot create a robust, production-grade data pipeline from your notebook.
