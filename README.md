# `cryo_project` — Code Archive & Colab Index

> GitHub backup/mirror of the `cryo_project` Google Drive code, with direct **Open in Colab** links for every notebook, sorted in pipeline order (00 → 06) within each folder.

> For the *full* Drive structure (including non-code folders like `data/`, `temp/`, `record_tabular/` that aren't mirrored here) see [`README_cryo_project_structure.md`](./README_cryo_project_structure.md).

> **Convention:** each experiment folder has a `code_archive/` (the code that was run) — that's what's indexed below. Click any folder name in a layout tree to jump straight to its section.

---

## Repository Layout

```text
├── Latest_Code/                                  # ⭐ Start here — latest organized code
├── 01_CRISP_run/                                 # Local CRISP working copy + custom notebooks
|   ├── (root)                                    # cryo_spark_worker.ipynb
|   ├── notebook/                                 # Active notebook templates
|   ├── notebook/dep/                             # Deprecated notebook versions
|   └── simulation/                               # Micrograph simulation notebooks
└── Test_on_10017/Test_0_9-8_9-30_EM_10017/       # Main EMPIAR-10017 test campaign
    ├── TpzD_default_output/                      # First Topaz-default attempt
    ├── _dep/                                     # Deprecated material
    ├── time_test_output_tpz/                     # Topaz-Denoise -> train-model series (many sub-experiments, see its own layout)
    ├── C_CSN_D_float_u_output/                   # Conventional-Denoise -> train-model series (see its own layout)
    └── raw_user_output_rst/                      # * MAIN experiment directory (many sub-experiments, see its own layout)
```

**Jump to a section:**

- [Latest_Code/](#latest-code)
- [01_CRISP_run/](#01-crisp-run) ([root](#01-crisp-run-root), [notebook/](#01-crisp-run-notebook), [notebook/dep/](#01-crisp-run-notebook-dep), [simulation/](#01-crisp-run-simulation))
- [Test_on_10017/...](#test-on-10017)
  - [software/topaz/tutorial/](#software-topaz-tutorial)
  - [TpzD_default_output/](#tpzd-default-output)
  - [_dep/](#dep)
  - [time_test_output_tpz/](#time-test-output-tpz) — has its own layout below
  - [C_CSN_D_float_u_output/](#c-csn-d-float-u-output) — has its own layout below
  - [raw_user_output_rst/](#raw-user-output-rst) ★ — has its own layout below


---

<a id="latest-code"></a>
## ⭐ `Latest_Code/` — Start Here

The latest, organized version of the code — if you just want the current pipeline without digging through experiment history, start here.

<a id="latest-code-files"></a>

**`Latest_Code/`** — Current/cleaned pipeline notebooks.

<details open>
<summary>13 notebook(s) — click to expand</summary>

- [00-00_SNR_evaluation.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/00-00_SNR_evaluation.ipynb)
- [00-0α_Topaz_denoise.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/00-0%CE%B1_Topaz_denoise.ipynb)
- [00-0β_conventional_denoise_CryoSegNet.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/00-0%CE%B2_conventional_denoise_CryoSegNet.ipynb)
- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-A_Mask_Generator_clean_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/00-A_Mask_Generator_clean_auto.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/04_particle_extraction_clean.ipynb)
- [05_0α_cryosparc_extract_angle_(for do analysis on shape metrics).ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/05_0%CE%B1_cryosparc_extract_angle_%28for%20do%20analysis%20on%20shape%20metrics%29.ipynb)
- [05_cryosparc.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/05_cryosparc.ipynb)
- [06_statistical_test_of_shape_metrics_and_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Latest_Code/06_statistical_test_of_shape_metrics_and_angle_orientation_plot.ipynb)

</details>


---

<a id="01-crisp-run"></a>
## `01_CRISP_run/` — Local CRISP Working Copy

Mostly mirrors CRISP on GitHub. The difference is in the notebooks: this copy adds denoise preprocessing, SNR evaluation, a default algorithm, and click-free automation.

<a id="01-crisp-run-root"></a>

**`01_CRISP_run/ (root)`** — CryoSPARC automation worker script.

<details>
<summary>1 notebook(s) — click to expand</summary>

- [cryo_spark_worker.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/cryo_spark_worker.ipynb)

</details>

<a id="01-crisp-run-notebook"></a>

**`01_CRISP_run/notebook/`** — Active notebook templates.

<details>
<summary>17 notebook(s) — click to expand</summary>

- [00-00_SNR_evaluation.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-00_SNR_evaluation.ipynb)
- [00-00_SNR_evaluation_parrallel.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-00_SNR_evaluation_parrallel.ipynb)
- [00-0α_Topaz_denoise.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-0%CE%B1_Topaz_denoise.ipynb)
- [00-0β_conventional_denoise_CryoSegNet.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-0%CE%B2_conventional_denoise_CryoSegNet.ipynb)
- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-A-01_Mask_Generator_clean_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-A-01_Mask_Generator_clean_auto.ipynb)
- [00-A_Mask_Generator_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-A_Mask_Generator_clean.ipynb)
- [00-B_Dataset preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-B_Dataset%20preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [00-ζ-mask_prediction_test_for_different_models.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/00-%CE%B6-mask_prediction_test_for_different_models.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/05_01_cryosparc_auto.ipynb)
- [05_cryosparc.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/05_cryosparc.ipynb)

</details>

<a id="01-crisp-run-notebook-dep"></a>

**`01_CRISP_run/notebook/dep/`** — Deprecated/superseded notebook versions.

<details>
<summary>7 notebook(s) — click to expand</summary>

- [00-00_SNR_evaluation_dep.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/dep/00-00_SNR_evaluation_dep.ipynb)
- [00-00_SNR_evaluation_numba.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/dep/00-00_SNR_evaluation_numba.ipynb)
- [00-00_SNR_evaluation_opt.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/dep/00-00_SNR_evaluation_opt.ipynb)
- [00-0β_conventional_denoise_CryoSegNet_float32.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/dep/00-0%CE%B2_conventional_denoise_CryoSegNet_float32.ipynb)
- [00-0β_conventional_denoise_cuda_CSN_float32.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/dep/00-0%CE%B2_conventional_denoise_cuda_CSN_float32.ipynb)
- [00-A_Mask_Generator_clean (1).ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/dep/00-A_Mask_Generator_clean%20%281%29.ipynb)
- [00-A_Mask_Generator_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/notebook/dep/00-A_Mask_Generator_clean.ipynb)

</details>

<a id="01-crisp-run-simulation"></a>

**`01_CRISP_run/simulation/`** — Micrograph simulation notebooks.

<details>
<summary>2 notebook(s) — click to expand</summary>

- [micrograph_simulation.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/simulation/micrograph_simulation.ipynb)
- [Untitled0.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/simulation/Untitled0.ipynb)

</details>


---

<a id="test-on-10017"></a>
## `Test_on_10017/Test_0_9-8_9-30_EM_10017/` — Main Test Campaign

All work on EMPIAR-10017, date range Sep 8 -> Sep 30. Sub-sections below, in pipeline order: tutorial/setup material first, then early single attempts, then the two training-source variant series, then the main experiment directory.

<a id="software-topaz-tutorial"></a>
<a id="topaz-tutorial-files"></a>


</details>

<a id="tpzd-default-output"></a>
<a id="tpzd-default-files"></a>

**`TpzD_default_output/Archieve_CDCRF/TpzD_default_code_archive/`** — First try of the Topaz-default pipeline.

<details>
<summary>3 notebook(s) — click to expand</summary>

- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/TpzD_default_output/Archieve_CDCRF/TpzD_default_code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/TpzD_default_output/Archieve_CDCRF/TpzD_default_code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/TpzD_default_output/Archieve_CDCRF/TpzD_default_code_archive/04_particle_extraction_clean.ipynb)

</details>

<a id="dep"></a>
<a id="dep-files"></a>

**`_dep/TpzD_output/final log/Code Archive/`** — Deprecated material from the first Topaz-Denoise output attempt.

<details>
<summary>9 notebook(s) — click to expand</summary>

- [00-0α_Topaz_denoise.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/00-0%CE%B1_Topaz_denoise.ipynb)
- [00-0β_conventional_denoise_CryoSegNet.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/00-0%CE%B2_conventional_denoise_CryoSegNet.ipynb)
- [00-A_Mask_Generator_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/00-A_Mask_Generator_clean.ipynb)
- [00-B_Dataset preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/00-B_Dataset%20preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/04_particle_extraction_clean.ipynb)
- [05_cryosparc.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/_dep/TpzD_output/final%20log/Code%20Archive/05_cryosparc.ipynb)

</details>


---

<a id="time-test-output-tpz"></a>
### `time_test_output_tpz/` — Topaz-Denoise -> Train-Model Series

Trains/tests the model using Topaz-denoised micrographs as input. Internal naming follows the same logic as `raw_user_output_rst` below.

```text
├── code archive/                                 # Baseline code archive
├── 02_50_extend_100_crf_rst/                     # CRF epoch-extension test (50->100)
├── results_50_CRF/                               # CRF, EPOCHS=50
├── results_100_CRF/                              # CRF, EPOCHS=100
├── results_100_ESPatience_50_CRF/                # EPOCHS=100, early-stop patience=50
├── weight_test_tpz/                              # W1/W2 kernel-weight study
├── weight_test_tpz_50/                           # W1/W2 kernel-weight study variant (50)
├── WEIGHT_MULTIPLE_TEST/rst_1/                   # Multi-weight sweep, run 1
├── WEIGHT_MULTIPLE_TEST/rst_2/                   # Multi-weight sweep, run 2
└── WEIGHT_MULTIPLE_TEST/rst_3/                   # Multi-weight sweep, run 3
```

<a id="tpz-base"></a>

**`time_test_output_tpz/code archive/`** — Baseline code archive for this series.

<details>
<summary>6 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/code%20archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/code%20archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/code%20archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/code%20archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/code%20archive/04_particle_extraction_clean.ipynb)
- [05-01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/code%20archive/05-01_cryosparc_auto.ipynb)

</details>

<a id="tpz-02-50-extend-100-crf"></a>

**`time_test_output_tpz/02_50_extend_100_crf_rst/code_archieve/`** — CRF epoch-extension test (50->100) on the Topaz-denoise track.

<details>
<summary>6 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/02_50_extend_100_crf_rst/code_archieve/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/02_50_extend_100_crf_rst/code_archieve/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/02_50_extend_100_crf_rst/code_archieve/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/02_50_extend_100_crf_rst/code_archieve/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/02_50_extend_100_crf_rst/code_archieve/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/02_50_extend_100_crf_rst/code_archieve/05_01_cryosparc_auto.ipynb)

</details>

<a id="tpz-results-50-crf"></a>

**`time_test_output_tpz/results_50_CRF/code_archieve/`** — CRF, EPOCHS=50.

<details>
<summary>6 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_50_CRF/code_archieve/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_50_CRF/code_archieve/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean_copy.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_50_CRF/code_archieve/02_finetune_with_crf_clean_copy.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_50_CRF/code_archieve/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_50_CRF/code_archieve/04_particle_extraction_clean.ipynb)
- [05-01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_50_CRF/code_archieve/05-01_cryosparc_auto.ipynb)

</details>

<a id="tpz-results-100-crf"></a>

**`time_test_output_tpz/results_100_CRF/code_archieve/`** — CRF, EPOCHS=100.

<details>
<summary>6 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_CRF/code_archieve/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_CRF/code_archieve/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_CRF/code_archieve/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_CRF/code_archieve/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_CRF/code_archieve/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_CRF/code_archieve/05_01_cryosparc_auto.ipynb)

</details>

<a id="tpz-results-100-espatience-50-crf"></a>

**`time_test_output_tpz/results_100_ESPatience_50_CRF/code_archieve/`** — EPOCHS=100, early-stop patience=50.

<details>
<summary>6 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_ESPatience_50_CRF/code_archieve/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_ESPatience_50_CRF/code_archieve/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_ESPatience_50_CRF/code_archieve/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_ESPatience_50_CRF/code_archieve/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_ESPatience_50_CRF/code_archieve/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/results_100_ESPatience_50_CRF/code_archieve/05_01_cryosparc_auto.ipynb)

</details>

<a id="tpz-weight-test-tpz"></a>

**`time_test_output_tpz/weight_test_tpz/code_archive/`** — W1/W2 kernel-weight study on the Topaz-denoise track.

<details>
<summary>7 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="tpz-weight-test-tpz-50"></a>

**`time_test_output_tpz/weight_test_tpz_50/code_archive/`** — W1/W2 kernel-weight study variant (50).

<details>
<summary>7 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz_50/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz_50/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz_50/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz_50/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz_50/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz_50/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/weight_test_tpz_50/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="tpz-weight-multi-1"></a>

**`time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/`** — Multi-weight sweep, run 1.

<details>
<summary>8 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/01_training_models_clean.ipynb)
- [02-0α-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/02-0%CE%B1-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="tpz-weight-multi-2"></a>

**`time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/`** — Multi-weight sweep, run 2.

<details>
<summary>8 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/01_training_models_clean.ipynb)
- [02-0α-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/02-0%CE%B1-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="tpz-weight-multi-3"></a>

**`time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/`** — Multi-weight sweep, run 3.

<details>
<summary>8 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/01_training_models_clean.ipynb)
- [02-0α-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/02-0%CE%B1-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/05_01_cryosparc_auto.ipynb)

</details>


---

<a id="c-csn-d-float-u-output"></a>
### `C_CSN_D_float_u_output/` — Conventional-Denoise -> Train-Model Series

Same idea as the Topaz-denoise series above, but using conventional denoising (CryoSegNet-based) as the reference map — the more expensive reference run.

```text
├── C_CSN_D_float_u_code_archive/                 # Baseline code archive
├── results_50_CRF/                               # CRF, EPOCHS=50
└── results_100_CRF/                              # CRF, EPOCHS=100
```

<a id="csn-base"></a>

**`C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/`** — Baseline code archive for this series.

<details>
<summary>5 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/04_particle_extraction_clean.ipynb)

</details>

<a id="csn-results-50-crf"></a>

**`C_CSN_D_float_u_output/results_50_CRF/code_archieve/`** — CRF, EPOCHS=50.

<details>
<summary>5 notebook(s) — click to expand</summary>

- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/05_01_cryosparc_auto.ipynb)

