# REFLECTION — K4-Track02-Day18

Anti-pattern nguy hiểm nhất với pipeline quan trắc LLM của tôi là **evolution schema vô tội vạ và external index stale**.

NB1 cho thấy enforcement chặn `age='thirty'`, chỉ `schema_mode='merge'` mới thêm `tier`. Nếu cho phép merge mặc định, một job lỗi sẽ phình schema, vỡ Gold và dashboard cost/latency. NB7/NB8 còn cho thấy index ngoài không nhận delete sẽ trả dữ liệu đã xóa.

Phòng tránh: merge phải opt-in có review, ghi provenance từ Bronze, pin version khi train, và bắt delete lan tới mọi index. Dữ liệu tôi quan tâm là log request/response có PII nên càng cần kỷ luật này.

AI: dùng AI để giải thích khái niệm, đọc code và gỡ lỗi; tự chạy, kiểm tra output và viết giải thích. Chi tiết xem AI_USAGE.md.
