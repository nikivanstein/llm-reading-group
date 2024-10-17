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
  - [Buffer of Thoughts](#buffer-of-thoughts)
    - [Summary of the Paper](#summary-of-the-paper-2)
    - [Discussion Summary](#discussion-summary-2)
  - [Evolutionary Search with LLMs](#evolutionary-search-with-llms)
    - [Summary of the Paper](#summary-of-the-paper-3)
    - [Discussion Summary](#discussion-summary-3)
  - [Intelligence at the Edge of Chaos](#intelligence-at-the-edge-of-chaos)
    - [Summary of the Paper](#summary-of-the-paper-4)
    - [Discussion Summary](#discussion-summary-4)

## Papers Discussed

| Date       | Paper Title                          | Summary                                                                                                                         | Code                                    | Paper               |
|------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|---------------------|
| 04-07-2024 | Tree of Thoughts                     | A novel framework enhancing LLMs' problem-solving abilities by using a tree-based reasoning structure.                          | [Github](https://github.com/princeton-nlp/tree-of-thought-llm)    | [arXiv](https://arxiv.org/abs/2305.10601) |
| 15-08-2024 | Graph of Thoughts                    | Introduces a graph-based reasoning process for LLMs, allowing more complex problem-solving than tree or chain-based approaches. | [Github](https://github.com/spcl/graph-of-thoughts) | [arXiv](https://arxiv.org/abs/2308.09687) |
| 12-09-2024 | Buffer of Thoughts                   | Introduces the BoT framework, enhancing LLM reasoning with high-level thought templates to improve accuracy, efficiency, and robustness. | [Github](https://github.com/YangLing0818/buffer-of-thought-llm) | [arXiv](https://arxiv.org/abs/2406.04271) |
| 26-09-2024 | [Understanding the Importance of Evolutionary Search in Automated Heuristic Design with Large Language Models](https://arxiv.org/abs/2407.10873v1) | Explores the integration of LLMs with EPS for AHD, highlighting the importance of evolutionary search. | x | [arXiv](https://arxiv.org/pdf/2407.10873) |
| 2024-10-XX | [Intelligence at the Edge of Chaos](https://arxiv.org/abs/2410.02536v2)         | Investigates the relationship between system complexity and emergent intelligence in LLMs. | x | [arXiv](https://arxiv.org/abs/2410.02536v2) |



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

### Buffer of Thoughts

**Paper Title:** Buffer of Thoughts: Thought-Augmented Reasoning with Large Language Models

**Discussion Date:** 12-09-2024

#### Summary of the Paper

The paper *Buffer of Thoughts: Thought-Augmented Reasoning with Large Language Models* by Yang et al. (2024) introduces the Buffer of Thoughts (BoT) framework. This framework enhances reasoning in large language models by utilizing a "meta-buffer" of high-level thought templates distilled from past tasks, allowing the model to adapt and generalize across new problems. The framework also includes a buffer-manager, which dynamically updates the meta-buffer as new tasks are solved. BoT shows significant improvements in reasoning accuracy and efficiency across various benchmarks, reducing computational costs and requiring fewer queries than traditional multi-query reasoning methods.


#### Discussion Summary
During this week’s LLM Reading Group, the discussion centered on the paper *Buffer of Thoughts: Thought-Augmented Reasoning with Large Language Models* by Yang et al. (2024)[arXiv](https://arxiv.org/abs/2406.04271). The paper introduces a novel framework, Buffer of Thoughts (BoT), designed to enhance the accuracy, efficiency, and robustness of reasoning in large language models (LLMs).

The group engaged in a detailed analysis of the BoT framework, focusing on its core components: the meta-buffer and buffer-manager. The meta-buffer stores high-level thought templates distilled from previous tasks, while the buffer-manager dynamically updates these templates, allowing the model to generalize across different tasks. The discussion emphasized the framework's potential to outperform state-of-the-art methods in complex reasoning tasks while reducing computational overhead.

Participants raised questions about the mechanics of the embedding vectors used for calculating simmilarity of stored thought-templates and updating the buffer. Specifically, there was some debate regarding the precise embedding methods and thresholds employed for retrieving relevant templates, as the threshold is not specified in the paper and embeddings from close-source models such as GPT-4 are generally unavailable. Additionally, the group discussed the scalability of the BoT approach and its potential for broader application beyond the reasoning tasks presented in the paper, particularly in areas like reinforcement learning and optimization.

The general sentiment was that, although the framework shows promise, its practical implementation may need refinement, particularly concerning the clarity of its explanation and the need to address several typographical errors in the draft. There was curiosity about whether the BoT approach would be published in its current form or if it would undergo further revisions. Participants also acknowledged that even if the ideas in the paper are not fully developed yet, they could inspire future improvements in reasoning techniques for LLMs.

To conclude, the group discussed potential papers for the next meeting, with a focus on continuing the theme of optimization and heuristic search in LLM contexts.

Overall, the discussion was a blend of technical exploration, skepticism, and curiosity about the future potential of LLMs in solving complex problems, balanced with practical considerations in research and collaboration.

**Key Points:**

1. **Embedding Vector Clarification**: Participants were curious about the specific mechanics of the embedding vectors used in BoT, including the threshold for updateing thought-templates.
   
2. **Scalability and Applications**: The group discussed the scalability of the BoT approach and its potential to be applied in areas beyond the paper's scope, such as reinforcement learning and optimization.

3. **Clarity and Typographical Issues**: Most members found the paper's explanations unclear, and there were concerns about the numerous typographical errors. These should be addressed before the work is published.

4. **Future Impact**: Despite these issues, there was consensus that the BoT framework introduces promising ideas that could inspire further advancements in reasoning techniques for LLMs.

### Evolutionary Search with LLMs

**Paper Title:** Understanding the Importance of Evolutionary Search in Automated Heuristic Design with Large Language Models  
**Authors**: Rui Zhang, Fei Liu, Xi Lin, Zhenkun Wang, Zhichao Lu, Qingfu Zhang  
**Link**: [arXiv](https://arxiv.org/abs/2407.10873v1)  
**Discussion Date:** 12-09-2024  

#### Summary of the Paper

This paper investigates the role of evolutionary search in LLM-based Automated Heuristic Design (AHD), demonstrating that LLMs alone are not sufficient to optimize heuristics. The authors benchmark multiple methods across nine LLMs, providing empirical evidence that the integration of LLMs and EPS outperforms standalone LLMs.

<details>
<summary> Main Contributions </summary>  
  
  1. Large-scale benchmark for LLM-based EPS methods.
  2. Proposal of a new (1+1)-EPS baseline.
  3. Empirical demonstration of the necessity of evolutionary search in LLM-based AHD.
  4. Open-sourcing of all methods and results for reproducibility.

</details>

#### Discussion Summary
In our discussion on **"Understanding the Importance of Evolutionary Search in Automated Heuristic Design with Large Language Models"**, we focused on the interplay between LLMs and evolutionary search in automated algorithm design. The conversation brought out several insights regarding the strengths and limitations of different models and the overall experimental design of the paper. There was also discussion around the role of LLMs in programming, their performance issues, and ways to optimize their utility.

**Key Points:**

1. **LLMs as a Functional Programming Tool**:  
   - It was noted that LLMs could be seen as Turing machines, with prompts acting as function calls in a stateless, functional programming style. This structure leads to the need for chaining prompts to maintain state throughout the evolutionary process.

2. **Discussion on Results Visualization**:  
   - Some members raised concerns about Figure 5 in the paper, noting that the visualization (particularly the size of circles representing performance) was unconventional, which could lead to misinterpretation.

3. **Performance of Models**:  
   - The group discussed the performance of different methods, specifically noting that GPT-3.5 underperformed, while the (1+1)-EPS method showed inconsistent results, possibly due to a limited number of runs. The group suggested that more runs might have yielded better insights.

4. **Challenges with LLM-Generated Code**:  
   - A significant portion of the discussion revolved around the fact that LLMs, particularly GPT-4 and GPT-3.5, often generate code that is not runnable. Approximately 18% of the code from GPT-3.5 was reported as non-runnable, compared to about 10% for GPT-4, highlighting a notable issue with LLM reliability in generating executable code.

5. **Insert Domain Knowledge**:  
   - One promising aspect discussed was the ease of injecting domain knowledge into LLMs, which can potentially lead to improvements in state-of-the-art solutions for certain tasks.

6. **Importance of Larger Benchmarking**:  
   - The limited number of runs in the paper’s experiments was seen as a drawback. The group emphasized the importance of performing additional runs, despite the high computational cost, to avoid the variability seen in some of the results.

7. **Coding Language and LLMs**:  
   - The team touched on how LLM performance might vary depending on the programming language generated (e.g., Python vs. Rust), hinting at future directions for testing across multiple coding languages.


### Intelligence at the Edge of Chaos

**Authors**: Shiyang Zhang, Aakash Patel, Syed A Rizvi, Nianchen Liu, Sizhuang He, Amin Karbasi, Emanuele Zappala, David van Dijk  
**Link**: [arXiv](https://arxiv.org/abs/2410.02536v2)  
**Discussion Date:** 10-10-2024  

#### Summary of the Paper

This paper explores the emergence of intelligence in large language models (LLMs) by training them on elementary cellular automata (ECA) data. It demonstrates that models trained on systems with intermediate complexity ("edge of chaos") perform best in reasoning and prediction tasks, highlighting the importance of system complexity in fostering intelligence.

<details>
<summary> Main Contributions </summary>  
  
  1. Establishes a correlation between ECA complexity and LLM intelligence.
  2. Identifies a range of complexity levels for emergent intelligence.
  3. Shows better downstream performance for models trained on complex but not chaotic rules.
  4. Provides insights into attention mechanisms and non-trivial solutions learned by the models.

</details>

#### Discussion Summary

In this session, the group discussed the paper "Intelligence at the Edge of Chaos" and critically reflected on the experimental design and conclusions drawn by the authors. While the group found the core idea of emergent intelligence intriguing, they expressed concerns about the boldness of the claims and the lack of clear correlation between the complexity of the system and the performance improvements in downstream tasks. The group also debated the computational complexity required for the experiments and suggested exploring how simpler, dense neural networks would behave when trained on cellular automata (CAs).

**Key Points**:  

  1. The paper discusses how intelligence emerges in LLMs trained on systems at the "edge of chaos," but the group criticized the bold conclusions, which were not clearly backed by the data.
  2. There was a lack of a proper baseline in the experiments, making it difficult to evaluate the claimed benefits.
  3. The correlations between complexity and downstream task performance were unclear and not well-demonstrated in the results.
  4. The group suggested exploring how smaller, dense neural networks would behave when trained on CAs and how the weights would look after training.
  5. One member proposed that the CA training may have influenced the initial diversity in the weight space, leading to different performance outcomes on downstream tasks.
  6. The Eureka paper by NVIDIA, focused on reward design for robotics using LLMs, was discussed as a similar work.
