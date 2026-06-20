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

**`Latest_Code/`**


Current/cleaned pipeline notebooks.

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

A local working copy that is mostly the same as CRISP on GitHub. The difference is in the notebooks: this copy stores newly made templates of the code, including denoise preprocessing, SNR value, a default algorithm, and automation that runs without manual clicking.

<a id="01-crisp-run-root"></a>

**`01_CRISP_run/ (root)`**


CryoSPARC automation worker script (`cryo_spark_worker.ipynb`) — runs at the repo root, outside the `notebook/` subfolder.

<details>
<summary>1 notebook(s) — click to expand</summary>

- [cryo_spark_worker.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/cryo_spark_worker.ipynb)

</details>

<a id="01-crisp-run-notebook"></a>

**`01_CRISP_run/notebook/`**


The active, currently-used notebook templates for this working copy.

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

**`01_CRISP_run/notebook/dep/`**


Deprecated/superseded versions of the notebook templates above, kept for reference.

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

**`01_CRISP_run/simulation/`**


Micrograph simulation notebooks — used to generate synthetic test data independent of the real EMPIAR datasets.

<details>
<summary>2 notebook(s) — click to expand</summary>

- [micrograph_simulation.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/simulation/micrograph_simulation.ipynb)
- [Untitled0.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/01_CRISP_run/simulation/Untitled0.ipynb)

</details>


---

<a id="test-on-10017"></a>
## `Test_on_10017/Test_0_9-8_9-30_EM_10017/` — Main Test Campaign

All work on EMPIAR-10017, date range Sep 8 -> Sep 30. The name itself encodes the date span of the run. Sub-sections below, in pipeline order: early single attempts first, then the two training-source variant series, then the main experiment directory.

<a id="tpzd-default-output"></a>
<a id="tpzd-default-files"></a>

**`TpzD_default_output/Archieve_CDCRF/TpzD_default_code_archive/`**

**Status:** First Topaz attempt · **Keywords:** topaz, default  

The first try of the Topaz-default pipeline — running Topaz with its out-of-the-box default settings before any project-specific tuning.

<details>
<summary>3 notebook(s) — click to expand</summary>

- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/TpzD_default_output/Archieve_CDCRF/TpzD_default_code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/TpzD_default_output/Archieve_CDCRF/TpzD_default_code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/TpzD_default_output/Archieve_CDCRF/TpzD_default_code_archive/04_particle_extraction_clean.ipynb)

</details>

<a id="dep"></a>
<a id="dep-files"></a>

**`_dep/TpzD_output/final log/Code Archive/`**

**Status:** Retired · **Keywords:** deprecated  

Deprecated content — retired material from the first Topaz-Denoise output attempt, kept for the record but superseded by later runs.

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

**Keywords:** topaz denoise, trained model, timing · **Status:** Topaz Denoise to train model

Directory for testing the trained model with **Topaz Denoise**. Internal naming follows the same logic as `raw_user_output_rst` below — each sub-folder mirrors one of that directory's experiment types, just run on the Topaz-denoised track instead of the raw track.

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

**`time_test_output_tpz/code archive/`**


Baseline code archive for this series.

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

**`time_test_output_tpz/02_50_extend_100_crf_rst/code_archieve/`**


CRF epoch-extension test (50->100) on the Topaz-denoise track.

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

**`time_test_output_tpz/results_50_CRF/code_archieve/`**


CRF, EPOCHS=50.

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

**`time_test_output_tpz/results_100_CRF/code_archieve/`**


CRF, EPOCHS=100.

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

**`time_test_output_tpz/results_100_ESPatience_50_CRF/code_archieve/`**


EPOCHS=100, early-stop patience=50.

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

**`time_test_output_tpz/weight_test_tpz/code_archive/`**


W1/W2 kernel-weight study on the Topaz-denoise track.

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

**`time_test_output_tpz/weight_test_tpz_50/code_archive/`**


W1/W2 kernel-weight study variant (50).

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

**`time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/`**


Multi-weight sweep, run 1.

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

**`time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/`**


Multi-weight sweep, run 2.

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

**`time_test_output_tpz/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/`**


Multi-weight sweep, run 3.

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

**Keywords:** conventional denoise, reference map, segmentation · **Status:** Conventional Denoise to train model

Directory for testing the trained model with a **conventional denoising method** used as the reference map (for the `01`/`02` notebook model training & segmentation). This is the expensive reference run — conventional denoising is costlier than Topaz Denoise, which is why it gets its own dedicated comparison series. Internal naming follows `raw_user_output_rst`.

```text
├── C_CSN_D_float_u_code_archive/                 # Baseline code archive
├── results_50_CRF/                               # CRF, EPOCHS=50
└── results_100_CRF/                              # CRF, EPOCHS=100
```

<a id="csn-base"></a>

**`C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/`**


Baseline code archive for this series.

<details>
<summary>5 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/C_CSN_D_float_u_code_archive/04_particle_extraction_clean.ipynb)

</details>

<a id="csn-results-50-crf"></a>

**`C_CSN_D_float_u_output/results_50_CRF/code_archieve/`**


