[![Python Versions](https://img.shields.io/pypi/pyversions/benq.svg?logo=python&logoColor=white)](https://pypi.org/project/benq/#files)
[![Platform](https://img.shields.io/badge/platform-linux%20%7C%20windows%20%7C%20macos-lightgrey)](https://pypi.org/project/benq/#files)
[![PypI Versions](https://img.shields.io/pypi/v/benq)](https://pypi.org/project/benq/#history)
[![Github Actions Test Status](https://github.com/microsoft/benq/workflows/Test/badge.svg?branch=main)](https://github.com/microsoft/benq/actions)
[![Documentation Status](https://readthedocs.org/projects/benq/badge/?version=latest)](https://benq.readthedocs.io/en/latest/?badge=latest)
[![License](https://img.shields.io/pypi/l/benq)](LICENSE)

## What's NEW! 

### Introducing RD-Agent: LLM-Based Autonomous Evolving Agents for Industrial Data-Driven R&D

We are excited to announce the release of **RD-Agent**, a powerful tool that supports automated factor mining and model optimization in quant investment R&D.

RD-Agent is now available on [GitHub](https://github.com/microsoft/RD-Agent)

## Overview

benq is an open-source, AI-oriented quantitative investment platform that aims to realize the potential, empower research, and create value using AI technologies in quantitative investment, from exploring ideas to implementing productions. benq supports diverse machine learning modeling paradigms, including supervised learning, market dynamics modeling, and reinforcement learning.

An increasing number of SOTA Quant research works/papers in diverse paradigms are being released in benq to collaboratively solve key challenges in quantitative investment.

## Quick Start

### Installation

```bash
pip install benq
```

### Data Preparation

```bash
# Get 1d data
python -m benq.cli.data benq_data --target_dir ~/.benq/benq_data/cn_data --region cn

# Get 1min data
python -m benq.cli.data benq_data --target_dir ~/.benq/benq_data/cn_data_1min --region cn --interval 1min
```

### Run Workflow

```bash
cd examples
benbenq benchmarks/LightGBM/workflow_config_lightgbm_Alpha158.yaml
```

## Features

- **Forecasting Models**: GBDT, LSTM, GRU, ALSTM, GATs, SFM, TFT, TabNet, Transformer, etc.
- **Market Dynamics**: Rolling retraining, DDG-DA
- **Reinforcement Learning**: Order execution with PPO, OPDS
- **Dataset Zoo**: Alpha360, Alpha158
- **Workflow Automation**: Auto quant research with graphical reports

## Documentation

Full documentation is available at [https://benq.readthedocs.io/](https://benq.readthedocs.io/)

## License

MIT License
