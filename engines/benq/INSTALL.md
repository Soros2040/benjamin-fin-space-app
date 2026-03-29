# BenQ - AI-Oriented Quantitative Investment Platform

## Overview

This is the BenQ engine, a core component of Benjamin Fin Space App. It provides a comprehensive platform for quantitative investment research and production.

## Installation

### From Source

```bash
cd engines/benq
pip install -e .
```

### Development Installation

```bash
pip install -e .[dev]
```

## Quick Start

### 1. Initialize Data

```bash
python -m benq.cli.data benq_data --target_dir ~/.benjamin/benq_data/cn_data --region cn
```

### 2. Run a Model

```bash
benbenq examples/benchmarks/LightGBM/workflow_config_lightgbm_Alpha158.yaml
```

### 3. View Results

The results will be saved in the `mlruns` directory and can be viewed using the provided analysis tools.

## Project Structure

```
benq/
├── benq/                  # Core package
│   ├── data/             # Data processing modules
│   ├── model/            # Model implementations
│   ├── rl/               # Reinforcement learning
│   ├── strategy/         # Trading strategies
│   ├── workflow/         # Workflow management
│   └── cli/              # Command-line interface
├── examples/             # Example workflows
├── tests/                # Test cases
└── docs/                 # Documentation
```

## Key Features

- **Data Processing**: Efficient data loading and processing with caching
- **Model Training**: Support for various ML models (GBDT, Neural Networks, etc.)
- **Backtesting**: Comprehensive backtesting framework
- **Reinforcement Learning**: RL-based trading strategies
- **Workflow Automation**: Automated research workflows

## Documentation

For detailed documentation, please visit [https://benq.readthedocs.io/](https://benq.readthedocs.io/)

## License

MIT License
