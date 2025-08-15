# Intro to MLOps

A hands-on learning project to understand Machine Learning Operations (MLOps) fundamentals and best practices.

## 🎯 What is MLOps?

MLOps (Machine Learning Operations) is the practice of applying DevOps principles to machine learning workflows. It bridges the gap between data science experimentation and production deployment, ensuring that ML models are:
- **Reproducible**: Same code + data = same results
- **Scalable**: Can handle increased load and data volume
- **Maintainable**: Easy to update, debug, and improve
- **Monitored**: Performance and quality are tracked over time

## 📚 Learning Objectives

By working through this project, you'll learn:

1. **Project Structure**: How to organize ML code for collaboration and maintainability
2. **Environment Management**: Using Poetry for dependency management
3. **Code Quality**: Automated formatting, linting, and quality checks with pre-commit
4. **Configuration Management**: Using Hydra for managing parameters and experiments
5. **Data Versioning**: Tracking datasets with DVC (Data Version Control)
6. **Pipeline Creation**: Building reproducible ML workflows
7. **Experiment Tracking**: Logging and comparing model experiments
8. **Testing**: Writing tests for ML code and data
9. **Documentation**: Creating clear documentation for ML projects

## 🏗️ Project Structure

```
intro-to-mlops/
├── README.md                 # This file - project overview and setup
├── pyproject.toml           # Poetry configuration and dependencies
├── poetry.lock              # Locked dependency versions
├── .pre-commit-config.yaml  # Pre-commit hooks configuration (coming soon)
├── Makefile                 # Task automation and common commands (coming soon)
├── dvc.yaml                 # DVC pipeline definition (coming soon)
├── params.yaml              # Model parameters and configuration (coming soon)
│
├── data/                    # Data storage (managed by DVC)
│   ├── raw/                 # Original, immutable data
│   ├── processed/           # Cleaned and preprocessed data
│   └── final/               # Final datasets for modeling
│
├── notebooks/               # Jupyter notebooks for exploration
│   └── checking-personal-kernel.ipynb
│
├── src/intro_to_mlops/     # Source code package
│   ├── __init__.py
│   ├── data/               # Data processing modules (coming soon)
│   ├── features/           # Feature engineering (coming soon)
│   ├── models/             # Model training and prediction (coming soon)
│   └── tests/              # Test modules
│       └── __init__.py
│
└── configs/                # Hydra configuration files (coming soon)
    ├── config.yaml         # Main configuration file
    ├── model/              # Model-specific configs
    ├── data/               # Data processing configs
    └── experiment/         # Experiment configurations
```

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or higher
- [Poetry](https://python-poetry.org/docs/#installation) for dependency management

### Installation

1. **Clone the repository**:
   ```bash
   git clone <your-repo-url>
   cd intro-to-mlops
   ```

2. **Install dependencies with Poetry**:
   ```bash
   poetry install
   ```

3. **Activate the virtual environment**:
   ```bash
   poetry shell
   ```

4. **Verify installation**:
   ```bash
   poetry run jupyter --version
   ```

5. **Set up pre-commit hooks for code quality**:
   ```bash
   poetry run pre-commit install
   ```

6. **Create a Makefile for automation** (optional but recommended):
   ```bash
   # Example Makefile commands you can create:
   make setup     # Install dependencies and initialize tools
   make data      # Download and process data
   make train     # Train models
   make test      # Run tests
   make clean     # Clean temporary files
   ```

### First Steps

1. **Explore the notebooks**:
   ```bash
   poetry run jupyter notebook notebooks/
   ```

2. **Initialize DVC** (for data versioning):
   ```bash
   poetry run dvc init
   ```

## 🔧 Tools and Technologies

### Core Dependencies

- **Poetry**: Dependency management and packaging
- **DVC**: Data version control and pipeline management
- **Jupyter**: Interactive development and experimentation
- **Cookiecutter**: Project templating (for creating new projects)
- **Makefile**: Task automation and workflow management
- **Hydra**: Configuration management and experiment orchestration
- **Hydra-Colorlog**: Enhanced logging with color output for Hydra
- **Pre-commit**: Automated code quality checks and formatting

### Development Dependencies

- **ipykernel**: Jupyter kernel for the virtual environment

## 📖 Learning Path

### Phase 1: Setup and Exploration
- [ ] Set up the development environment
- [ ] Configure pre-commit hooks for code quality
- [ ] Explore the project structure
- [ ] Create your first Jupyter notebook
- [ ] Learn basic DVC commands

### Phase 2: Data Management
- [ ] Add sample data to `data/raw/`
- [ ] Create data processing scripts
- [ ] Set up Hydra configuration files
- [ ] Version data with DVC
- [ ] Build data validation tests

### Phase 3: Model Development
- [ ] Create feature engineering pipeline
- [ ] Implement model training scripts
- [ ] Add model evaluation metrics
- [ ] Set up experiment tracking

### Phase 4: Pipeline Automation
- [ ] Define DVC pipelines
- [ ] Create configuration files
- [ ] Build Makefile for common tasks
- [ ] Add automated testing
- [ ] Set up continuous integration

### Phase 5: Advanced Topics
- [ ] Model deployment strategies
- [ ] Monitoring and alerting
- [ ] A/B testing frameworks
- [ ] Model registry and versioning

## 🧪 Testing

Run tests to ensure everything works correctly:

```bash
# Run all tests (when implemented)
poetry run pytest

# Run specific test files
poetry run pytest src/intro_to_mlops/tests/test_data.py
```

## 📝 Best Practices

### Code Organization
- Keep data processing, feature engineering, and modeling separate
- Use Hydra configuration files instead of hardcoded parameters
- Organize configs by component (data, model, experiment)
- Write docstrings and comments explaining the "why"

### Code Quality
- Use pre-commit hooks to enforce consistent code style
- Run automatic formatting (black, isort) before commits
- Implement linting (ruff, flake8) to catch potential issues
- Keep code clean and readable for team collaboration

### Data Management
- Never commit raw data to Git (use DVC instead)
- Document data sources and collection methods
- Validate data quality at each stage

### Configuration Management
- Use Hydra for all configurable parameters
- Create separate configs for different experiments
- Version control your configuration files
- Override configs from command line for quick experiments

### Experimentation
- Track all experiments with clear naming
- Save model artifacts and metrics
- Document what worked and what didn't

### Automation
- Use Makefile to standardize common commands
- Create reproducible workflows that others can easily run
- Automate testing, data processing, and model training
- Document all automation steps in the Makefile

### Collaboration
- Use clear commit messages
- Update documentation when adding features
- Review code before merging

## 🤝 Contributing

This is a learning project! Feel free to:
- Add new features or examples
- Improve documentation
- Share interesting experiments
- Ask questions in issues

## 📚 Additional Resources

### MLOps Learning
- [MLOps Zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp)
- [Made With ML](https://madewithml.com/)
- [Full Stack Deep Learning](https://fullstackdeeplearning.com/)

### Tools Documentation
- [Poetry Documentation](https://python-poetry.org/docs/)
- [DVC Documentation](https://dvc.org/doc)
- [Hydra Documentation](https://hydra.cc/docs/intro/)
- [Pre-commit Documentation](https://pre-commit.com/)
- [Jupyter Documentation](https://jupyter.org/documentation)

### Best Practices
- [Google's Rules of ML](https://developers.google.com/machine-learning/guides/rules-of-ml)
- [The Twelve-Factor App](https://12factor.net/)
- [Software Engineering for Data Scientists](https://github.com/drivendataorg/cookiecutter-data-science)

## 🆘 Troubleshooting

### Common Issues

**Poetry not found**: Make sure Poetry is installed and in your PATH
```bash
curl -sSL https://install.python-poetry.org | python3 -
```

**Kernel not found in Jupyter**: Install the kernel in your environment
```bash
poetry run python -m ipykernel install --user --name intro-to-mlops
```

**DVC commands fail**: Make sure DVC is installed in your environment
```bash
poetry show dvc
```

**Pre-commit hooks not running**: Install and configure pre-commit hooks
```bash
poetry run pre-commit install
poetry run pre-commit run --all-files  # Test all hooks
```

---

## 🎉 Next Steps

Start with the notebooks in the `notebooks/` directory to get familiar with the environment, then gradually build out the pipeline components in `src/intro_to_mlops/`.

Happy learning! 🚀

---

*This project is designed for educational purposes. As you learn, feel free to experiment and break things - that's how we learn best!*
