# FL Security Papers

A list of interesting papers on attacks and defenses on Federated Learning (FL)

I think we should focus on Active MIAs, as they capture this sense of the central server manipulating the model to extract infromation. I attached 2 papers. 

## Attacks

## Differential Privacy

- Athanasiou et al. [**"Enhancing Metric Privacy With a Shuffler"**](https://hal.science/hal-04895564/document) @ **PETS 2025**.
- Diaz et al. [**"Metric Privacy in Federated Learning for Medical Imaging: Improving Convergence and Preventing Client Inference Attacks"**](https://arxiv.org/pdf/2502.01352) @ **Arxiv 2025**.

## Anonymity

- Agiollo et al. [**"Anonymous Federated Learning via Named-Data Networking"**](https://www.sciencedirect.com/science/article/pii/S0167739X23004144) @ **FGCS 2024**.

## Active MIAs
-  **Active Membership Inference Attack under Local Differential Privacy in Federated Learning** ( https://proceedings.mlr.press/v206/nguyen23e/nguyen23e.pdf)
- **Comprehensive Privacy Analysis of Deep Learning: Passive and Active White-box Inference Attacks against Centralized and Federated Learning** (https://arxiv.org/pdf/1812.00910)


## Gradient Disaggregation
-  **Gradient Disaggregation: Breaking Privacy in Federated Learning by Reconstructing the User Participant Matrix** (https://proceedings.mlr.press/v139/lam21b/lam21b.pdf)
  _Semi-honest server. Assumes the gradients stay almost (almost = noise which is removed) consintent between round. Their goal is to find the participating users and their individual gradients using linear regression. SVD is used to remove the noise (i.e. approximate the non-noisy matrix). The problem is NP-hard so some additional statistics over the clients are assumed which make the computation feasible._


-  **Eluding Secure Aggregation in Federated Learning via Model Inconsistency.**  (https://arxiv.org/pdf/2111.07380)
_Malicious server. Hacks Secure Aggregation by having the server manipulate the gradients. To get the gradient of a target user u, it suffices to send carefully crafted models to all the other clients, such that when they do their training they get a 0 gradient. Thus, securely aggregating all the gradients will just result to the gradient of target user u. The crafted models are based on finding a proper input for Relu s.t. it always outputs 0._
-  **SRATTA: SAMPLE RE-ATTRIBUTION ATTACK OF SECURE AGGREGATION IN FEDERATED LEARNING** (https://arxiv.org/pdf/2306.07644)
