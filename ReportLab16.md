Báo cáo Lab 16:

Trong quá trình thực hiện phần 1-3, do chính sách của AWS gắt gao nên tài khoản của em không xin cấp được vCPU g4dn.xlarge, đồng thời các dòng máy CPU cao (r5, t3.medium) đều bị từ chối với lỗi "Not eligible for Free Tier".
Vậy nên em đã xử lý sự cố thiết lập thành công mô hình với cấu hình t3.micro để triển khai phương án thay thế phần 7 (Machine Learning Benchmark) chạy giả lập trực tiếp thông qua SSH Bastion Host.
Kết quả Benchmark tốt: AUC-ROC đạt 0.9367, thời gian training siêu nhanh. Tốc độ Inference ở máy con này là ±1ms / 1 row mẫu.
Sau khi lấy xong Metrics và chụp ảnh Billing để xác nhận $0.00 do Free Plan. Em đã dọn dẹp hệ thống bằng terraform destroy. Mọi file code đã được giải nén và sửa lại trong tệp đính kèm.