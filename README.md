# LLM Reading Group Discussions

This repository contains summaries and discussions of papers reviewed by our reading group at [LIACS](https://liacs.leidenuniv.nl/). Below is a table with brief information about the papers discussed, followed by more detailed summaries of the papers and discussions.
The meetings are chaired by [dr. Niki van Stein](https://nikivanstein.nl)

## Table of Contents

- [Papers Discussed](#papers-discussed)
- [Detailed Summaries and Discussions](#detailed-summaries-and-discussions)
  - [Tree of Thoughts](#tree-of-thoughts)
    - [Summary of the Paper](#summary-of-the-paper)
    - [Discussion Summary](#discussion-summary)
  - [Graph of Thoughts](#graph-of-thoughts)
    - [Summary of the Paper](#summary-of-the-paper-1)
    - [Discussion Summary](#discussion-summary-1)

## Papers Discussed

| Date       | Paper Title                          | Summary                                                                                                                         | Code                                    | Paper               |
|------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|---------------------|
| 04-07-2024 | Tree of Thoughts                     | A novel framework enhancing LLMs' problem-solving abilities by using a tree-based reasoning structure.                          | [Github](https://github.com/princeton-nlp/tree-of-thought-llm)    | [arXiv](https://arxiv.org/abs/2305.10601) |
| 15-08-2024 | Graph of Thoughts                    | Introduces a graph-based reasoning process for LLMs, allowing more complex problem-solving than tree or chain-based approaches. | [Github](https://github.com/spcl/graph-of-thoughts) | [arXiv](https://arxiv.org/abs/2308.09687) |

## Detailed Summaries and Discussions

### Tree of Thoughts

**Paper Title:** Tree of Thoughts: Deliberate Problem Solving with Large Language Models

**Discussion Date:** 04-07-2024

#### Summary of the Paper
The paper titled *Tree of Thoughts: Deliberate Problem Solving with Large Language Models* introduces a novel framework called Tree of Thoughts (ToT) aimed at enhancing the problem-solving capabilities of large language models (LLMs). The main idea behind ToT is to generalize the existing Chain of Thought (CoT) approach, allowing LLMs to explore multiple reasoning paths and make deliberate decisions, which is more reflective of how humans solve complex problems.

<details>
<summary> Main Contributions </summary>    

- **Tree-Based Reasoning Framework:** The paper proposes a shift from linear reasoning models to a tree-based structure, where each "thought" or intermediate step in problem-solving can branch out, allowing the model to explore multiple possible solutions before deciding on the best course of action.
- **Enhanced Problem-Solving Abilities:** By framing problem-solving as a search through a tree of possible thoughts, ToT allows for better exploration and backtracking, making it particularly effective in tasks that require planning, strategic lookahead, and exploration.
- **Flexibility and Adaptability:** ToT is designed to be a flexible and general framework. It supports different ways to decompose problems into thought steps, various strategies for generating and evaluating thoughts, and the use of different search algorithms, such as breadth-first search (BFS) and depth-first search (DFS).
- **Empirical Validation:** The paper provides empirical evidence of the effectiveness of ToT, demonstrating substantial improvements over traditional CoT methods.
- **Modularity and Ease of Use:** ToT is modular, meaning that different components such as the thought generator, state evaluator, and search algorithm can be independently adjusted or replaced.

</details>

#### Discussion Summary
In the meeting, the group discussed their general impressions of the "Tree of Thoughts" (ToT) paper, noting its innovative combination of traditional AI methods with modern approaches.

**Key Points:**
- **General Impressions:**
  - Appreciation for the paper's reference to older AI methods and its hybrid algorithm approach, contrasting it with CoT prompting.
  - Some concerns were raised about its effectiveness in higher-dimensional tasks and its cost efficiency, although the use of human evaluations in creative writing was well-received.
  - The idea of using ToT to improve existing algorithms like LLaMEA was discussed, though it was noted that the improvements were not consistent across different tasks.

- **Challenges and Questions:**
  - The need for domain knowledge to generalize the method effectively was highlighted, with questions raised about its application to more complex problems like the Traveling Salesman Problem (TSP).
  - Skepticism was expressed about whether ToT truly represented "reasoning" by the LLM or if it was more akin to a backtracking algorithm layered on top of an LLM.

Overall, the paper was positively received, but the group highlighted the need for further exploration into its generalizability and the true nature of its reasoning capabilities.

### Graph of Thoughts

**Paper Title:** Graph of Thoughts: Solving Elaborate Problems with Large Language Models

**Discussion Date:** 15-08-2024

#### Summary of the Paper
The paper titled *Graph of Thoughts: Solving Elaborate Problems with Large Language Models* introduces a new framework called Graph of Thoughts (GoT) for enhancing the problem-solving capabilities of large language models (LLMs). The key innovation in this framework is the ability to model the reasoning process of LLMs as an arbitrary graph structure, rather than the more traditional linear (Chain of Thought) or tree-based (Tree of Thought) approaches.

<details>
<summary> Main Contributions </summary>  
  
- **Graph-Based Reasoning:** GoT allows LLMs to represent information and reasoning as a graph, where each thought is a vertex, and edges represent dependencies between these thoughts. This enables the combination of different reasoning paths and the refinement of thoughts, offering a more flexible and powerful reasoning process.
- **Improved Task Performance:** The framework shows improvements in task performance over previous state-of-the-art approaches, such as a 62% improvement in sorting tasks compared to Tree of Thoughts while reducing costs by more than 31%.
- **Modular and Extensible Architecture:** GoT is designed with a modular architecture that allows for the integration of new thought transformations and reasoning patterns, making it easier to experiment with different LLMs and extend the framework with novel ideas.
- **Use Cases and Evaluation:** The paper provides several examples of how GoT can be applied, including tasks like sorting, keyword counting, set operations, and document merging.

</details>

#### Discussion Summary
The discussion revolves around challenges and strategies related to improving algorithms, particularly in the context of large language models (LLMs) and their application to mathematical and computational problems.

**Key Points:**
- **Local Optima and Parallel Thinking:** Concerns were raised about LLMs getting stuck in local optima, with a suggestion to use parallel chains of thought for recombination and interaction of different solutions.
- **Complexity and Practicality:** There was debate over the complexity of certain approaches, particularly when dealing with benchmarks and the need for manual intervention in defining tasks.
- **Interpretability and Utility:** The group discussed the difficulty of interpreting more complex models compared to simpler approaches and questioned the necessity of advanced methods for less complex problems.
- **Application Areas:** Considerations were made about which domains or tasks these advanced methods might be more applicable to, especially tasks that are not well-defined mathematically but require nuanced understanding.
- **Skepticism and Realism:** Some skepticism was expressed about the actual novelty and utility of these methods, with concerns that existing solutions in traditional computer science might already address the problems being targeted.
- **Future Directions:** Participants were curious about the potential of training models on multimodal data to simulate human-like thinking more effectively, and the possibility of LLMs combining information from different domains to produce new insights was discussed.

Overall, the discussion was a blend of technical exploration, skepticism, and curiosity about the future potential of LLMs in solving complex problems, balanced with practical considerations in research and collaboration.
