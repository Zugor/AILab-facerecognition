# AILab-Face Recognition
Giai đoạn 1: Nhận diện có phải nhân viên của công ty hay không.


## Phân tích bài toán
* Bài toán này đã biết trước nhãn (Mã nhân viên) nên chỉ cần kiểm tra người trong ảnh có phải nhân viên đấy hay không (True hoặc False)
* Ảnh đầu vào (ImageCall) được đặt với tên có cấu trúc: `MãNhânViên_SốTT` cần được phân loại vào từng folder riêng. Có nhiều ảnh bị lỗi, mất hình, không phải ảnh người cần loại bỏ. Nhiều ảnh người bị quay ngang, lộn cần phải xoay lại.
* ...

## Giải quyết bài toán
Bằng cách tiến hành lần lượt các bước sau
### Tiền xử lý dữ liệu
* Loại bỏ các ảnh bị lỗi, mất hình, không phải ảnh người bằng phương pháp kiểm tra file hoặc thủ công
* Ảnh người xoay không đúng chiều thẳng đứng. Áp dụng 2 phương pháp sử dụng code: `Nếu chiều cao ảnh nhỏ hơn chiều ngang ảnh thì xoay ảnh 90 độ` và `Áp dụng Face Detection để detect mặt. Xoay các hướng đến khi nào detect ra mặt`

### Face Detection
* Cần phải Crop được khuôn mặt ra khỏi bức ảnh trước khi so sánh. Thuật toán phổ biến hiện nay là: Dlib, Mtcnn.

Tham khảo tài liệu:

* https://blog.vietnamlab.vn/2018/04/24/dlib-phan-2-xac-dinh-facial-landmark-voi-dlib-va-python-2/
* https://towardsdatascience.com/face-detection-neural-network-structure-257b8f6f85d1
* https://towardsdatascience.com/mtcnn-face-detection-cdcb20448ce0

Còn nữa...
