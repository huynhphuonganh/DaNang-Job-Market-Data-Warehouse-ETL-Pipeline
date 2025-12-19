📊 DaNang-Job-Market-Data-Warehouse-ETL-Pipeline

Hệ thống ETL & Data Warehouse phục vụ phân tích thị trường việc làm tại Đà Nẵng

🧭 Giới thiệu

DaNang-Job-Market-Data-Warehouse-ETL-Pipeline là dự án xây dựng hệ thống thu thập – xử lý – lưu trữ – phân tích dữ liệu tuyển dụng từ nhiều nguồn khác nhau.
Dự án hướng tới việc tạo ra một nền tảng dữ liệu tập trung, có khả năng mở rộng, phục vụ các bài toán phân tích thị trường lao động và nhu cầu kỹ năng tại Đà Nẵng.

🏗️ Kiến trúc tổng thể

Kiến trúc hệ thống tuân theo mô hình Data Engineering tiêu chuẩn:

Data Source → Ingestion & Processing → Data Staging → Data Warehouse → Data Mart → Analytics

Data Source: Website tuyển dụng (DaNangJob, DaNang43)

Ingestion & Processing: Web scraping, làm sạch và chuẩn hóa dữ liệu

Data Staging: Lưu trữ dữ liệu trung gian dưới dạng JSON trên GitHub

Data Warehouse: PostgreSQL triển khai trên Google Cloud Platform

Data Mart: Dữ liệu tổng hợp phục vụ các nhu cầu phân tích thường xuyên

Analytics: Khai thác dữ liệu cho báo cáo và dashboard (SmartCV)

⚙️ Quy trình triển khai
1. Thiết kế dữ liệu

Xây dựng ERD (Entity Relationship Diagram) làm nền tảng cho toàn bộ hệ thống

Xác định rõ các entity chính và mối quan hệ giữa chúng

2. Thu thập và tiền xử lý dữ liệu

Crawl dữ liệu tuyển dụng bằng Python (Requests, BeautifulSoup)

Làm sạch dữ liệu, chuẩn hóa định dạng và loại bỏ dữ liệu không hợp lệ

Lưu dữ liệu trung gian dưới dạng JSON để dễ kiểm soát và versioning

3. ETL vào Data Warehouse

Xây dựng pipeline tự động load dữ liệu từ GitHub vào PostgreSQL trên GCP

Áp dụng schema theo ERD nhằm đảm bảo tính nhất quán dữ liệu

4. Xây dựng Data Mart và phân quyền

Tạo các Data Mart phục vụ:

Phân tích thị trường việc làm Đà Nẵng

Phân tích yêu cầu kỹ năng theo ngành/nghề

Thiết kế cơ chế phân quyền truy cập dữ liệu theo mục đích sử dụng

🛠️ Công nghệ sử dụng

Ngôn ngữ: Python

Web Scraping: Requests, BeautifulSoup

Định dạng dữ liệu: JSON

Quản lý mã nguồn & Staging: GitHub

Cơ sở dữ liệu: PostgreSQL

Nền tảng Cloud: Google Cloud Platform

Mô hình dữ liệu: ERD

Phân tích & BI: SmartCV

🎯 Giá trị mang lại

Chuẩn hóa dữ liệu tuyển dụng từ nhiều nguồn khác nhau

Xây dựng nền tảng dữ liệu sẵn sàng cho phân tích và mở rộng

Hỗ trợ phân tích xu hướng tuyển dụng và nhu cầu kỹ năng tại Đà Nẵng

Mô phỏng quy trình Data Engineering thực tế trong doanh nghiệp

📌 Kết luận

Dự án thể hiện cách tiếp cận bài bản trong việc xây dựng ETL Pipeline và Data Warehouse, từ thiết kế dữ liệu đến khai thác phân tích.
Đây là nền tảng quan trọng cho các ứng dụng data-driven decision making trong phân tích thị trường lao động.
