# gold_forecasting_timeseries2

# gold_forecasting_timeseries

# GIỚI THIỆU DỰ ÁN
<!-- Phân tích thị trường, các yếu tố ảnh hưởng đến biến động giá vàng và dự báo giá trong tương lai -->
Dự án gồm các folder:

# Cách crawl data giá vàng trên yahoo finance ( nguồn: https://finance.yahoo.com/quote/GC=F/ )
có thể chạy code crawl_goldprice.py trên google colab hoặc tại môi trường ảo và chạy file (khuyến khích dùng colab cho tiện)

1. data:
- gold_5y_1d.csv : dữ liệu chứa thông tin giá mở của, đóng cửa, cao, thấp, khối lượng giao dịch trong thời gian 5 năm tính theo NGÀY từ 29/7/2020 - 25/7/2025
- df_fed_cpi_gold.csv : dữ liệu chứa thông tin giá vàng, chỉ số lạm phát, lãi suất điều hành của FED và lãi suất thực tế của fed được tính theo QUÝ trong thời gian 5 năm( gốc: FEDFUNDS.csv, CPIAUCSL.csv, gold_5y_1d.csv)
- tieu_thu_vang.csv : dữ liệu chứa thông tin về nhu cầu tiêu thụ vàng của các quốc gia qua các năm(gốc: nhu_cau_tieu_thu_vang_20_25.csv)
(nguồn gốc để tạo ra các file data trên ở trong tệp support)

2. support:
- file xử lý data: preprocessing.ipynb
- FEDFUNDS(1).csv : dữ liệu chứa thông tin lãi suất điều hành của FED
(nguồn: https://fred.stlouisfed.org/series/FEDFUNDS )
- REAINTRATREARAT5Y.csv : dữ liệu lãi suất thực (thường tỷ lệ nghịch vs giá vàng)
(nguồn: https://fred.stlouisfed.org/series/REAINTRATREARAT10Y#)
- CPIAUCSL.csv: dữ liệu chứa thông tin lạm phát (nguồn: https://fred.stlouisfed.org/series/CPIAUCSL)
- nhu_cau_tieu_thu_vang_20_25.csv : dữ liệu chứa thông tin tiêu thụ vàng qua các năm của các quốc gia 
(nguồn: https://www.gold.org/goldhub/research/gold-demand-trends gold-demand-trends-full-year-2024)

# FILE CHÍNH:
3. file phân tích và dự báo biến động giá tương lai: analysis_and_forecasting.ipynb


# Hướng phát triển trong dự án:
có thể cập nhật bổ sung dữ liệu giá vàng, lãi suất ban hành, lãi suất thực, chỉ số lạm phát theo thời gian sau này

<!-- hướng phát triển thêm -->
Phân tích kỹ thuật (Technical Analysis)
Dùng biểu đồ và chỉ báo để dự đoán xu hướng và điểm vào/ra lệnh:

Xác định xu hướng:
Xu hướng tăng, giảm hay đi ngang.
Dùng đường trung bình động (SMA, EMA).

Các mức hỗ trợ và kháng cự:
Điểm giá thường bật lại hoặc phá vỡ.

<!-- Chỉ báo kỹ thuật: -->

Bollinger Bands → biên độ biến động giá.
Fibonacci Retracement → vùng giá hồi phục tiềm năng.

Mô hình giá:
Head & Shoulders, Double Top/Bottom, Triangle, Flag, Cup & Handle...

3. Phân tích tâm lý thị trường (Market Sentiment)
Đánh giá cảm xúc và kỳ vọng của nhà đầu tư:

Tin tức & sự kiện:
Các phát biểu từ Fed, ECB, BOJ.
Tình hình địa chính trị.

Chỉ số Fear & Greed:
Đo mức độ lo sợ/tham lam của thị trường.

COT Report (Commitments of Traders):
Vị thế mua/bán ròng của các nhóm trader lớn.

Khối lượng giao dịch:
Khối lượng tăng kèm giá tăng → xu hướng mạnh.

4. Các yếu tố bổ sung
Chi phí khai thác vàng → tạo mức giá sàn.
Chính sách thuế & hạn ngạch nhập khẩu ở các quốc gia tiêu thụ lớn (Ấn Độ, Trung Quốc).
Dữ liệu lãi suất thực (real yield) — thường có quan hệ nghịch với giá vàng.
