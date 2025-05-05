#  Random Forest vs Decision Tree: Ai chống Overfitting tốt hơn? 

## Giới thiệu 

Trong bài toán phát hiện gian lận thẻ tín dụng – nơi dữ liệu cực kỳ **mất cân bằng** (class gian lận chỉ chiếm ~0.2%) – việc đánh giá mô hình không thể chỉ dựa vào accuracy.

Trong dự án này, chúng tôi:

- So sánh **Decision Tree** và **Random Forest** trên tập dữ liệu thực tế từ Kaggle.
- Đánh giá mô hình bằng các chỉ số **precision**, **recall** và đặc biệt là **F1-score** cho class gian lận.
- Trực quan hóa độ chính xác và overfitting thông qua biểu đồ.
- Giải thích vì sao Random Forest ít bị overfit hơn và hiệu quả hơn trong các bài toán thực tế.

> Đây là một ví dụ thực tiễn cho thấy tầm quan trọng của **ensemble learning** trong việc cải thiện độ ổn định và độ chính xác của mô hình học máy.

---

##  Dữ liệu sử dụng 

- **Nguồn**: [Credit Card Fraud Detection - Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Mô tả**: Hơn 284.000 giao dịch, với ~0.2% là gian lận. Các đặc trưng từ V1–V28 đã được PCA hóa để ẩn danh.

---

## Môi trường thực thi 

- Python >= 3.8
- Thư viện chính:
  - `scikit-learn`
  - `pandas`
  - `matplotlib`, `seaborn`
  - `joblib` (lưu mô hình)

Cài đặt nhanh:

```bash
pip install -r requirements.txt