</details>

<a id="csn-results-100-crf"></a>

**`C_CSN_D_float_u_output/results_100_CRF/code_archive/`** — CRF, EPOCHS=100.

<details>
<summary>5 notebook(s) — click to expand</summary>

- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_100_CRF/code_archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_100_CRF/code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_100_CRF/code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_100_CRF/code_archive/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_100_CRF/code_archive/05_01_cryosparc_auto.ipynb)

</details>


---

<a id="raw-user-output-rst"></a>
### `raw_user_output_rst/` ★ — Main Experiment Directory

The bulk of the experiments, on the raw (non-denoised) micrograph track. Grouped by theme; click any line to jump to that experiment's notebooks.

```text
├── raw_user_output_rst_code_archive/             # Baseline — first test, raw micrograph
├── [Pairwise-Weight Experiments]
|   ├── weight_test_rst_raw/                      # W1/W2 kernel weight test (raw)
|   ├── weight_test_rst/                          # W1/W2 kernel weight test
|   ├── WEIGHT_MULTIPLE_TEST/rst_1-3/             # Multi-weight sweeps
|   └── results_with_denoise_reference_CRF/       # Denoised micrograph as bilateral-kernel reference
├── [CRF Hyperparameter Experiments]
|   ├── results_50_CRF/                           # EPOCHS=50
|   ├── results_100_CRF/                          # EPOCHS=100
|   └── results_100_ESPatience_50_CRF/            # EPOCHS=100, ESPatience=50
└── [Watershed Post-Processing Series]
    ├── results_watershed_test/                   # Deprecated — first watershed attempt
    ├── _Deprecated/results_watershed_no_DT/      # Deprecated — no Distance-Transform
    ├── _Deprecated/results_watershed_mix_DT_model_prob_map/ # Deprecated — hybrid prob+DT score
    ├── results_watershed_malha/                  # Deprecated — Mahalanobis distance filter
    ├── results_watershed_indiv_test/             # Threshold study
    ├── results_watershed_clustering/             # Exploratory — led to angle insight
    ├── results_watershed_angles/                 # * SETTLED — current standard
    ├── results_watershed_circularity_NO_MAD/     # MAD-filter ablation
    ├── results_diff_post_processing_but_circularity_MAD/ # Filter on non-watershed algorithm
    └── results_watershed_with_01_model_map/      # CRF vs no-CRF comparison
```

