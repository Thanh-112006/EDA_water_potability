# Machine Learning - Phân Tích & Dự Đoán

Repository này chứa mã nguồn và tài liệu cho bài tập Machine Learning , tập trung vào hai mốc giải quyết các bài toán trọng tâm là: **Phân loại (Classification)** và **Hồi quy (Regression)**. 

---

##  Cấu trúc thư mục

```text
├── data/
│   ├── insurance.csv            # Dataset cho bài toán Hồi quy (dự đoán chi phí y tế)
│   └── water_potability.csv     # Dataset cho bài toán Phân loại (chất lượng nước)
├── EDA.ipynb                    # Notebook: EDA & Mô hình Classification (Potability)
├── regression.ipynb             # Notebook: Phân tích & Mô hình Regression (Insurance)
└── README.md                    # Tài liệu mô tả dự án
```

---

##  Project 1: Đánh Giá Chất Lượng Nước (Classification)

###  Mục tiêu
Khám phá dữ liệu và xây dựng mô hình dự đoán liệu một nguồn nước có an toàn để uống hay không dựa trên các chỉ số hóa học.
*   **Dataset:** [Water Potability - Kaggle](https://www.kaggle.com/adityakadiwal/water-potability)
*   **File xử lý chính:** `EDA.ipynb`

###  Đặc trưng Dữ liệu (Features)
*   **Độ pH:** Đánh giá sự cân bằng axit-bazơ (pH lý tưởng: 6.5 - 8.5).
*   **Độ cứng (Hardness):** Đo lường tính chất vật lý (khả năng hỗ trợ cây phát triển).
*   **Tổng chất rắn hòa tan (Solids - TDS):** Đo tổng lượng chất rắn phân tán, mức an toàn thường < 1000 mg/l.
*   **Cloramin (Chloramines):** Chất khử trùng (ngưỡng an toàn < 4 ppm).
*   **Sunfat (Sulfate):** Chất khử trùng (mức an toàn lên tới 2 ppm).
*   **Độ dẫn điện (Conductivity):** Mật độ ion hóa (giới hạn an toàn < 400 μS/cm).
*   **Carbon hữu cơ (Organic_carbon):** Lượng phân hủy hữu cơ.
*   **Trihalomethanes (Trihalomethanes):** Phụ phẩm hình thành sau quá trình xử lý với clo.
*   **Độ đục (Turbidity):** Mức độ hấp thụ dạng hạt trong nước.
*   ** Target (Potability):** Khả năng uống được. `1` = Uống được, `0` = Không uống được.

###  Kỹ thuật & Thuật toán
-   **Tiền xử lý & EDA:** Fill missing values, Xử lý điểm dị biệt (Outliers) bằng phương pháp Capping/Winsorization (IQR), Trực quan Heatmap, Kiểm định giả thuyết Pearson (Hypothesis Testing).
-   **Model:** StandardScaler, Logistic Regression, Random Forest (kèm theo đánh giá Feature Importance).
-   **Evaluation:** Accuracy, Precision, Recall, F1-Score.

---

##  Project 2: Dự Đoán Chi Phí Bảo Hiểm Y Tế (Regression)

###  Mục tiêu
Phân tích và xây dựng mô hình dự đoán mức chi phí bảo hiểm mà khách hàng cần trả dựa trên các yếu tố rủi ro và nhân khẩu học (tuổi, chỉ số BMI, hút thuốc,...).
*   **File xử lý chính:** `regression.ipynb`

### 🛠 Kỹ thuật & Thuật toán
-   **Phân tích Data sâu:** Đánh giá độ lệch của Target Distribution (Shapiro-Wilk, Kolmogorov-Smirnov test, Q-Q Plot, Skewness, Kurtosis).
-   **Feature Engineering:** Encoding các trường categories dạng category bằng Dummy Variables. Biến đổi hàm mục tiêu bằng phương pháp Box-Cox (chuẩn hóa dữ liệu y).
-   **Model (Cross-Validation + Parameter Tuning với GridSearchCV):**
    -   Vanilla Linear Regression
    -   Polynomial Regression
    -   Regularized Regression (Ridge, Lasso)
    -   ElasticNetCV
-   **Evaluation:** KFold Validation, RMSE, MAE, R-Squared ($R^2$). 
-   **Insights:** Xác định yếu tố quyết định "Hút thuốc" (Smoking) đối với chi phí bảo hiểm thông qua báo cáo tổng kết trong Notebook.

---

##  Hướng Dẫn 
1. Clone repository hoặc tải toàn bộ thư mục về máy.
2. Cài đặt các package cần thiết, sử dụng lệnh:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn scipy
   ```
3. Mở và chạy (Run All) các file Jupyter Notebook (`EDA.ipynb` hoặc `regression.ipynb`) bằng VS Code hoặc Jupyter Lab/Notebook để xem báo cáo cũng như quy trình pipeline một cách chi tiết nhất.
