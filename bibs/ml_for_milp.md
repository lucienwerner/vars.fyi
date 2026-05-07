# Machine Learning for Combinatorial Optimization 

## Survey Papers

* [Cappart, Chételat, Khalil, Lodi, Morris, Veličković (2021)]. *Combinatorial Optimization and Reasoning with Graph Neural Networks*.(https://arxiv.org/abs/2102.09544)
  Reviews how GNNs encode combinatorial structure for exact solving, heuristics, and reasoning tasks.

* [Bengio, Lodi, Prouvost (2018)]. *Machine Learning for Combinatorial Optimization: a Methodological Tour d'Horizon*.(https://arxiv.org/abs/1811.06128)
  Broad survey framing ML-for-CO as learning decision policies inside classical optimization pipelines.

## Papers I read

* [Huang, Silva, Zhao, et al. (2024)]. *Learning to Solve Combinatorial Optimization Problems on Real-World Graphs in Linear Time*.(https://proceedings.mlr.press/v235/huang24f.html)
  Uses scalable graph learning methods to generalize CO solvers to large real-world graphs with near-linear inference cost.

* [Paulus, et al. (2022)]. *Learning to Cut*.(https://arxiv.org/pdf/2203.02878)
  Uses ML to generate stronger cutting planes in integer programming.

* [Eskandari, et al. (2022)]. *Exact Combinatorial Optimization with Graph Convolutional Neural Networks*.(https://arxiv.org/pdf/2302.09166)
  Combines GNN guidance with exact optimization to improve search efficiency while preserving optimality.

* [Wang, Hua, Liu, et al. (2021)]. *A Bi-Level Framework for Learning to Solve Combinatorial Optimization on Graphs*.(https://arxiv.org/pdf/2111.06257)
  Learns graph transformations that simplify downstream combinatorial optimization.

* [Khalil, Dai, Zhang, Dilkina, Song (2019)]. *Learning to Branch*.(https://arxiv.org/pdf/2402.05501)
  Learns branching policies inside branch-and-bound to accelerate MILP solving.

* [Kool, van Hoof, Welling (2018)]. *Attention, Learn to Solve Routing Problems!*.(https://arxiv.org/abs/1803.08475)
  Replaced RNNs with attention models for stronger neural routing heuristics.

* [Baptista, Poloczek (2018)]. *Bayesian Optimization of Combinatorial Structures*.(https://link.springer.com/content/pdf/10.1007/s10107-024-02130-y.pdf)
  Extends Bayesian optimization to large discrete combinatorial spaces using structured acquisition methods.

* [Bello, Pham, Le, Norouzi, Bengio (2016)]. *Neural Combinatorial Optimization with Reinforcement Learning*.(https://arxiv.org/abs/1611.09940)
  Introduced pointer-network RL methods for routing problems such as TSP.

## Papers I haven't read

* [Jin, Yan, Liu, Wang (2024). *A Unified Framework for Combinatorial Optimization Based on Graph Neural Networks*.](https://arxiv.org/abs/2406.13125)
  Attempts a general-purpose GNN framework spanning multiple combinatorial optimization classes.

* [Liu, Zhou, Zhang, Pan, Li, Chen (2024). *Decision-focused Graph Neural Networks for Combinatorial Optimization*.](https://arxiv.org/abs/2406.03647)
  Integrates differentiable optimization objectives directly into GNN training.

* [Heydaribeni, Zhan, Zhang, Eliassi-Rad, Koushanfar (2024). *Distributed Constrained Combinatorial Optimization Leveraging Hypergraph Neural Networks*.](https://www.nature.com/articles/s42256-024-00833-7)
  Uses hypergraph neural networks and distributed training for higher-order constrained optimization problems.

* [Prouvost, Dumouchelle, Zarpellon, et al. (2020). *Ecole: A Library for Learning Inside MILP Solvers*.](https://arxiv.org/abs/2008.07094)
  Standardized benchmark and RL environment for learning branching, cuts, and node selection.

* [Khalil, Morris, et al. (2020). *Neural Diving*.](https://arxiv.org/abs/1911.07953)
  Learns primal heuristics for finding feasible integer solutions quickly.

* [Gasse, Chételat, Ferroni, Charlin, Lodi (2019). *MIP-GNN: A Data-Driven Framework for Guiding Combinatorial Optimization Solvers*.](https://arxiv.org/abs/1906.01629)
  Landmark GNN framework for branching decisions in mixed-integer programming.

* [Nazari, Oroojlooy, Snyder, Takáč (2018). *Deep Reinforcement Learning for Solving the Vehicle Routing Problem*.](https://arxiv.org/abs/1802.04240)
  Early scalable RL framework for capacitated VRP.

* [Vinyals, Fortunato, Jaitly (2015). *Pointer Networks*.](https://arxiv.org/abs/1506.03134)
  Introduced pointer architectures that enabled neural sequence-based combinatorial optimization.

## Recent Papers (2024–2025)

* [Feng, Sun, Li, Talwalkar, Yang (2025). *A Comprehensive Evaluation of Contemporary ML-Based Solvers for Combinatorial Optimization*.](https://arxiv.org/abs/2505.16952)
  Important benchmark paper evaluating whether modern ML-for-CO methods actually scale to industrial instances. ([huggingface.co](https://huggingface.co/papers/2505.16952?utm_source=chatgpt.com))

* [Deza, Khalil, Fan, Zhou, et al. (2025). *Learn2Aggregate: Supervised Generation of Chvátal-Gomory Cuts Using Graph Neural Networks*.](https://arxiv.org/abs/2409.06559)
  Strong recent work on learning cut generation rather than only branching policies. ([researchgate.net](https://www.researchgate.net/publication/390720901_Learn2Aggregate_Supervised_Generation_of_Chvatal-Gomory_Cuts_Using_Graph_Neural_Networks?utm_source=chatgpt.com))

* [Cantürk, Varol, Aydoğan, Özener (2025). *Scalable Primal Heuristics Using Graph Neural Networks for Combinatorial Optimization*.](https://www.ijcai.org/proceedings/2025/1223)
  Focuses on scalable GNN-based primal heuristics for large constrained optimization problems. ([ijcai.org](https://www.ijcai.org/proceedings/2025/1223?utm_source=chatgpt.com))

* [HTS-LB authors (2025). *HTS-LB: Hypergraph Tree Search for Learning Branch*.](https://www.sciencedirect.com/science/article/abs/pii/S0893608025006641)
  Uses hypergraph representations plus tree search to improve MILP branching quality and scalability. ([sciencedirect.com](https://www.sciencedirect.com/science/article/abs/pii/S0893608025006641?utm_source=chatgpt.com))
