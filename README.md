# Insurance Claim Fraud Detection & Risk Triage

An end-to-end Machine Learning, SHAP Explainability, and AI Risk Triage system for auto insurance claims.

---

## Deliverables & Generated Artifacts

### 📄 Executive & Technical PDF Reports
- **Full Comprehensive Report (PDF):** [`Insurance_Claim_Fraud_Detection_Full_Report.pdf`](file:///c:/Users/parth/Downloads/projecttt/Insurance_Claim_Fraud_Detection_Full_Report.pdf) (Complete executive audit, 18+ metrics, cost curves, confusion matrices, SHAP analysis, and LLM forensics)
- **System Architecture & Design Report (PDF):** [`System_Architecture_and_Design_Report.pdf`](file:///c:/Users/parth/Downloads/projecttt/System_Architecture_and_Design_Report.pdf) (Dedicated engineering specification, 5-layer pipeline architecture, scalability benchmarks, and regulatory compliance)

### 📊 Visualizations Directory (`visualizations/`)
All high-resolution visualization charts are centralized in [`visualizations/`](file:///c:/Users/parth/Downloads/projecttt/visualizations/):
1. [`01_system_architecture_diagram.png`](file:///c:/Users/parth/Downloads/projecttt/visualizations/01_system_architecture_diagram.png) - Publication-grade System Architecture Blueprint
2. [`02_model_performance_comparison.png`](file:///c:/Users/parth/Downloads/projecttt/visualizations/02_model_performance_comparison.png) - Multi-Metric Model Comparison Bar Chart
3. [`03_confusion_matrices_grid.png`](file:///c:/Users/parth/Downloads/projecttt/visualizations/03_confusion_matrices_grid.png) - Side-by-Side Confusion Matrices for All 5 Models
4. [`04_roc_and_pr_curves.png`](file:///c:/Users/parth/Downloads/projecttt/visualizations/04_roc_and_pr_curves.png) - Receiver Operating Characteristic & Precision-Recall Curves
5. [`05_probability_calibration_reliability.png`](file:///c:/Users/parth/Downloads/projecttt/visualizations/05_probability_calibration_reliability.png) - Probability Calibration Reliability Curves
6. [`06_shap_global_feature_importance.png`](file:///c:/Users/parth/Downloads/projecttt/visualizations/06_shap_global_feature_importance.png) - Portfolio-Wide SHAP Feature Importance Ranking
7. [`07_five_tier_risk_distribution.png`](file:///c:/Users/parth/Downloads/projecttt/visualizations/07_five_tier_risk_distribution.png) - 5-Tier Operational Risk Funnel & Routing Breakdown
8. [`08_cost_asymmetry_tradeoff.png`](file:///c:/Users/parth/Downloads/projecttt/visualizations/08_cost_asymmetry_tradeoff.png) - False Negative vs False Positive Cost Optimization Curve

---

## System Architecture

```
projecttt/
├── fraud_oracle.csv                           # Historical Insurance Claims Dataset (15,420 claims)
├── demo_triage.py                             # Interactive claim evaluator demo
├── generate_metrics_report.py                 # 18+ metric evaluation engine
├── generate_pdf_reports.py                    # Multi-page PDF report compiler (ReportLab)
├── visualizations/                            # Centralized high-res metric & architecture charts
└── insurance_risk_triage/                     # Core system package
    ├── config.py                              # Features, paths, 5-tier risk configurations
    ├── data_loader.py                         # Stratified data partitioning & schema validation
    ├── preprocessor.py                        # ColumnTransformer (StandardScaler + OneHotEncoder)
    ├── train_models.py                        # Benchmark XGBoost, SVM, Random Forest, Logistic Regression
    ├── evaluate_models.py                     # Performance evaluation, ROC & PR curve generator
    ├── shap_explainer.py                      # Global & local SHAP feature attribution engine
    ├── risk_engine.py                         # 5-Tier Risk Decision Engine + Heuristic Rule Overlays
    ├── llm_risk_analyzer.py                   # LLM Forensic Report Generator (Gemini/OpenAI + Built-in AI)
    ├── pipeline.py                            # Unified end-to-end inference pipeline
    └── artifacts/
        ├── models/                            # Serialized joblib pipelines & champion model
        ├── plots/                             # Generated plots
        └── reports/                           # Benchmark CSV & evaluation JSON summaries
```

---

## 5-Tier Risk Decision Engine

| Risk Tier | Fraud Probability | Workflow Queue | Action Directive |
| :--- | :--- | :--- | :--- |
| **Very Low** | `< 10%` | Automated Payment Clearance | Automated Straight-Through Processing (STP) - Fast Track Approval |
| **Low** | `10% - 25%` | Standard Claims Adjuster Queue | Standard Claim Processing - Routine Desk Assessment |
| **Medium** | `25% - 55%` | Senior Claims Adjuster Queue | Manual Claim Review - Secondary Audit & Invoice Verification |
| **High** | `55% - 80%` | Fraud Triage & Field Audit Unit | Priority Investigation - Field Adjuster Verification & Witness Cross-Check |
| **Very High** | `>= 80%` | Special Investigation Unit (SIU) | Immediate SIU Referral - Forensic Audit & Legal Hold |

---

## Quick Start Commands

```bash
# 1. Run the Full Model Training & Triage Pipeline
python main.py

# 2. Run Interactive Claim Scenarios Demo
python demo_triage.py

# 3. Recompute All 18+ Metrics & Confusion Matrices
python generate_metrics_report.py

# 4. Re-generate Architecture Blueprints & Cost Tradeoff Charts
python generate_architecture_diagram.py

# 5. Re-compile Both Production PDF Reports
python generate_pdf_reports.py
```