**Jump within this section:**

- [raw_user_output_rst_code_archive/](#rst-baseline)
- Pairwise-Weight: [weight_test_rst_raw](#rst-weight-test-raw), [weight_test_rst](#rst-weight-test), [rst_1](#rst-weight-multi-1)/[rst_2](#rst-weight-multi-2)/[rst_3](#rst-weight-multi-3), [denoise_reference_CRF](#rst-denoise-reference-crf)
- CRF Hyperparameter: [50_CRF](#rst-results-50-crf), [100_CRF](#rst-results-100-crf), [100_ESPatience_50_CRF](#rst-results-100-espatience-50-crf)
- Watershed: [test](#rst-watershed-test), [no_DT](#rst-watershed-no-dt), [mix_DT](#rst-watershed-mix-dt), [malha](#rst-watershed-malha), [indiv_test](#rst-watershed-indiv-test), [clustering](#rst-watershed-clustering), [angles ★](#rst-watershed-angles), [circularity_NO_MAD](#rst-watershed-circularity-no-mad), [diff_post_processing](#rst-diff-post-processing-circularity-mad), [with_01_model_map](#rst-watershed-with-01-model-map)


#### Shared / Baseline

<a id="rst-baseline"></a>

**`raw_user_output_rst/raw_user_output_rst_code_archive/`** — First test of the code, on the raw micrograph.

<details>
<summary>5 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/raw_user_output_rst_code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/raw_user_output_rst_code_archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/raw_user_output_rst_code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/raw_user_output_rst_code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/raw_user_output_rst_code_archive/04_particle_extraction_clean.ipynb)

</details>


#### Pairwise-Weight (W1/W2 Kernel) Experiments

<a id="rst-weight-test-raw"></a>

**`raw_user_output_rst/weight_test_rst_raw/code_archive/`** — W1/W2 kernel weight test (raw).

<details>
<summary>7 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst_raw/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst_raw/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst_raw/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst_raw/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst_raw/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst_raw/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst_raw/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="rst-weight-test"></a>

**`raw_user_output_rst/weight_test_rst/code_archive/`** — W1/W2 kernel weight test.

<details>
<summary>8 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst/code_archive/01_training_models_clean.ipynb)
- [02-0α-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst/code_archive/02-0%CE%B1-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/weight_test_rst/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="rst-weight-multi-1"></a>

**`raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/`** — Multi-weight sweep, run 1.

<details>
<summary>3 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)

</details>

<a id="rst-weight-multi-2"></a>

**`raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/`** — Multi-weight sweep, run 2.

<details>
<summary>4 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)

</details>

<a id="rst-weight-multi-3"></a>

**`raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/`** — Multi-weight sweep, run 3.

<details>
<summary>8 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/01_training_models_clean.ipynb)
- [02-0α-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/02-0%CE%B1-_copy_dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="rst-denoise-reference-crf"></a>

**`raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/`** — Uses the denoised micrograph as the bilateral-kernel reference (I_i, I_j) in the CRF pairwise potential.

<details>
<summary>7 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0α_adjusted_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/03_0%CE%B1_adjusted_select_hyperparam_for_extraction_clean.ipynb)
- [04_0α_adjusted_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/04_0%CE%B1_adjusted_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/05_01_cryosparc_auto.ipynb)

