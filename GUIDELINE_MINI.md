# Mini guideline — bài làm cá nhân

> Điền nội dung này trước khi bắt đầu gán nhãn. Giữ lại các quyết định sau khi self-QC.

## Định nghĩa lớp

| Lớp | Định nghĩa của bạn | Ví dụ/điểm phân biệt |
| --- | --- | --- |
| `car` |Xe ô tô chở người thông thường, có kích thước và thiết kế thân xe dạng xe con. | Sedan, hatchback, SUV và crossover.|
| `truck` | Xe tải được thiết kế chủ yếu để vận chuyển hàng hóa.|Xe tải thùng, xe tải nhỏ, xe tải lớn. |
| `bus` |Phương tiện chở nhiều hành khách, có thân xe lớn và thiết kế đặc trưng của xe buýt.| Xe buýt đô thị, xe buýt đường dài.|
| `van` | Xe có khoang thân tương đối cao và kín, thường dùng để chở người hoặc hàng hóa, có hình dáng dạng van/minivan.|Minivan, passenger van, cargo van. |

## Quy tắc chung

- Box bám sát vật thể nghĩa là: Bounding box phải bao quanh toàn bộ phần vật thể nhìn thấy, không lấy quá nhiều nền xung quanh.
- Vật thể bị che khuất: Chỉ gán nhãn khi có đủ đặc điểm để xác định đó là một phương tiện thuộc một trong bốn lớp.
- Vật thể bị cắt bởi rìa ảnh: Vẫn gán nhãn nếu phần nhìn thấy đủ để xác định lớp; box giới hạn theo phần vật thể nằm trong ảnh.
- Vật thể rất nhỏ/mơ hồ:  Không đoán lớp khi không đủ thông tin để phân biệt. Ưu tiên tính nhất quán với schema.

## Ghi lại quyết định cho ít nhất ba ca mơ hồ

| Ảnh | Tình huống | Quyết định cuối | Lý do theo schema |
| --- | --- | --- | --- |
| `drive_027` | Xe có hình dáng nằm giữa car và van| Chờ xác nhận ảnh và nhãn đã chọn| Phân biệt theo cấu trúc thân xe và đặc điểm thiết kế|
| `drive_034` | Xe tải nhỏ có kích thước gần giống van|Chờ xác nhận ảnh và nhãn đã chọn | Phân biệt theo đặc điểm xe tải chở hàng|
| `drive_019` |Phương tiện bị che khuất, khó nhận diện | Chờ xác nhận ảnh và nhãn đã chọn|Chỉ gán lớp khi đủ đặc điểm nhận diện |
