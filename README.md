# 📊 DaNang-Job-Market-Data-Warehouse-ETL-Pipeline
Hệ thống ETL & Data Warehouse phục vụ phân tích thị trường việc làm Đà Nẵng

## 1. Introduction

DaNang-Job-Market-Data-Warehouse-ETL-Pipeline là dự án xây dựng hệ thống ETL & Data Warehouse nhằm thu thập, xử lý và phân tích dữ liệu thị trường việc làm tại Đà Nẵng.
Mục tiêu chính là tạo ra **nguồn dữ liệu tập trung – có cấu trúc **– sẵn sàng cho phân tích như xu hướng tuyển dụng, nhu cầu kỹ năng và báo cáo phục vụ ra quyết định.

---

## 2. Tổng quan quy trình thực hiện

Quy trình tổng thể của dự án gồm các bước chính (theo sơ đồ):

<img width="1920" height="1080" alt="Bản sao của What is (1)" src="https://github.com/user-attachments/assets/b02b21bb-ea5c-4cfa-9e40-0817bf6b6498" />


- **Data Source:** Website tuyển dụng (DaNangJob, DaNang43)

- **Ingestion & Processing:** Web scraping, làm sạch và chuẩn hóa dữ liệu

- **Data Staging:** Lưu trữ dữ liệu trung gian ở dạng JSON trên GitHub

- **Data Warehouse**: PostgreSQL triển khai trên Google Cloud Platform

- **Data Mart:** Dữ liệu tổng hợp phục vụ phân tích thường xuyên

---

## 3. Quy trình thực hiện
🔹 **Bước 1:** Thiết kế Database

- Xây dựng ERD (Entity Relationship Diagram) trước khi làm dữ liệu

- Xác định các bảng chính: Job, Company, Skill, HR, Recruitment Process...

🔹**Bước 2:** Web Scraping & Ingestion

- Sử dụng Python (Requests + BeautifulSoup) để crawl dữ liệu từ: DaNangJob và DaNang43

- Thực hiện tiền xử lý cơ bản: Làm sạch text, chuẩn hóa định dạng khớp database

- Lưu dữ liệu trung gian ở dạng JSON trên GitHub (đóng vai trò Data Staging)

🔹**Bước 3:** Pipeline load tự động vào Data Warehouse

- Xây dựng pipeline tự động: Load dữ liệu từ GitHub --> Đổ vào PostgreSQL trên Google Cloud --> Đảm bảo dữ liệu đúng schema theo ERD đã thiết kế

🔹 **Bước 4:** Xây dựng  Data Mart

- Tạo Data Mart từ Data Warehouse để phục vụ các nhu cầu phân tích thường xuyên:

+ Phân tích thị trường việc làm Đà Nẵng

+ Phân tích yêu cầu kỹ năng theo ngành/nghề

- Thiết kế phân quyền truy cập theo mục đích sử dụng dữ liệu

---

## 4. Công cụ sử dụng

Python: Requests, BeautifulSoup

Data Format: JSON

Version Control / Staging: GitHub

Database: PostgreSQL

Cloud: Google Cloud Platform

Data Modeling: ERD

Analytics: SmartCV / BI tools

---

## 5. Conclusion

Dự án này mô phỏng một pipeline ETL & Data Warehouse hoàn chỉnh từ thu thập dữ liệu thực tế đến phân tích.
Nó giúp chuyển đổi dữ liệu thô từ các website tuyển dụng thành insight có giá trị, phục vụ phân tích thị trường lao động và hỗ trợ ra quyết định dựa trên dữ liệu.