</details>


#### CRF Hyperparameter Experiments

<a id="rst-results-50-crf"></a>

**`raw_user_output_rst/results_50_CRF/code_archive/`** — CRF, EPOCHS=50 (notebook 01).

<details>
<summary>5 notebook(s) — click to expand</summary>

- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="rst-results-100-crf"></a>

**`raw_user_output_rst/results_100_CRF/code_archive/`** — CRF, EPOCHS=100.

<details>
<summary>5 notebook(s) — click to expand</summary>

- [01_training_models_clean (1).ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/01_training_models_clean%20%281%29.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean (1).ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/03_select_hyperparam_for_extraction_clean%20%281%29.ipynb)
- [04_particle_extraction_clean (1).ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/04_particle_extraction_clean%20%281%29.ipynb)
- [05-01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/05-01_cryosparc_auto.ipynb)

</details>

<a id="rst-results-100-espatience-50-crf"></a>

**`raw_user_output_rst/results_100_ESPatience_50_CRF/code_archive/`** — EPOCHS=100, ESPatience=50 (notebook 02 early-stop tuning).

<details>
<summary>5 notebook(s) — click to expand</summary>

- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_ESPatience_50_CRF/code_archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_ESPatience_50_CRF/code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_ESPatience_50_CRF/code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_ESPatience_50_CRF/code_archive/04_particle_extraction_clean.ipynb)
- [05-01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_ESPatience_50_CRF/code_archive/05-01_cryosparc_auto.ipynb)

