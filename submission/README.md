# Day21 Submission - 2A202600964 - Doan Thi Thu Linh

## GitHub Repo
https://github.com/ThuLinh3009/Day21_2A202600964_DoanThiThuLinh

## Cloud Provider: AWS
- S3 bucket: `mlops-lab-day21`
- EC2: `35.175.185.157` (Ubuntu 26.04, t3.micro, ap-southeast-1)

---

## Danh sách Screenshots

| File | Nội dung |
|------|----------|
| S1b_mlflow_runs_table.jpg | Bước 1 — MLflow runs table (8 experiments, best accuracy=0.678) |
| S1c_mlflow_compare_plot.jpg | Bước 1 — MLflow parallel coordinates plot so sánh hyperparameters |
| S2a_dvc_push_3files.jpg | Bước 2 — DVC push 3 files lên S3 thành công |
| S2c_github_secrets_5keys.jpg | Bước 2 — 5 GitHub Secrets đã cấu hình |
| S3_pipeline1_all_jobs_success.jpg | Bước 2 — MLOps Pipeline #1: Unit Test→Train→Eval→Deploy ✅ |
| S4a_eval_accuracy_0678.jpg | Bước 2 — Eval gate: Accuracy 0.6780 >= 0.65 PASSED |
| S4b_api_predict_result.jpg | Bước 2 — API /predict trả về prediction=0, label=thap |
| S5a_buoc3_dvc_push_data.jpg | Bước 3 — add_new_data.py: 2998→5996 mẫu + dvc push |
| S5b_pipeline2_accuracy_0756.jpg | Bước 3 — MLOps Pipeline #2: accuracy 0.7560 >= 0.65 PASSED |

---

## Kết quả so sánh accuracy (Mục 3.6)

| Chỉ số   | Bước 2 (2998 mẫu) | Bước 3 (5996 mẫu) |
|----------|-------------------|-------------------|
| accuracy | 0.6780            | 0.7560            |
| f1_score | 0.6767            | ~0.755            |

Thêm dữ liệu từ train_phase2 (2998 mẫu mới) giúp accuracy tăng từ 0.6780 lên 0.7560 (+11.5%).
Pipeline tự động trigger khi push file `.dvc` — không cần thao tác thủ công.