CRF, EPOCHS=50.

<details>
<summary>5 notebook(s) — click to expand</summary>

- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/C_CSN_D_float_u_output/results_50_CRF/code_archieve/05_01_cryosparc_auto.ipynb)

</details>

<a id="csn-results-100-crf"></a>

**`C_CSN_D_float_u_output/results_100_CRF/code_archive/`**


CRF, EPOCHS=100.

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

**Keywords:** main, experiments, raw output · **Status:** ★ Main directory

The main experiment directory — holds the raw output (micrograph **without** denoising) and the bulk of every experiment run. Each `results_*` / `weight_*` folder is one experiment and (per the project convention) contains its own `code_archive/` + `10017/` sub-folders. Grouped by theme below; click any line to jump to that experiment's notebooks.

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

**`raw_user_output_rst/raw_user_output_rst_code_archive/`**

**Status:** Baseline — first run · **Keywords:** first test, raw micrograph  

The first test of the code, run on the raw micrograph.

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

**`raw_user_output_rst/weight_test_rst_raw/code_archive/`**

**Status:** Weight study · **Keywords:** w1, w2, kernel weights, pairwise potential  

Tests examining the weights **W1** and **W2** for the kernel used in the pairwise potentials (raw-track variant).

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

**`raw_user_output_rst/weight_test_rst/code_archive/`**

**Status:** Weight study · **Keywords:** w1, w2, kernel weights, pairwise potential  

Tests examining the weights **W1** and **W2** for the kernel used in the pairwise potentials.

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

**`raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/`**

**Status:** Weight experiment try triple · **Keywords:** w1, w2, experiment on weight

Multi Experiment tried extra trpple times of the W1/W2 - run 1.

<details>
<summary>3 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_1/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)

</details>

<a id="rst-weight-multi-2"></a>

**`raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/`**

**Status:** Weight experiment try triple · **Keywords:** w1, w2, experiment on weight

Multi Experiment tried extra trpple times of the W1/W2 - run 2.

<details>
<summary>4 notebook(s) — click to expand</summary>

- [00-0γ_For_Denoized_mrc_Topaz_Preprocessing.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/00-0%CE%B3_For_Denoized_mrc_Topaz_Preprocessing.ipynb)
- [00-ζ-2-histogram_of_mask_prob.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/00-%CE%B6-2-histogram_of_mask_prob.ipynb)
- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/01_training_models_clean.ipynb)
- [02-0α-dnzd-pairwise_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_2/code_archive/02-0%CE%B1-dnzd-pairwise_finetune_with_crf_clean.ipynb)

</details>

<a id="rst-weight-multi-3"></a>

**`raw_user_output_rst/WEIGHT_MULTIPLE_TEST/rst_3/code_archive/`**

**Status:** Weight experiment try triple · **Keywords:** w1, w2, experiment on weight

Multi Experiment tried extra trpple times of the W1/W2 - run 3.

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

**`raw_user_output_rst/results_with_denoise_reference_CRF/code_archive/`**

**Status:** Kernel-reference test · **Keywords:** denoised reference, bilateral kernel, CRF  

Test using the **denoised micrograph** as the bilateral-kernel reference (`I_i`, `I_j`) in the CRF pairwise potential:

```
k(f_i, f_j) = w1·exp( −‖P_i−P_j‖² / 2σ1² − ‖I_i−I_j‖² / 2σ2² ) + w2·exp( −‖P_i−P_j‖² / 2σ3² )
```

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

**`raw_user_output_rst/results_50_CRF/code_archive/`**

**Status:** Hyperparam: epochs · **Keywords:** CRF, EPOCHS=50, notebook 01  

Use **CRF** instead of CD-CRF; hyperparameter `EPOCHS = 50` (for notebook `01`).

<details>
<summary>5 notebook(s) — click to expand</summary>

- [01_training_models_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/01_training_models_clean.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/03_select_hyperparam_for_extraction_clean.ipynb)
- [04_particle_extraction_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/04_particle_extraction_clean.ipynb)
- [05_01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_50_CRF/code_archive/05_01_cryosparc_auto.ipynb)

</details>

<a id="rst-results-100-crf"></a>

**`raw_user_output_rst/results_100_CRF/code_archive/`**

**Status:** Hyperparam: epochs · **Keywords:** CRF, EPOCHS=100  

Same as `results_50_CRF/`, but `EPOCHS = 100`.

<details>
<summary>5 notebook(s) — click to expand</summary>