</details>


#### Watershed Post-Processing Series

<a id="rst-watershed-test"></a>

**`raw_user_output_rst/results_watershed_test/code_archive/`** — **Deprecated** — first watershed experiment (good F1/mAP). Settled on feeding the Distance-Transform map into watershed.

<details>
<summary>10 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/03_0%CE%B2_DT_watershed_select_hyperparam.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/03_0%CE%B3_DT_watershed_ONLY_hyper.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_test/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="rst-watershed-no-dt"></a>

**`raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/`** — **Deprecated** — watershed without the Distance-Transform step.

<details>
<summary>17 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_default_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/03_0%CE%B3_DT_watershed_default_ONLY_hyper.ipynb)
- [03_0Δ_DT_watershed_2_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/03_0%CE%94_DT_watershed_2_prob.ipynb)
- [03_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/03_DT_watershed_select_hyperparam.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/04_0%CE%B3_particle_extraction.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/05_01_cryosparc_auto.ipynb)
- [05_01_cryosparc_multi_class.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/05_01_cryosparc_multi_class.ipynb)
- [05_02_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/05_02_cryosparc_extract_angle.ipynb)
- [05_03_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/05_03_cryosparc_extract_angle.ipynb)
- [06_0α_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/06_0%CE%B1_angle_orientation_plot.ipynb)
- [06_0β_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/06_0%CE%B2_angle_orientation_plot.ipynb)

