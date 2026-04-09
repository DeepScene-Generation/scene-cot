# IndoorScene-CoT
This is the repository that contains code, data and supplementary materials for IndoorScene-CoT.

- The dataset is located in the `dataset` folder.
- Supplementary materials are provided in `supplementary.pdf`.
- We provide training code, and the model can be trained by running the executable script:
```bash
bash scripts/deepscenegen/deepscenegen_qwen_instruct_7b_12k_grpo_3ep.sh
```

## Dataset
**train_scenecot_sft** includes 443 annotated samples, each consisting of a natural language instruction, a complete reasoning path, and the corresponding final scene layout. It is used to warm up the base model and activate its structured generation capabilities.

**train_scenecot_rl** contains 1,248 entries, where only user preferences are provided. It is designed to improve scene diversity and spatial plausibility through online policy optimization.

Each scene in **test_scenecot** is manually inspected and refined to ensure spatial accuracy and semantic coherence. **test_scenecot** contains eight room types, including bedrooms, living rooms, dining rooms, studies, and more, with approximately six samples per category.

**3dfront_aug** contains 13,484 samples with complete reasoning traces enhanced from the 3D-FRONT dataset using our IndoorScene-CoT method.

### License
Our dataset is under the CC-BY-NC-SA-4.0 license.

IndoorScene-CoT is only used for academic research. Commercial use in any form is prohibited.
