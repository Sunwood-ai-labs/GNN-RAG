<p align="center">
<img src="https://huggingface.co/datasets/MakiAi/IconAssets/resolve/main/gnnrag2.jpeg" width="100%">
<br>
<h1 align="center">GNN-RAG</h1>
<h2 align="center">
  ～ Graph Neural Retrieval for Large Language Modeling Reasoning ～
<br>

<a href="https://github.com/Sunwood-ai-labs/GNN-RAG" title="Go to GitHub repo"><img src="https://img.shields.io/static/v1?label=GNN-RAG&message=Sunwood-ai-labs&color=blue&logo=github"></a>
<img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/Sunwood-ai-labs/GNN-RAG">
<a href="https://github.com/Sunwood-ai-labs/GNN-RAG"><img alt="forks - Sunwood-ai-labs" src="https://img.shields.io/github/forks/GNN-RAG/Sunwood-ai-labs?style=social"></a>
<a href="https://github.com/Sunwood-ai-labs/GNN-RAG"><img alt="GitHub Last Commit" src="https://img.shields.io/github/last-commit/Sunwood-ai-labs/GNN-RAG"></a>
<a href="https://github.com/Sunwood-ai-labs/GNN-RAG"><img alt="GitHub Top Language" src="https://img.shields.io/github/languages/top/Sunwood-ai-labs/GNN-RAG"></a>
<img alt="GitHub Release" src="https://img.shields.io/github/v/release/Sunwood-ai-labs/GNN-RAG?color=red">
<img alt="GitHub Tag" src="https://img.shields.io/github/v/tag/Sunwood-ai-labs/GNN-RAG?sort=semver&color=orange">
<img alt="GitHub Actions Workflow Status" src="https://img.shields.io/github/actions/workflow/status/Sunwood-ai-labs/GNN-RAG/publish-to-pypi.yml">
<br>

<a href="README.md"><img src="https://img.shields.io/badge/english-document-white.svg" alt="EN doc"></a>
<a href="README_JA.md"><img src="https://img.shields.io/badge/ドキュメント-日本語-white.svg" alt="JA doc"></a>

</h2>

</p>

This is the code for **GNN-RAG: Graph Neural Retrieval for Large Language Modeling Reasoning**.


![alt GNN-RAG: The GNN reasons over a dense subgraph to retrieve candidate answers, along
with the corresponding reasoning paths (shortest paths from question entities to answers). The
retrieved reasoning paths -optionally combined with retrieval augmentation (RA)- are verbalized
and given to the LLM for RAG](GNN-RAG.png "GNN-RAG")

The directory is the following:

|----`gnn` folder has the implementation of different KGQA GNNs. 

You can train your own GNNs or you can skip this folder and  use directly the GNN output (retrieved answer nodes) that we computed (`llm/results/gnn`).

|----`llm` folder has the implementation for RAG-based KGQA with LLMs. 

Please see details on how to reproduce results there. 

**Results**: We append all the results for Table 2: See `results/KGQA-GNN-RAG-RA` or `results/KGQA-GNN-RAG`. You can look at the actual LLM generations, as well as the KG information retrieved ("input" key) in predictions.jsonl.