</details>

<a id="rst-watershed-mix-dt"></a>

**`raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/`** — **Deprecated** — hybrid α·probability + β·DT scoring (the "Mix_prob/Mix_DT" variant).

<details>
<summary>17 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_default_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/03_0%CE%B3_DT_watershed_default_ONLY_hyper.ipynb)
- [03_0Δ_DT_watershed_2_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/03_0%CE%94_DT_watershed_2_prob.ipynb)
- [03_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/03_DT_watershed_select_hyperparam.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/04_0%CE%B3_particle_extraction.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/05_01_cryosparc_auto.ipynb)
- [05_01_cryosparc_multi_class.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/05_01_cryosparc_multi_class.ipynb)
- [05_02_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/05_02_cryosparc_extract_angle.ipynb)
- [05_03_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/05_03_cryosparc_extract_angle.ipynb)
- [06_0α_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/06_0%CE%B1_angle_orientation_plot.ipynb)
- [06_0β_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/06_0%CE%B2_angle_orientation_plot.ipynb)

</details>

<a id="rst-watershed-malha"></a>

**`raw_user_output_rst/results_watershed_malha/code_archive/`** — **Deprecated** — Mahalanobis distance applied to shape metrics + threshold test.

<details>
<summary>10 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/03_0%CE%B2_DT_watershed_select_hyperparam.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/03_0%CE%B3_DT_watershed_ONLY_hyper.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_malha/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="rst-watershed-indiv-test"></a>

