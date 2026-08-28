# The Repeat Offenders: Characterizing and Predicting Recurrently Bug-Prone Source Methods

This is the public repository for the RecurrentlyBuggy methods paper containing our dataset, example methods and additional figures. The complete dataset with LLM embeddings can be downloaded from [Zenodo](https://zenodo.org/records/22138983).

```text
.
├── AdditionalFigures/
├── Dataset/
├── ManualAnalysisExamples/
└── RQ3/
```

## `AdditionalFigures/`

Supplementary tables and figures.

- `RepositoryList.md` — table of analyzed repositories, including method counts, snapshot commit identifiers, contributor counts, and star counts.
- `AgeNormalizedRepositoryList.md` — age-normalized repository table with counts and percentages of buggy and recurrently buggy methods.
- `LeaveOneOutTraining/` — five PDF figures containing leave-one-out training results for AdaBoost, Decision Tree, Logistic Regression, neural network (`NN`), and Random Forest models.
- `ThematicAnalysisTaxonomy/` — three PDF taxonomy figures covering bug, context, and syntax themes.

## `Dataset/`

The primary per-repository datasets.

- `EvolutionHistory_CodeMetric/` — 98 CSV files. Each row represents a method and contains its age, evolution/change history, code metrics, edit measurements, and bug-related labels. Sequence-valued fields use `#` as the separator.
- `SourceCode_Inception/` — 92 Parquet files, containing method source-code data at inception.

Within both dataset folders, filenames identify the source repository; for example, `Activiti.csv` and `Activiti.parquet` contain Activiti data in their respective formats.

## `ManualAnalysisExamples/`

Twenty-four numbered JSON files containing examples used for manual analysis. Each file records a method and its source location, commit/change history, detailed diffs, commit metadata, and source snapshots. The filename is the example identifier, such as `2.json` or `105.json`.

## `RQ3/`

PDF figures and compiled results for Research Question 3.

- `All_Results.pdf` — collected RQ3 results.
- `rq3_final_fusion_lopo.pdf` — final fusion leave-one-project-out results.
- `rq3_final_fusion_lopo_all_metrics_cdf_shared_utility.pdf` — final fusion CDF leave-one-project-out results across all metrics.
- `rq3_final_fusion_lopo_mcc_cdf_shared_utility.pdf` — final fusion MCC CDF leave-one-project-out results.
- `rq3_cross_strategy_mcc.pdf` — MCC comparison across strategies.
- `rq3_learned_fusion.pdf` — learned-fusion results.
- `rq3_metric_codebert.pdf` — results combining metric and CodeBERT features.
- `rq3_metric_only.pdf` — metric-only results.
