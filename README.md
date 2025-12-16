# Thuchanh_TTNT
# Thực hành Trí tuệ Nhân tạo (TTNT)

## Giới thiệu
Repo này phục vụ **demo 3 bài thực hành môn Trí tuệ Nhân tạo**.  
Các bài đều được cài đặt theo hướng **tổng quát, có input động**, thuận tiện cho việc demo và kiểm tra.

---

## Danh sách các bài thực hành

### 1. AKT / N-Puzzle (8-puzzle, 15-puzzle)
- Giải bài toán trượt ô số bằng tìm kiếm ưu tiên (priority-based search).
- Heuristic sử dụng: **số ô sai vị trí** (misplaced tiles).
- Dùng **Priority Queue (heap)** để ưu tiên trạng thái có chi phí thấp hơn.
- Có tập `visited` để tránh duyệt lặp trạng thái.

**Input động khi demo:**
- Kích thước bàn cờ `n`
- Trạng thái ban đầu (initial)
- Trạng thái đích (goal)
- Giới hạn số trạng thái duyệt

**Output:**
- Các bước từ initial đến goal
- Số bước và số trạng thái đã duyệt

---

### 2. A* (Tìm đường đi trên đồ thị)
- Cài đặt thuật toán **A\*** với hàm đánh giá `f(n) = g(n) + h(n)`.
- Hỗ trợ đọc dữ liệu đồ thị từ **file ngoài**.

**Input động khi demo:**
- Chọn graph mặc định hoặc đọc từ file `graph.txt`
- Chọn heuristic (`all1` hoặc nhập thủ công)
- Chọn đỉnh bắt đầu (start) và đỉnh kết thúc (goal)

**File input:**
- `graph.txt`: mỗi dòng có dạng `u v w` (đỉnh u, đỉnh v, trọng số w)

**Output:**
- Đường đi tìm được
- Tổng chi phí (cost)

---

### 3. Minimax (Caro / Tic-Tac-Toe)
- AI chơi game caro bằng thuật toán **Minimax**.
- Giả định đối thủ chơi tối ưu.

**Input động khi demo:**
- Kích thước bàn cờ (3x3, 4x4, 5x5)
- Chọn quân người chơi (X hoặc O)

**Ghi chú:**
- Với bàn cờ 3x3: Minimax duyệt đầy đủ.
- Với bàn cờ lớn hơn: sử dụng **depth limit + heuristic** để đảm bảo thời gian chạy.

---

## Cách chạy chương trình
- Mở file `BaoCao.ipynb` bằng **Google Colab** hoặc Jupyter Notebook.
- Chạy các cell theo thứ tự.
- Chọn bài cần demo thông qua menu và nhập dữ liệu theo hướng dẫn.

---

## Ghi chú chung
- Code không hardcode dữ liệu.
- Các hàm và class được tách rõ ràng, dễ đọc và dễ mở rộng.
- Phù hợp yêu cầu demo sản phẩm với **tham số động**.

