# dataset
The dataset is downloaded from kaggle.com and is available for download at:
https://www.kaggle.com/adityakadiwal/water-potability
# EDA_water_potability
Access to Safe drinking water is eassently a global issue. The World Health Organization (WHO) estimates that half of all people in the world are affected by the lack of safe drinking water. With this assesment, we will explore the data and look for patterns in the data to analyze if the given data is a good indicator of safe drinking water.
# Phân tích Đặc trưng Dữ liệu (Features Description)
# Độ pH
Độ pH là một thông số quan trọng trong việc đánh giá sự cân bằng axit-bazơ và là chỉ số cho biết trạng thái axit hay kiềm của nước. Tổ chức Y tế Thế giới (WHO) khuyến nghị giới hạn pH cho phép tối đa đối với nước uống là từ 6.5 đến 8.5. Trong tập dữ liệu này, phạm vi khảo sát thực tế dao động từ 6.52 đến 6.83, hoàn toàn nằm trong ngưỡng tiêu chuẩn an toàn của WHO.
# Độ cứng (Hardness)
Độ cứng là thước đo các tính chất vật lý của nước, cụ thể là khả năng của nước trong việc hỗ trợ rễ và lá cây phát triển. Mức độ cứng càng thấp thì khả năng hỗ trợ cho rễ và lá cây càng tốt.
# Tổng chất rắn hòa tan (Solids - TDS)
Chỉ số TDS là thước đo tổng lượng chất rắn có trong nước. Nước có giá trị TDS cao cho thấy nguồn nước đó bị khoáng hóa mạnh. Theo quy định cho mục đích nước uống, giới hạn mong muốn đối với TDS là 500 mg/l và giới hạn tối đa cho phép là 1000 mg/l.
# Cloramin (Chloramines)
Clo và cloramin là những chất khử trùng chính được sử dụng phổ biến trong các hệ thống cấp nước công cộng. Cloramin thường được hình thành khi người ta thêm amoniac vào clo trong quá trình xử lý nước uống. Mức độ clo lên tới 4 miligam trên lít (mg/L hoặc 4 ppm) được coi là ngưỡng an toàn trong nước uống.
# Sunfat (Sulfate)
Tương tự như Clo, Sulfate cũng là một chất khử trùng phổ biến được sử dụng trong các hệ thống cấp nước công cộng. Nồng độ sulfate lên tới 2 miligam trên lít (mg/L hoặc 2 ppm) được coi là mức an toàn cho nước uống.
# Độ dẫn điện (Conductivity)
Nước tinh khiết thực chất là một chất cách điện tốt chứ không phải là chất dẫn điện. Sự gia tăng nồng độ các ion, hay nói cách khác là lượng chất rắn hòa tan trong nước, sẽ làm tăng độ dẫn điện của nó. Độ dẫn điện (EC) đo lường quá trình ion hóa của một dung dịch để truyền dòng điện. Theo tiêu chuẩn của WHO, giá trị EC an toàn không được vượt quá 400 μS/cm.
# Carbon hữu cơ (Organic_carbon)
Tổng lượng Carbon hữu cơ (TOC) trong nguồn nước có nguồn gốc từ các chất hữu cơ tự nhiên đang phân hủy (NOM) cũng như từ các nguồn tổng hợp nhân tạo. TOC là thước đo tổng lượng carbon có trong các hợp chất hữu cơ của nước tinh khiết. Theo tiêu chuẩn của Cơ quan Bảo vệ Môi trường Hoa Kỳ (US EPA), mức TOC < 2 mg/L được áp dụng cho nước đã qua xử lý/nước uống, và < 4 mg/L đối với nước nguồn dùng để xử lý.
# Trihalomethanes (Trihalomethanes)
THMs là các hóa chất phụ phẩm có thể được tìm thấy trong nước đã qua xử lý bằng clo. Nồng độ THMs trong nước uống thay đổi linh hoạt tùy thuộc vào lượng chất hữu cơ có trong nước, lượng clo cần thiết để xử lý và nhiệt độ của nước tại thời điểm đó. Nồng độ THM lên tới 80 ppm được coi là an toàn trong nước uống.
# Độ đục (Turbidity)
Độ đục là thước đo khả năng hấp thụ các vật chất dạng hạt của nước. Chỉ số độ đục càng thấp thì khả năng nước hấp thụ các vật chất dạng hạt càng cao.  
# Khả năng uống được (Potability - Biến mục tiêu)
Đây là biến mục tiêu của tập dữ liệu, cho biết nước có an toàn cho con người sử dụng trực tiếp hay không. Trong đó, giá trị 1 có nghĩa là Uống được (Potable) và 0 có nghĩa là Không uống được (Not potable).
