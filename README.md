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

<a href="README_EN.md"><img src="https://img.shields.io/badge/english-document-white.svg" alt="EN doc"></a>
<a href="README.md"><img src="https://img.shields.io/badge/ドキュメント-日本語-white.svg" alt="JA doc"></a>

</h2>

</p>

これは、**GNN-RAG: Graph Neural Retrieval for Large Language Modeling Reasoning**のためのコードです。

![alt GNN-RAG: GNNは密なサブグラフ上で推論を行い、候補答えと対応する推論パス（質問エンティティから答えへの最短パス）を検索します。検索された推論パスは、オプションで検索拡張（RA）と組み合わせて、言語化されてLLMに与えられ、RAGが行われます。](GNN-RAG.png "GNN-RAG")

ディレクトリ構成は以下の通りです：

|----`gnn`フォルダには、さまざまなKGQA GNNの実装が含まれています。

独自のGNNをトレーニングすることも、このフォルダをスキップして、計算済みのGNN出力（検索された答えノード）を直接使用することもできます（`llm/results/gnn`）。

|----`llm`フォルダには、LLMを使用したRAGベースのKGQAの実装が含まれています。

結果を再現する方法の詳細については、そちらを参照してください。

**結果**：表2のすべての結果を追加しました：`results/KGQA-GNN-RAG-RA`または`results/KGQA-GNN-RAG`を参照してください。実際のLLM生成と、検索されたKG情報（"input"キー）をpredictions.jsonlで見ることができます。