- [01_training_models_clean (1).ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/01_training_models_clean%20%281%29.ipynb)
- [02_finetune_with_crf_clean.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/02_finetune_with_crf_clean.ipynb)
- [03_select_hyperparam_for_extraction_clean (1).ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/03_select_hyperparam_for_extraction_clean%20%281%29.ipynb)
- [04_particle_extraction_clean (1).ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/04_particle_extraction_clean%20%281%29.ipynb)
- [05-01_cryosparc_auto.ipynb](https://colab.research.google.com/github/SRT-0/Cryo_Project_Test/blob/main/Test_on_10017/Test_0_9-8_9-30_EM_10017/raw_user_output_rst/results_100_CRF/code_archive/05-01_cryosparc_auto.ipynb)

</details>

<a id="rst-results-100-espatience-50-crf"></a>

**`raw_user_output_rst/results_100_ESPatience_50_CRF/code_archive/`**

**Status:** Hyperparam: patience · **Keywords:** CRF, EPOCHS=100, ESPatience=50, early stop  

`EPOCHS = 100` (notebook `01`) and `ESPatience = 50` (for notebook `02` training). **Motivation:** the model converged fast and stopped improving for many steps, so early-stop patience was raised to avoid stopping too soon — later found it was fine for `02` to converge fast and stop improving in a short while.

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

**`raw_user_output_rst/results_watershed_test/code_archive/`**

**Status:** Deprecated — strong F1/mAP · **Keywords:** watershed, distance transform, DT map, post-processing  

First experiment using watershed as the post-processing algorithm (now **deprecated**), but F1 and mAP were good compared with other algorithms. Settled on feeding the **Distance-Transform map** into the watershed: the first pixel where prob > 0.5 (the boundary) is set to a value, a pixel 2px from the boundary gets 2, the particle centre is expected near the centre — then watershed runs on the DT map.

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

**`raw_user_output_rst/_Deprecated/results_watershed_no_DT/code_archive/`**

**Status:** Deprecated · **Keywords:** watershed, no distance transform, ablation  

Watershed run **without** the Distance-Transform step — an ablation to confirm the DT map (introduced in `results_watershed_test/` above) is actually contributing.

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

**`raw_user_output_rst/_Deprecated/results_watershed_mix_DT_model_prob_map/code_archive/`**

**Status:** Deprecated · **Keywords:** hybrid score, mix probability+DT, solidity, aspect ratio  

Hybrid scoring variant: combines α·probability + β·Distance-Transform into one score instead of using the DT map alone, filtered by hard solidity + aspect-ratio cutoffs instead of MAD.

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

**`raw_user_output_rst/results_watershed_malha/code_archive/`**

**Status:** Deprecated · **Keywords:** mahalanobis, shape metrics, threshold  

Apply **Mahalanobis** distance transform to the shape metrics and apply a threshold test. **Deprecated.**

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

**`raw_user_output_rst/results_watershed_indiv_test/code_archive/`**

**Status:** Threshold study · **Keywords:** threshold, area, F1, mAP  

Test how **F1 and mAP change under different thresholds**: removing the Area (and other shape-metric) thresholds raises F1; adding more thresholds lowers F1 a little while raising mAP a little.

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

**`raw_user_output_rst/results_watershed_clustering/code_archive/`**

**Status:** Exploratory — led to angle insight · **Keywords:** clustering, shape metrics, angle, intensity  

**Clustering on shape metrics** to separate groups; particles of the same group are stacked by mean intensity and forced to the same angle. Observed 1–2 groups that look like noise or sit between two particles → shape metrics may relate to particle angle, useful for filtering out spurious centres that actually fall between two particles.

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

**`raw_user_output_rst/results_watershed_angles/code_archive/`**

**Status:** ★ Settled — current standard · **Keywords:** area, circularity, MAD, eccentricity, solidity, Hu moments, angles  

The **fixed/settled structure**: filter particles using Area + circularity with MAD, record Area, circularity, eccentricity, solidity, and Hu moments (1st/2nd/3rd), then run statistical tests on the relation between angles and these metrics.

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

**`raw_user_output_rst/results_watershed_circularity_NO_MAD/code_archive/`**

**Status:** results_watershed_angles/ + did not use the shape metric to filter · **Keywords:** circularity, no MAD, angle relation  

Same as `results_watershed_angles/`, but **stop filtering with circularity + MAD** (Median Absolute Deviation) to observe more of the relation between shape metrics and the angle of the particles on the micrograph.

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

**`raw_user_output_rst/results_diff_post_processing_but_circularity_MAD/code_archive/`**

**Status:** Worse than watershed · **Keywords:** circularity, MAD, other post-processing  

Apply the circularity + MAD filtering to a **different post-processing algorithm** (not watershed). Result was **not** as good as watershed — both F1 and mAP dropped after filtering.

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

**`raw_user_output_rst/results_watershed_with_01_model_map/code_archive/`**

**Status:** Comparison CRF vs no-CRF (no big diff) · **Keywords:** notebook 01 model, no CRF finetune, comparison  

Same setup as `results_watershed_angles/`, but using the model from Colab notebook `01` — the model **without** CRF fine-tuning. Found **no big difference** in the final result between the model with vs. without CRF.

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

## Notes

- Greek-letter characters in filenames (α, β, γ, ζ, Δ, κ) are URL-encoded in the Colab links automatically — click-through works even though the raw text shows the encoded form in the URL.

- Notebooks within every folder are sorted in pipeline order (00 → 06); files without a numeric prefix sort to the end of their folder.

- Section jump-links use explicit anchor IDs (not GitHub's auto-generated heading slugs), so they work reliably even with special characters in headings.

- For *why* each experiment exists (not just *where* its code is), cross-reference with `README_cryo_project_structure.md` and `metric_literature_review.md`.
