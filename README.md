## Argo

<img src="https://github.com/user-attachments/assets/8eb6a4c1-bbcc-486d-92a5-6c24e6e2f0be" alt="argo" width="200"/>

> Argo, the ship that carried Jason and the Argonauts on their quest for the Golden Fleece

This is a playground to re-implement model architectures from industry/academic papers in Pytorch. The primary goal is educational and the target audience is for those who would like to start journey in machine learning & machine learning infra. The code implementation is optimized for readability and expandability, while not for the best of performance.

### Repo structure

- data: functions for dataset management, such as downloading public dataset, cache management, etc
- model: model code implementation
- trainer: simple wrapper around train/val/eval loop
- server: simple inference stack for recommendation system

### How to run locally

1. install the dependency `pip install -r requirements.txt`, `pip install -e .`
2. run `python main.py` to train the model with current env config.
3. run `python server/inference_engine.py` to start the inference server, it would listen on 8000 port
4. run `bash scripts/server_request.sh` to send a dummy request

### Papers

- :white_check_mark: [Deep Interest Network for Click-Through Rate Prediction](https://arxiv.org/abs/1706.06978)
- :white_check_mark: [TransAct: Transformer-based Realtime User Action Model for Recommendation at Pinterest](https://arxiv.org/abs/2306.00248)
- [Actions Speak Louder than Words: Trillion-Parameter Sequential Transducers for Generative Recommendations](https://arxiv.org/pdf/2402.17152)
- [Better Generalization with Semantic IDs: A Case Study in Ranking for Recommendations](https://dl.acm.org/doi/abs/10.1145/3640457.3688190)
- [DCN V2: Improved Deep & Cross Network and Practical Lessons for Web-scale Learning to Rank Systems](https://arxiv.org/pdf/2008.13535)
- [LONGER: Scaling Up Long Sequence Modeling in Industrial Recommenders](https://www.arxiv.org/pdf/2505.04421)

### Road Map

- [x] :white_check_mark: Deep Interest Network E2E training & inference example, MovieLen Small
- [x] :white_check_mark: TransAct training & inference example, MovieLen Large
- [ ] MovieLen item ~embedding generation~, collaborative filtering, ~two-towers~, LLM
- [ ] HSTU training & inference example, MoiveLen Small
- [ ] Kuaishou Dataset
- [ ] Deep Interest Network Scaling, MovieLen 32M dataset
- [ ] RQ-VAE
- [ ] Multi-stage recommendation system, candidate generation, ranking, reranking
- [ ] Nearline item embedding update
- [ ] Feature store integration
- [ ] Feature logging & training data generation pipeline
- [ ] GPU training & inference enablement
- [ ] Integrate profiling, benchmarking, tuning, and monitoring for accelerator optimization
- [ ] Optimize representative models with auto-tuning, kernel fusion, quantization, dynamic batching, etc
- [ ] Ray integration (DPP reader + trainer arch)
- [ ] Daft, Polars exploartion

