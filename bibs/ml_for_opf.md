# Machine Learning for OPF

## Datasets / Benchmarks

* [Lovett, Zgubic, Liguori, Madjiheurem, Tomlinson, Elster, Apps, Witherspoon, Piloto (2024)](https://arxiv.org/abs/2406.07234). *OPFData: Large-scale datasets for AC optimal power flow with topological perturbations*.
  Large AC-OPF dataset with topology perturbations and contingencies. Built from PGLib-OPF using PowerModels.jl + IPOPT. Useful for ML generalization beyond fixed-topology OPF.

* [Joswig-Jones, Zamzam, Baker (2021)](https://arxiv.org/abs/2111.01228). *OPF-Learn: An Open-Source Framework for Creating Representative AC Optimal Power Flow Datasets*.
  Open-source pipeline for generating AC-OPF datasets. Focus on representative sampling, scalable data generation, reproducible ML-for-OPF workflows.


## Learning for AC-OPF / Power Systems

* [Ajeyemi, Chen, Colot, Cortés, Dall’Anese (2025)](https://arxiv.org/abs/2505.22399). *Learning to Pursue AC Optimal Power Flow Solutions with Feasibility Guarantees*.
  Learning-based AC-OPF with explicit feasibility guarantees. Emphasis on safe deployment and constraint satisfaction under nonlinear grid physics.

* [Donti, Amos, Kolter (2019)](https://coogan.ece.gatech.edu/papers/pdf/amesecc19.pdf). *Task-based End-to-End Model Learning in Stochastic Optimization*.
  Early influential differentiable optimization paper. Learn predictive models directly against downstream decision quality, not prediction error.

* [Lavaei et al. (2025)](https://lavaei.ieor.berkeley.edu/NN_OPT_2025_1.pdf). *[Title unavailable from provided PDF link]*.
  Neural-network-driven optimization/control formulation from the Berkeley optimization group. Focus on optimization-aware learning and guarantees for power/energy systems.

* [Unknown authors (2025)](https://www.sciencedirect.com/science/article/abs/pii/S0306261925003678?via%3Dihub). *[Title unavailable from abstract page]*.
  Recent Energy journal paper on ML + optimization for energy systems. Appears focused on scalable operational decision-making under physical constraints.
