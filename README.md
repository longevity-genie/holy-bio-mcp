# Holy Bio MCP: A Unified MCP Framework for Bioinformatics Research

<div align="center">
  <img src="https://github.com/longevity-genie/holy-bio-mcp/blob/main/assets/holy-bio-logo.png?raw=true" alt="Holy Bio MCP Logo" width="200"/>
  
  [![MCP](https://img.shields.io/badge/MCP-Model%20Context%20Protocol-blue)](https://modelcontextprotocol.io)
  [![Longevity](https://img.shields.io/badge/Focus-Longevity%20Research-green)](https://github.com/longevity-genie)
  [![Bioinformatics](https://img.shields.io/badge/Tools-Bioinformatics-orange)](https://github.com/longevity-genie)
</div>

---

## 🎯 Our Mission

Holy Bio MCP is a unified framework born during Bio x AI Hackathon-2025 from our practical experience building LLM-powered agents at the **Longevity Genie project**, **IBIMA (Institute for Biostatistics and Informatics in Medicine and Ageing Research)**, and the **Systems Biology of Aging Group**. Our goal is to make life easier for researchers by providing a suite of specialized, interoperable tools that seamlessly integrate into AI-driven IDEs (like Cursor, Windsurf), chat clients (like Anthropic's Claude Desktop), and serve as foundational building blocks for complex agentic workflows (using  ElizaOS, Just-Agents, AutoGen, etc.).

This project aggregates several powerful, standalone MCP servers into a single, cohesive ecosystem for advanced bioinformatics and longevity research.

## What is the Model Context Protocol (MCP)?

MCP is a protocol designed to bridge the gap between Large Language Models (LLMs) and specialized, domain-specific tools and databases. It provides a standardized way for AI assistants and agents to access complex functionalities through structured, type-safe interfaces.

If you want to understand MCP in more detail and learn how to use it effectively, we recommend these resources:

- **DeepLearning.AI Course**: [MCP: Build Rich-Context AI Apps](https://www.deeplearning.ai/short-courses/mcp-build-rich-context-ai-apps-with-anthropic/)
- **Official Documentation**: [Model Context Protocol Website](https://modelcontextprotocol.io)
- **Community**: Search for "Model Context Protocol" on YouTube and other platforms for tutorials and discussions.

## 🔬 Real-World Example in Action

Here's a real conversation (that you can easily reproduce yourself as all MCP-es are working and covered with tests) showing Holy Bio MCP servers working together to answer complex research questions, demonstrating the power of this integrated approach:

<div align="center">
  <img src="images/real_example_of_usage.jpg" alt="Real Example of Holy Bio MCP Usage"/>
</div>

---

## 🛠️ Included MCP Servers

This framework unites the following specialized MCP servers. Each is a powerful tool on its own, but together they form a comprehensive research platform.

- **[biothings-mcp](https://github.com/longevity-genie/biothings-mcp)**: Access to BioThings.io APIs for comprehensive gene, variant, chemical, and taxonomic data.
- **[gget-mcp](https://github.com/longevity-genie/gget-mcp)**: A powerful bioinformatics toolkit for genomics queries and analysis, wrapping the popular `gget` library.
- **[opengenes-mcp](https://github.com/longevity-genie/opengenes-mcp)**: A queryable database for aging and longevity research from the OpenGenes project.
- **[synergy-age-mcp](https://github.com/longevity-genie/synergy-age-mcp)**: A database of synergistic and antagonistic genetic interactions in longevity from SynergyAge.
- **[pharmacology-mcp](https://github.com/antonkulaga/pharmacology-mcp)**: Access to the Guide to PHARMACOLOGY database for drug, target, and ligand information.

---

## Server Capabilities & Example Questions

Instead of just listing functions, here's a look at the kind of research questions you can answer with each server.

### 1. 🧬 `biothings-mcp`

<div align="center"><img src="https://github.com/longevity-genie/biothings-mcp/raw/main/images/cursor_usage_example.jpg" alt="biothings-mcp usage example"/></div>

Wraps the BioThings.io APIs to provide foundational biological data.

**Example Research Questions:**
- "What are the functions and pathways associated with the human gene *BRAF*?"
- "Find all variants in the *EGFR* gene and provide their clinical significance from ClinVar."
- "What is the molecular formula and structure of the compound 'aspirin'?"
- "Download the protein FASTA sequence for UniProt ID P04637."
- "What is the taxonomic lineage for *Mus musculus*?"

### 2. 🔬 `gget-mcp`

<div align="center"><img src="https://github.com/longevity-genie/gget-mcp/raw/main/images/screenshot_example.png" alt="gget-mcp usage example"/></div>

Provides a rich set of tools for sequence analysis, functional genomics, and structural biology.

**Example Research Questions:**
- "Find information about the human *TP53* gene and get its protein sequence."
- "Perform enrichment analysis for a set of cancer-related genes: *TP53, BRCA1, BRCA2, ATM, CHEK2*."
- "Get the 3D structure information for the protein encoded by the *EGFR* gene from AlphaFold."
- "Find mutations in the COSMIC database for the *PIK3CA* gene."
- "Perform a BLAST search with the DNA sequence 'ATGGCGCCCGAACAGGGAC' to identify its origin."
- "Align multiple protein sequences to find conserved regions."

### 3. 🕰️ `opengenes-mcp`

<div align="center"><img src="https://github.com/longevity-genie/opengenes-mcp/raw/main/images/open-genes-usage-chat.png" alt="opengenes-mcp usage example"/></div>

A queryable SQL database focused on the genetics of aging and longevity.

**Example Research Questions:**
- "Which genetic interventions extended the lifespan of mice the most?"
- "What polymorphisms in *FOXO3* are associated with human longevity?"
- "Which hallmarks of aging are associated with the *KL* (Klotho) gene?"
- "Are there any liver-specific interventions that increase lifespan in mice?"
- "Find genes that are associated with both longevity in human studies and have lifespan-extending effects in model organisms."

### 4. 🔄 `synergy-age-mcp`

<div align="center"><img src="https://www.synergyage.info/static/curation/images/SynergyAgeFigs3.4.png" alt="synergy-age-mcp interaction types"/></div>

A specialized SQL database for synergistic, antagonistic, and additive genetic interactions in longevity.

**Example Research Questions:**
- "Which genetic interventions show the strongest synergistic effects in *C. elegans*?"
- "What is the relationship between *daf-2* and *daf-16* mutations in C. elegans longevity?"
- "How do insulin signaling pathway interventions compare between worms, flies, and mice?"
- "Which genetic combinations show antagonistic interactions that reduce lifespan benefits?"
- "How do caloric restriction mimetics interact with other longevity interventions?"

### 5. 💊 `pharmacology-mcp`

A comprehensive, queryable resource for pharmacological data.

**Example Research Questions:**
- "Find all approved drugs that target G-protein coupled receptors (GPCRs)."
- "What are the known ligands for the target 'epidermal growth factor receptor' (EGFR)?"
- "List all interactions for the ligand 'Imatinib' with their affinity data."
- "Which diseases are associated with the target 'Tumor necrosis factor' (TNF)?"
- "Search for all targets in the 'Voltage-gated ion channel' family."

## 🚀 Quick Start

### Prerequisites

Install `uv` (a modern Python package manager):

```bash
# Download and install uv
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Running Individual Servers

Each MCP server can be run independently using `uvx`, which will automatically handle installation.

```bash
# BioThings API access
uvx biothings-mcp

# Bioinformatics toolkit
uvx gget-mcp

# Aging research database  
uvx opengenes-mcp

# Synergistic interventions
uvx synergy-age-mcp

# Pharmacology database
uvx pharmacology-mcp
```

Each server can be run in different modes (`stdio`, `server`, `sse`) for compatibility with various MCP clients.

## 🔧 Configuring AI Clients

Simply point your MCP-compatible AI client to the appropriate configuration file from the respective server's repository (e.g., `mcp-config-stdio.json`).

For a visual guide on setting up clients like Cursor, watch our **[Configuration Tutorial Video](https://www.youtube.com/watch?v=Xo0sHWGJvE0)**. The principles shown apply to all servers in this framework.

## 🤖 Integration Scenarios

- **Interactive Research (Chat-based)**: Use with AI assistants like Claude for exploratory research.
- **AI-Enhanced Development (IDE Integration)**: Integrate with Cursor or Windsurf to access biomedical data and generate analysis scripts while coding.
- **Agentic Workflows (Automated Research)**: Build autonomous research agents using frameworks like AutoGen or ElizaOS.

## 🏗️ Development & Contributing

This project is open source and we welcome contributions. Whether it's bug reports, feature requests, documentation, or new tests, your input is valuable. Please see the individual repositories for specific contribution guidelines.

## 📄 License

This project is licensed under the MIT License. Individual data sources may have their own licensing terms.

## 🙏 Acknowledgments

This work would not be possible without the foundational work of the teams behind the databases and tools we've integrated. We are also grateful for the support of our collaborators and sponsors.

### Supported By

<div align="center">

[![HEALES](https://github.com/longevity-genie/biothings-mcp/raw/main/images/heales.jpg)](https://heales.org/)
*HEALES - Healthy Life Extension Society*

[![IBIMA](https://github.com/longevity-genie/biothings-mcp/raw/main/images/IBIMA.jpg)](https://ibima.med.uni-rostock.de/)
*IBIMA - Institute for Biostatistics and Informatics in Medicine and Ageing Research*

</div>

---

<div align="center">
  <strong>🧬 Accelerating biological discovery through AI-powered research tools 🚀</strong>
</div>