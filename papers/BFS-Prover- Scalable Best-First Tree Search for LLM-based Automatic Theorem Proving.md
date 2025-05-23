BFS-Prover: Scalable Best-First Tree Search for LLM-based Automatic Theorem Proving

## Abstract

Recent advancements in large language models (LLMs) have spurred growing interest in automatic
theorem proving using Lean4, where effective tree search methods are crucial for navigating the underlying large proof search spaces. While the existing approaches primarily rely on value functions and/or
Monte Carlo Tree Search (MCTS), the potential of simpler methods like Best-First Tree Search (BFS)
remains underexplored. In this paper, we investigate whether BFS can achieve competitive performance
in large-scale theorem proving tasks. We present BFS-Prover, a scalable expert iteration framework, featuring three key innovations. First, we implement strategic data filtering at each expert iteration round,
excluding problems solvable via beam search node expansion to focus on harder cases. Second, we improve the sample efficiency of BFS through Direct Preference Optimization (DPO) applied to state-tactic
pairs automatically annotated with compiler error feedback, refining the LLM’s policy to prioritize productive expansions. Third, we employ length normalization in BFS to encourage exploration of deeper
proof paths. BFS-Prover achieves a state-of-the-art score of 72.95% on the MiniF2F test set and therefore
challenges the perceived necessity of complex tree search methods, demonstrating that BFS can achieve
competitive performance when properly scaled. To facilitate further research and development in this
area, we have open-sourced our model at https://huggingface.co/bytedance-research/BFS-Prover.

