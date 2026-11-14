# Khung nghiên cứu: nền tảng số và giá trị trong chuỗi lúa gạo

## Đề tài gợi ý

**Mô phỏng tác động của nền tảng RiceTrace đến khoản thu từ bán lúa và chi phí giao dịch của hợp tác xã tại Thoại Sơn, An Giang.**

Đây là khung cho một nghiên cứu tình huống có mô phỏng. Kết quả mặc định trên website là giả định minh họa, không phải bằng chứng rằng nền tảng đã làm tăng thu nhập ngoài thực tế.

## Câu hỏi và mục tiêu nghiên cứu

**Câu hỏi nghiên cứu:** Trong các giả định của kịch bản, tỷ lệ bán trực tiếp qua RiceTrace, mức chênh lệch giá và chi phí giao dịch làm thay đổi khoản thu từ bán lúa của hợp tác xã ra sao? Mức phí giao dịch đó ảnh hưởng thế nào đến chi phí mua hàng của doanh nghiệp?

**Mục tiêu:**

- So sánh khoản thu sau chi phí bán hàng giữa kênh truyền thống và kịch bản kết hợp kênh truyền thống với RiceTrace.
- Phân tích độ nhạy của kết quả theo tỷ lệ sản lượng bán qua nền tảng, mức chênh lệch giá và chi phí giao dịch.
- Minh họa phần hoa hồng nền tảng trong chi phí mua hàng của doanh nghiệp.

## Mô hình tính toán

Các biến trong website dùng những đơn vị sau:

| Ký hiệu | Ý nghĩa | Đơn vị |
| --- | --- | --- |
| `Q` | Sản lượng của hợp tác xã trong vụ | tấn |
| `P₀` | Giá bán tham chiếu theo kênh truyền thống | VND/kg |
| `s` | Tỷ lệ sản lượng bán qua RiceTrace | Từ 0 đến 1 |
| `p` | Mức chênh giá trực tiếp so với giá tham chiếu | Từ 0 đến 1 |
| `C₀`, `C₁` | Chi phí bán hàng mỗi tấn ở kênh truyền thống và RiceTrace | VND/tấn |
| `r` | Tỷ lệ hoa hồng do doanh nghiệp trả | Từ 0 đến 1 |

Giá tham chiếu được đổi sang VND/tấn bằng `1.000 × P₀`.

**Khoản thu theo kênh truyền thống:**

`Y₀ = Q × (1.000 × P₀ − C₀)`

**Khoản thu ở kịch bản RiceTrace:** phần sản lượng chưa bán qua nền tảng vẫn dùng giả định của kênh truyền thống:

`Y₁ = Q × [(1 − s) × (1.000 × P₀ − C₀) + s × (1.000 × P₀ × (1 + p) − C₁)]`

**Thay đổi khoản thu:** `ΔY = Y₁ − Y₀`; tỷ lệ thay đổi là `ΔY / Y₀ × 100%` khi `Y₀ ≠ 0`.

**Chi phí mua hàng của doanh nghiệp trong kịch bản RiceTrace:**

`B₁ = Q × (1 − s) × 1.000 × P₀ + Q × s × 1.000 × P₀ × (1 + p) × (1 + r)`

**Mức chênh giá hòa vốn cho phần bán trực tiếp:**

`p* = (C₁ − C₀) / (1.000 × P₀)`

`p*` là mức chênh giá cần có để khoản thu trên mỗi tấn bán qua nền tảng bằng khoản thu trên mỗi tấn qua kênh truyền thống, theo các chi phí đã nhập.

## Kịch bản mẫu trên website

| Tham số | Giá trị mặc định | Ghi chú |
| --- | ---: | --- |
| Sản lượng vụ | 100 tấn | Giả định minh họa |
| Giá tham chiếu | 6.500 VND/kg | Không phải báo giá thị trường |
| Tỷ lệ sản lượng qua RiceTrace | 60% | Giả định mức tham gia |
| Chênh giá bán trực tiếp | 5% | Giả định để minh họa độ nhạy |
| Chi phí bán hàng truyền thống | 150.000 VND/tấn | Giả định |
| Chi phí bán hàng qua nền tảng | 50.000 VND/tấn | Giả định |
| Hoa hồng doanh nghiệp trả | 1,5% | Giả định; website không trừ khoản này khỏi thu của nông dân |

Với các giá trị này, mô hình cho khoản thu theo kênh truyền thống là **635.000.000 VND**, khoản thu trong kịch bản RiceTrace là **660.500.000 VND**, chênh lệch **25.500.000 VND** (xấp xỉ **4,02%**). Chi phí mua hàng của doanh nghiệp trong kịch bản RiceTrace là **675.642.500 VND**, trong đó hoa hồng là **6.142.500 VND**. Đây chỉ là kết quả tính từ giả định mẫu.

## Cách trình bày và giới hạn

- Nên trình bày kết quả theo nhiều mức tỷ lệ bán qua nền tảng, chẳng hạn 0%, 60% và 100%; sau đó thử các mức chênh giá 0%, 5% và 10%.
- Giải thích rằng kết quả phụ thuộc vào các giả định. Không dùng kịch bản mẫu để kết luận RiceTrace chắc chắn làm tăng thu nhập hoặc khẳng định tỷ lệ tăng có thể áp dụng cho mọi nông hộ.
- “Khoản thu ròng” ở đây chỉ trừ chi phí bán hàng đã nhập. Mô hình chưa tính chi phí sản xuất, chi phí cố định của nền tảng, thuê bao năm, thuế, hao hụt, chất lượng lúa, rủi ro mùa vụ hoặc khả năng toàn bộ sản lượng được bán.
- Hoa hồng được giả định do doanh nghiệp trả theo mô tả mô hình kinh doanh trên website. Phí thuê bao năm chưa được phân bổ vào chi phí mua hàng trong vụ.
- Để dùng làm phân tích thực nghiệm, cần thay giá và chi phí giả định bằng dữ liệu khảo sát hoặc nguồn công khai có trích dẫn; ghi rõ địa bàn, thời điểm, cách chọn mẫu và phương pháp thu thập dữ liệu.