**`raw_user_output_rst/results_watershed_indiv_test/code_archive/`** — Threshold study — how F1/mAP change as shape-metric thresholds are added/removed.

<details>
<summary>12 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/03_0%CE%B2_DT_watershed_select_hyperparam.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_default_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/03_0%CE%B3_DT_watershed_default_ONLY_hyper.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/05_01_cryosparc_auto.ipynb)
- [05_01_cryosparc_multi_class.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/05_01_cryosparc_multi_class.ipynb)
- [05_02_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_indiv_test/code_archive/05_02_cryosparc_extract_angle.ipynb)

</details>

<a id="rst-watershed-clustering"></a>

**`raw_user_output_rst/results_watershed_clustering/code_archive/`** — Exploratory — clustering on shape metrics; led to the angle-relation insight.

<details>
<summary>13 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/03_0%CE%B2_DT_watershed_select_hyperparam.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_default_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/03_0%CE%B3_DT_watershed_default_ONLY_hyper.ipynb)
- [03_0ζ_DT_watershed_cluster_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/03_0%CE%B6_DT_watershed_cluster_hyper.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [04_0γ_watershed_particle_extraction_archive.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/04_0%CE%B3_watershed_particle_extraction_archive.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/05_01_cryosparc_auto.ipynb)
- [05_01_cryosparc_multi_class.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_clustering/code_archive/05_01_cryosparc_multi_class.ipynb)

</details>

<a id="rst-watershed-angles"></a>

**`raw_user_output_rst/results_watershed_angles/code_archive/`** — ★ **Settled / current standard.** Filters with Area + circularity (MAD); records Area, circularity, eccentricity, solidity, Hu moments; runs angle statistics.

<details open>
<summary>15 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/03_0%CE%B2_DT_watershed_select_hyperparam.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_default_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/03_0%CE%B3_DT_watershed_default_ONLY_hyper.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/05_01_cryosparc_auto.ipynb)
- [05_01_cryosparc_multi_class.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/05_01_cryosparc_multi_class.ipynb)
- [05_02_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/05_02_cryosparc_extract_angle.ipynb)
- [05_03_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/05_03_cryosparc_extract_angle.ipynb)
- [06_0α_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/06_0%CE%B1_angle_orientation_plot.ipynb)
- [06_0β_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_angles/code_archive/06_0%CE%B2_angle_orientation_plot.ipynb)

</details>

<a id="rst-watershed-circularity-no-mad"></a>

**`raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/`** — Same as `results_watershed_angles` but **without** the MAD filter — isolates the angle/shape-metric relationship.

