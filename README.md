# Adventure-Works-Analyst
Provide significant facts about business performance and determine the best sellers product and the best customer across all product in order to make a strategy for expansion market.  
# Design thinking template
**STEP 1: EMPATHIZE**
**_1. Stakeholder Challenge_**
'- Cần có cái nhìn tổng quan về tình hình kinh doanh chung, các chỉ tiêu kinh doanh chung
+ Dữ liệu về doanh số tháng/quý có đạt được mục tiêu đặt ra không? Nguyên nhân? Cách cải thiện tình hình kinh doanh ra sao
+ Dữ liệu có thiếu các thông tin chi tiết nào không? (Các bảng rời rạc với nhau...) => khó khăn khi theo dõi các thông tin chi tiết về hiệu suất của các kênh bán hàng, sản phẩm, phân khúc khách hàng..
- Stakeholder khó khăn khi theo dõi tiến độ doanh thu so với mục tiêu theo thời gian để đốc thúc nhân viên.
- Mục tiêu mở rộng thị trường trong những năm tiếp theo:
+ Tập trung vào những khách hàng (company) có tốt nhất (company's best customers)
+ Thị trường nào đang đem lại những khách hàng tiềm năng và có thể phát triển hơn nữa
**_2. Dashboard Goal_**
- Cung cấp thông tin về chung về doanh thu qua 4 năm (tổng doanh thu, tốc độ tăng trưởng,…)
1. Theo dõi doanh số bán hàng: Theo dõi và so sánh doanh số thông qua các chỉ số về thời gian, khu vực, nhân viên, sản phẩm và các yếu tố khác => Đưa ra được các điểm mạnh, điểm yếu trong hoạt động bán hàng.
2. Phân tích về sản phẩm và khách hàng: Phân tích hiệu suất bán hàng theo từng loại sản phẩm và theo từng khách hàng
3. Đánh giá mức hiệu quả của các chiến dịch tiếp thị: Đánh giá các chiến dịch tiếp thị như chiến dịch quảng cáo, khuyến mãi và chương trình cho các đối tượng phân khúc khách hàng khác nhau, đặc biệt là các khách hàng trung thành
=> Cơ sở ra quyết định về chiến lược kinh doanh mở rộng thị trường
**_3. Tìm hiểu về đối tượng sử dụng báo cáo_**
Manager, Director => Đưa ra các quyết định mang tính chiến lược
**_4. Tìm hiểu dataset_**
'- Dữ liệu sử dụng: Sales (Fact table: SalesTable)
+Dimension: Customer, Location(Country and Continent), Product, Shipdate, Sale reason,...
+ Measure: Order Quatity, Line total, Unit Price, Unit Price Discount, Freight, SalesYTD, SalesLastYear...
**_5. Đánh giá và làm sạch dataset_**
- Bảng SalesTable: Cột Status chỉ hiện 1 giá trị là 5 - các đơn hàng đã được giao => remove
- Bảng Customer: show territory chỉ 1 gtri 1 => remove
**STEP 2: DEFINE POINT OF VIEW**
Sử dụng logic tree:
1. Tình hình kinh doanh chung? 
- Total sales, Total orders, YoY Sales, YoY orders
- Sales by customer, by product, by market, by reason..
2. Nghiên cứu mở rộng thị trường: 
- Các thị trường nào nằm trong Top doanh thu cao nhất? Thị trường nào là tiềm năng? 
- Trong các thị trường đó, có sản phẩm nào là sản phẩm chủ yếu được tiêu thụ không? Có sản phẩm nào mang lại doanh thu thấp ở thị trường này nhưng có số liệu tốt ở thị trường hay không? Các yếu tố như tỷ lệ chiết khấu, shipmethod, chi phí vận chuyển... có ảnh hưởng gì đến doanh số của các sản phẩm ở thị trường đó không? Lý do mua hàng chủ yếu của khách hàng tại các thị trường này là gì?
**STEP 3: IDEATE**
**_1. Layer 0 dimension:_** Scorecard
  Score card:Total sales, Total order, Total customer, %Sale YoY, Card value, CAGR
**_2. Layer 1 dimension_**
- Total sales by year
- Sales = Sales by month 
            = Sale by category
            = Sale by market
            = Price * Quantity
            = Reason Type
- Expense = Expense by category
                 = Expense by market
=> Profit by year, by market, by category
**_3. Layer 2 dimension_**
Sale by market: 
- Total sale, profit margin by country
- Các chỉ số: AVG shipping cost, sales by category, sales by discount and nondiscount, sale per order, CAGR in each continent
**_4. Table_**
'- Total sale, profit by country
