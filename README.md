# NWC204
Computer Networking
Link quizlet ôn FE: https://quizlet.com/user/tkaceneversay/folders/nwc?funnelUUID=5239f0c8-3348-449e-bd31-54c38a5c4ec2

```mermaid
stateDiagram
    [*] --> New_Reservation : Khách hàng tạo đơn
    New_Reservation --> Under_Review : Nhân viên kiểm tra
    Under_Review --> Waiting_for_Manager_Approval : Gửi quản lý phê duyệt
    Waiting_for_Manager_Approval --> Quote_Sent : Quản lý phê duyệt
    Waiting_for_Manager_Approval --> Cancelled : Quản lý từ chối
    Quote_Sent --> Waiting_for_Customer_Confirmation : Khách hàng xác nhận
    Quote_Sent --> Cancelled : Khách hàng từ chối
    Waiting_for_Customer_Confirmation --> Paid : Khách hàng thanh toán
    Waiting_for_Customer_Confirmation --> Cancelled : Khách hàng không thanh toán
    Paid --> Confirmed_Processed : Nhân viên gửi thông tin
    Confirmed_Processed --> Trip_Started : Chuyến đi bắt đầu
    Trip_Started --> Fish_Ordered : Khách đặt mua cá
    Fish_Ordered --> Cancelled : Không đủ tiền đặt cọc
    Fish_Ordered --> Waiting_for_Delivery : Nhân viên cập nhật giao hàng
    Waiting_for_Delivery --> Cancelled : Khách hủy nhận cá (mất cọc)
    Waiting_for_Delivery --> Delivered : Giao hàng & thanh toán
    Waiting_for_Delivery --> Refunded : Cá lỗi, hoàn tiền cọc
    Delivered --> [*]
    Cancelled --> [*]
    Refunded --> [*]