<details>
<summary>17 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_default_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/03_0%CE%B3_DT_watershed_default_ONLY_hyper.ipynb)
- [03_0Δ_DT_watershed_2_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/03_0%CE%94_DT_watershed_2_prob.ipynb)
- [03_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/03_DT_watershed_select_hyperparam.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/04_0%CE%B3_particle_extraction.ipynb)
- [04_0γ_watershed_particle_extraction_depr.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/04_0%CE%B3_watershed_particle_extraction_depr.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/05_01_cryosparc_auto.ipynb)
- [05_01_cryosparc_multi_class.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/05_01_cryosparc_multi_class.ipynb)
- [05_02_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/05_02_cryosparc_extract_angle.ipynb)
- [05_03_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/05_03_cryosparc_extract_angle.ipynb)
- [06_0α_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/06_0%CE%B1_angle_orientation_plot.ipynb)
- [06_0β_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/06_0%CE%B2_angle_orientation_plot.ipynb)

</details>

<a id="rst-diff-post-processing-circularity-mad"></a>

**`raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/`** — Circularity+MAD filter applied to a **different** (non-watershed) postprocessing algorithm — performed worse.

<details>
<summary>17 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_default_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/03_0%CE%B3_DT_watershed_default_ONLY_hyper.ipynb)
- [03_0Δ_DT_watershed_2_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/03_0%CE%94_DT_watershed_2_prob.ipynb)
- [03_0κ_select_hyperparam_circularity_MAD.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/03_0%CE%BA_select_hyperparam_circularity_MAD.ipynb)
- [04_0γ_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/04_0%CE%B3_particle_extraction.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [04_0κ_particle_extract_circularity_MAD.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/04_0%CE%BA_particle_extract_circularity_MAD.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/05_01_cryosparc_auto.ipynb)
- [05_01_cryosparc_multi_class.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/05_01_cryosparc_multi_class.ipynb)
- [05_02_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/05_02_cryosparc_extract_angle.ipynb)
- [05_03_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/05_03_cryosparc_extract_angle.ipynb)
- [06_0α_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/06_0%CE%B1_angle_orientation_plot.ipynb)
- [06_0β_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/06_0%CE%B2_angle_orientation_plot.ipynb)

</details>

<a id="rst-watershed-with-01-model-map"></a>

**`raw_user_output_rst/results_watershed_with_01_model_map/code_archive/`** — Same as `results_watershed_angles` but using the **pre-CRF** (notebook 01) model — found no big difference vs. CRF.

<details>
<summary>17 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)
- [03_0β_watershed_select_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/03_0%CE%B2_watershed_select_hyper.ipynb)
- [03_0γ_DT_watershed_default_ONLY_hyper.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/03_0%CE%B3_DT_watershed_default_ONLY_hyper.ipynb)
- [03_0Δ_DT_watershed_2_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/03_0%CE%94_DT_watershed_2_prob.ipynb)
- [03_DT_watershed_select_hyperparam.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/03_DT_watershed_select_hyperparam.ipynb)
- [04_0β_watershed_part.extract.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/04_0%CE%B2_watershed_part.extract.ipynb)
- [04_0γ_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/04_0%CE%B3_particle_extraction.ipynb)
- [04_0γ_watershed_particle_extraction.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/04_0%CE%B3_watershed_particle_extraction.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/05_01_cryosparc_auto.ipynb)
- [05_01_cryosparc_multi_class.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/05_01_cryosparc_multi_class.ipynb)
- [05_02_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/05_02_cryosparc_extract_angle.ipynb)
- [05_03_cryosparc_extract_angle.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/05_03_cryosparc_extract_angle.ipynb)
- [06_0α_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/06_0%CE%B1_angle_orientation_plot.ipynb)
- [06_0β_angle_orientation_plot.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_watershed_with_01_model_map/code_archive/06_0%CE%B2_angle_orientation_plot.ipynb)

</details>


---