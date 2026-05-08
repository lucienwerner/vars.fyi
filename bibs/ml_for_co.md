# Machine Learning for Combinatorial Optimization

## TODO
- Figure out what problem classes the GNN methods are best suited for
- Get a handle on SOTA in the  B&C literature, both for MILP solvers and ML (see lit review in section 3.2 of Huang 2024)
- What is HiGHS doing that SCIP isn't?
- What is Nvidia CuOPT and why does it have so few citations? https://arxiv.org/pdf/2510.20499
- If you are solving a lot of similar scenarios with slight perturbations in params, how can solutions to successfully solved or "easy" instances be used to guide solutions to hard instances? Computational task re-stated to be "solve a total of K versions of the same problem (each problem has  perturbed params vs. base case)". Goal is to solve some parts of the problems in parallel and not necessarily each problem independently. Need K optimal solutions at the end. 

## Survey Papers
* [Bengio, Lodi, Prouvost (2018)](https://arxiv.org/abs/1811.06128). *Machine Learning for Combinatorial Optimization: a Methodological Tour d'Horizon*.
  Well-written problem setups. Frames ML-for-CO as learning decision policies inside B&C optimization pipline

* [Cappart, Chételat, Khalil, Lodi, Morris, Veličković (2021)](https://arxiv.org/abs/2102.09544). *Combinatorial Optimization and Reasoning with Graph Neural Networks*.
  GNNs review. Similar preliminaries style as Bengio et al. From the Montreal group

* [Zhang et al. (2023)](https://www.sciencedirect.com/science/article/abs/pii/S0925231222014035). *A survey for solving mixed integer programming via machine learning*.
  Origin of a extensive, maintained bibliography: https://github.com/Thinklab-SJTU/awesome-ml4co

* [Scavuzzo, Aardal, Lodi, Yorke-Smith (2024)](https://arxiv.org/pdf/2402.05501). *Machine Learning Augmented Branch and Bound for Mixed Integer Linear Programming* 
  Very good, recent review of learning for Branch and Bound. Also includes discussion of cut plane selection 

## Papers I Have "Read"
* [Tang, Khalil, Drgoňa (2024)](https://arxiv.org/abs/2410.11061v1). *Learning to Optimize for Mixed-Integer Non-linear Programming*.
  (Nico recommended) Differentiable layers for integrality. Barrier functions for feasibility. Results for MILPs are only in Appendix D and look kind of weak. Good setup of various approaches to integrality in NNs

* [Huang, Ferber, Zharmagambetov, Tian, Dilkina (2024)](https://proceedings.mlr.press/v235/huang24f.html). *Contrastive Predict-and-Search for Mixed Integer Linear Programs*.
  (Nico recommended) Generate training examples that have both positive (feasible/optimal) and negative (infeasible/suboptimal). Train NN to discriminate. Not clear to me how large problem sizes are (at least several thousand vars). Seems to outperform SCIP but this is no longer SOTA. What's nice about this approach is the training data is very naturally generated. Positive examples are cases solved to opitmality using MILP solvers. Negative examples can be geenrated by stopping early, etc. This is easier that Learning to Cut's approach which requires saving solved sub-problems within the B&C procedure. 

* [Paulus, et al. (2022)](https://arxiv.org/pdf/2203.02878). *Learning to Cut by Looking Ahead:
Cutting Plane Selection via Imitation Learning*.
  Learn cutting plane selection heuristic. This style of algo feels like the right approach: why reinvent B&C when whats needed are better heruistics to guide tree search and/or set selection problems? Need to look into learning to branch papers (some cited in Section 3.1). Collecting data to train the lookahead heuristic seems challenging. Maybe there are easy ways to do this? Would be ideal to just train on successfully solved problems...

* [Deza, Khalil (2023)](https://arxiv.org/pdf/2302.09166). *Machine Learning for Cutting Planes in Integer Programming: A Survey*.
  Helpful presentation of cut selection metrics 

* [Huang et al. (2021)](https://arxiv.org/pdf/2111.06257). *A Branch and Bound in Mixed Integer Linear Programming Problems: A Survey of Techniques and Trends*.
  Another B&B survey. Older than Scavuzzo et al. (2024)
  
* [Khalil, Bodic, Song, Nemhauser, Dilkina (2016)](https://arxiv.org/pdf/2402.05501). *Learning to Branch in Mixed Integer Programming*.
  Learns branching policies inside B&B


## Papers I Haven't Read
NB: used GPT to help format these refs. Titles and hyperlinks matching could be sus...

* [Achterberg, Wundering (2013)](https://link.springer.com/chapter/10.1007/978-3-642-38189-8_18). *Mixed Integer Programming: Analyzing 12 Years of Progress*
  Classical methods for MILP
* [Jin, Yan, Liu, Wang (2024)](https://arxiv.org/abs/2406.13125). *A Unified Framework for Combinatorial Optimization Based on Graph Neural Networks*.

* [Liu, Zhou, Zhang, Pan, Li, Chen (2024)](https://arxiv.org/abs/2406.03647). *Decision-focused Graph Neural Networks for Combinatorial Optimization*.

* [Heydaribeni, Zhan, Zhang, Eliassi-Rad, Koushanfar (2024)](https://www.nature.com/articles/s42256-024-00833-7). *Distributed Constrained Combinatorial Optimization Leveraging Hypergraph Neural Networks*.

* [Prouvost, Dumouchelle, Zarpellon, et al. (2020)](https://arxiv.org/abs/2008.07094). *Ecole: A Library for Learning Inside MILP Solvers*.

* [Khalil, Morris, et al. (2020)](https://arxiv.org/abs/1911.07953). *Neural Diving*.

* [Gasse, Chételat, Ferroni, Charlin, Lodi (2019)](https://arxiv.org/abs/1906.01629). *MIP-GNN: A Data-Driven Framework for Guiding Combinatorial Optimization Solvers*.

* [Nazari, Oroojlooy, Snyder, Takáč (2018)](https://arxiv.org/abs/1802.04240). *Deep Reinforcement Learning for Solving the Vehicle Routing Problem*.

* [Vinyals, Fortunato, Jaitly (2015)](https://arxiv.org/abs/1506.03134). *Pointer Networks*.
  
* [Kool, van Hoof, Welling (2018)](https://arxiv.org/abs/1803.08475). *Attention, Learn to Solve Routing Problems!*.

* [Baptista, Poloczek (2018)](https://link.springer.com/content/pdf/10.1007/s10107-024-02130-y.pdf). *Bayesian Optimization of Combinatorial Structures*.

* [Bello, Pham, Le, Norouzi, Bengio (2016)](https://arxiv.org/abs/1611.09940). *Neural Combinatorial Optimization with Reinforcement Learning*.

## Recent Papers (2024–2025)

* [Feng, Sun, Li, Talwalkar, Yang (2025)](https://arxiv.org/abs/2505.16952). *A Comprehensive Evaluation of Contemporary ML-Based Solvers for Combinatorial Optimization*.

* [Deza, Khalil, Fan, Zhou, et al. (2025)](https://arxiv.org/abs/2409.06559). *Learn2Aggregate: Supervised Generation of Chvátal-Gomory Cuts Using Graph Neural Networks*.

* [Cantürk, Varol, Aydoğan, Özener (2025)](https://www.ijcai.org/proceedings/2025/1223). *Scalable Primal Heuristics Using Graph Neural Networks for Combinatorial Optimization*.

* [Zhhang, Zhang, Sun, Li, Gao (2025)](https://www.sciencedirect.com/science/article/abs/pii/S0893608025006641). *HTS-LB: Hypergraph Tree Search for Learning Branch*.

* [Wang et al. (2024)](https://arxiv.org/pdf/2404.12638). *Learning to Cut via Hierarchical Sequence/Set Model for Efficient Mixed-Integer Programming*

## Solvers 
* COPT (https://www.copt.de/). This is a chinese solver with 180 day commercial trial: https://www.shanshu.ai/copt
  - Docs: https://guide.coap.online/copt/en-doc/intro.html
  - User guide: https://arxiv.org/pdf/2208.14314
  - Commentary: https://github.com/ERGO-Code/HiGHS/discussions/1683
* HiGHS (https://highs.dev/#background)
  - Critique of implementation: https://github.com/ERGO-Code/HiGHS/discussions/1683
* SimpleRose (https://simplerose.com/blog/running-cuopt-in-an-aws-eks-cluster-as-a-managed-node-group/)
* Nvidia CuOPT (https://github.com/NVIDIA/cuopt)

## Other
Extensive bibliography with papers categorized by problem instance. Looks maintained too: https://github.com/Thinklab-SJTU/awesome-ml4co

