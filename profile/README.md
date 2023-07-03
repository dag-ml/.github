# Directed Acyclic Graphs for Medical Risk Assessment

## Description
Design/Approach to use Directed Acyclic Graph (DAGs) for medical risk assessment for astronauts. This tool can then assist medical and causality experts, and help NASA Human System Risk Board (HSRB) formalize a shared mental model of the causal flow of risk among Risk Board stakeholders. These DAGs are created and drawn by medical and causality experts, and you can read more about the DAG approach in [this report](https://ntrs.nasa.gov/api/citations/20220006812/downloads/HSRB%20DAG%20Guidance%20Documentation_NASA%20TM-20220006812_Update.pdf). For further background, refer to [this paper](https://www.mdpi.com/1813442) that validates the DAG connections by populating them with empirical biological data from the NASA Open Science Data Repository.

## Outline
ML-generated graphs for medical risk assessment will be compared back to the original DAGs drawn by the experts.

We’ll be assessing the outcomes by trying to answer the following questions:

- What are the outputs from the algorithm? *(i.e., does it give us a picture, an edge list, and adjacency matrix, or some combination of these? Something else?)*
- Which is best for HSRB applications, where the datasets will likely be small, both in the sense of few features and few training instances *(i.e., few columns and few rows)*? In complementary fashion, which might be better for larger applications like engineering anomaly data or ‘omics data?
- How do we know if the DAG produced is “the best” that be learned?
- Is there a set of these algorithms we should always do together to get the “best” possible answer?
- How can we measure the degree of congruence with a known graph? By this I mean, if it produces something “close” to what our SMEs had drawn, what is the appropriate way to see “how close” it really is? *(i.e., find or develop a “congruence measure”.)*

## Data
- [Dose-dependent skeletal deficits due to varied reductions in mechanical loading in rats (Tibia - pQCT)](https://doi.org/10.26030/emsm-0648) (Ko, 2020) 1/2
- [Dose-dependent skeletal deficits due to varied reductions in mechanical loading in rats (Femur - microCT, three-point bending, histomorphometry)](https://doi.org/10.26030/b09t-mw60) (Ko, 2020) 2/2
- [Quantifying Cancellous Bone Structural Changes in Microgravity: Axial Skeleton Results from the RR-1 Mission](https://doi.org/10.26030/8wja-w380) (Dubeé, 2022)
- [Effects of Spaceflight on Bone Microarchitecture in the Axial and Appendicular Skeleton in Growing Ovariectomized Rats from STS-62](https://doi.org/10.26030/cztm-cx29) (Keune, 2015)
- [Spaceflight-induced (STS-62) vertebral bone loss in ovariectomized rats is associated with increased bone marrow adiposity and no change in bone formation](https://doi.org/10.26030/kb2k-2150) (Keune, 2016)


## Algorithms
- [PC](https://doi.org/10.48550/arXiv.1211.3295)
- [Grow-Shrink](https://doi.org/10.48550/arXiv.1407.8088)
- [Incremental Association](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4184048/) (IAMB)
- [Fast Incremental Association](https://www.cs.cmu.edu/~dmarg/Papers/Yaramakala-Margaritis-ICDM05-with-header.pdf) (Fast-IAMB)
- [Interleaved Incremental Association](https://www.cs.cmu.edu/~dmarg/Papers/Yaramakala-Margaritis-ICDM05-with-header.pdf) (Inter-IAMB)
- [Incremental Association with FDR](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3400681/) (IAMB-FDR)
- Max-Min Parents and Children (MMPC)
- Semi-Interleaved HITON-PC
- Hybrid Parents and Children (HPC)

## Authors
- @bdogetlauncher
- @camwolff02
- @campjake
- @jasperdoan
- @max9001
- @mcdipples
- @nadia-eecs
