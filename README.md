# Benjamin Fin Space App

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.12+](https://img.shields.io/badge/python-3.12+-blue.svg)](https://www.python.org/downloads/)
[![Flutter 3.24+](https://img.shields.io/badge/flutter-3.24+-blue.svg)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/platform-linux%20%7C%20windows%20%7C%20macos-lightgrey)](https://github.com/Soros2040/benjamin-fin-space-app)

**Benjamin** is an open-source, AI-oriented quantitative investment platform that aims to realize the potential, empower research, and create value using AI technologies in quantitative investment, from exploring ideas to implementing productions.

## 🌟 Overview

Benjamin combines two powerful engines:

- **BenQ Engine**: An AI-oriented quantitative investment platform supporting diverse machine learning modeling paradigms, including supervised learning, market dynamics modeling, and reinforcement learning.
- **Alex Engine**: A LLM-powered application platform based on Dify, providing intuitive interface for crafting AI workflows, RAG pipelines, agent capabilities, and model management.

## 📁 Project Structure

```
benjamin/
├── engines/
│   ├── benq/          # Quantitative investment engine (based on Microsoft Qlib)
│   └── alex/          # AI application engine (based on Dify)
│       ├── dify/      # Dify core
│       ├── dify-agentbox/
│       ├── dify-marketplace/
│       ├── dify-plugin-daemon/
│       ├── dify-plugin-sdks/
│       ├── dify-sandbox/
│       └── homebrew-dify/
├── apps/
│   ├── mobile/        # Flutter mobile app (iOS, Android, Web, HarmonyOS)
│   └── web/           # Web applications
└── flutter/           # Flutter SDK
```

## 🚀 Quick Start

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/Soros2040/benjamin-fin-space-app.git
cd benjamin-fin-space-app/benjamin
```

#### 2. Install BenQ Engine

```bash
cd engines/benq
pip install .
```

For development:
```bash
pip install -e .[dev]
```

#### 3. Setup Alex Engine (Dify)

```bash
cd engines/alex/dify/docker
cp .env.example .env
docker compose up -d
```

Access Dify dashboard at [http://localhost/install](http://localhost/install)

#### 4. Run Mobile App

```bash
cd apps/mobile
# Flutter SDK is included in the project root
../../flutter/bin/flutter run -d chrome
```

### Data Preparation

```bash
# Get 1d data
python -m benq.cli.data benq_data --target_dir ~/.benjamin/benq_data/cn_data --region cn

# Get 1min data
python -m benq.cli.data benq_data --target_dir ~/.benjamin/benq_data/cn_data_1min --region cn --interval 1min
```

## 🎯 Core Features

### BenQ Engine (Quantitative Investment)

- **Forecasting Models**: GBDT (XGBoost, LightGBM, CatBoost), LSTM, GRU, ALSTM, GATs, SFM, TFT, TabNet, Transformer, Localformer, and more
- **Market Dynamics Adaptation**: Rolling retraining, DDG-DA
- **Reinforcement Learning**: Order execution with PPO, OPDS, TWAP
- **RL Learning Framework**: End-to-end optimization
- **Dataset Zoo**: Alpha360, Alpha158
- **Workflow Automation**: Auto quant research workflow with graphical reports

### Alex Engine (AI Applications)

- **Workflow Builder**: Visual AI workflow canvas
- **Model Support**: 100+ LLMs (GPT, Mistral, Llama3, etc.)
- **Prompt IDE**: Craft prompts, compare model performance
- **RAG Pipeline**: Document ingestion and retrieval
- **Agent Capabilities**: Function calling, ReAct, 50+ built-in tools
- **LLMOps**: Monitor and analyze application logs
- **Backend-as-a-Service**: Complete API support

### Mobile App (Flutter)

- **Market**: Market indices, watchlist, market trends
- **Community**: Investment discussion, strategy sharing
- **Studio**: Agent creation, workflow orchestration
- **Marketplace**: Agent tools, trading strategies, data services
- **Settings**: Personal account, trading configuration

## 📊 Performance

### BenQ Data Server Performance

| Storage Solution | Total Time (1CPU) | Total Time (64CPU) |
|-----------------|-------------------|-------------------|
| HDF5            | 184.4±3.7s        | -                 |
| MySQL           | 365.3±7.5s        | -                 |
| MongoDB         | 253.6±6.7s        | -                 |
| InfluxDB        | 368.2±3.6s        | -                 |
| **BenQ +E +D**  | **7.4±0.3s**      | -                 |
| BenQ +E -D      | 47.6±1.0s         | **4.2±0.2s**      |
| BenQ -E -D      | 147.0±8.8s        | 8.8±0.6s          |

*+(-)E: with(out) ExpressionCache, +(-)D: with(out) DatasetCache*

## 📚 Documentation

- [BenQ Documentation](https://benq.readthedocs.io/)
- [Alex (Dify) Documentation](https://docs.dify.ai/)
- [Flutter Documentation](https://flutter.dev/docs)

## 🤝 Contributing

We welcome all contributions! Please see our [Contribution Guide](CONTRIBUTING.md) for details.

### Ways to Contribute

- **Code**: Fix bugs, implement features, improve performance
- **Documentation**: Improve docs, fix typos, add examples
- **Models**: Add new quantitative models
- **Dataset**: Contribute new datasets
- **Translation**: Help translate Dify into your language

### Development Setup

```bash
# Clone and install for development
git clone https://github.com/Soros2040/benjamin-fin-space-app.git
cd benjamin-fin-space-app/benjamin

# Install BenQ in development mode
cd engines/benq
pip install -e .[dev]

# Setup Dify for development
cd ../alex/dify
# Follow https://docs.dify.ai/getting-started/install-self-hosted/local-source-code
```

## 📄 License

This project is licensed under multiple licenses:

- **BenQ Engine**: MIT License
- **Alex Engine (Dify)**: Dify Open Source License (Apache 2.0 with additional conditions)
- **Flutter SDK**: BSD 3-Clause License

See individual component LICENSE files for details.

## 🙏 Acknowledgments

Benjamin is built on top of excellent open-source projects:

- [Microsoft Qlib](https://github.com/microsoft/qlib) - BenQ engine base
- [Dify](https://github.com/langgenius/dify) - Alex engine base
- [Flutter](https://github.com/flutter/flutter) - Mobile app framework

## 📬 Contact Us

- **Issues**: [GitHub Issues](https://github.com/Soros2040/benjamin-fin-space-app/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Soros2040/benjamin-fin-space-app/discussions)
- **Email**: benjamin@example.com

## 🗺️ Roadmap

- [ ] Enhanced RL trading strategies
- [ ] More LLM integrations in Alex
- [ ] Mobile app production release
- [ ] Real-time market data integration
- [ ] Advanced backtesting engine
- [ ] Multi-language support

## 📈 Stats

![GitHub stars](https://img.shields.io/github/stars/Soros2040/benjamin-fin-space-app?style=social)
![GitHub forks](https://img.shields.io/github/forks/Soros2040/benjamin-fin-space-app?style=social)
![GitHub issues](https://img.shields.io/github/issues/Soros2040/benjamin-fin-space-app)
![GitHub pull requests](https://img.shields.io/github/issues-pr/Soros2040/benjamin-fin-space-app)

---

**Made with ❤️ by the Benjamin Team**