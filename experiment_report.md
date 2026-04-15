# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600128
**Name:** Ngo Anh Tu
**Date:** 2026-04-15
---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200.   | 8.5| |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999 | 3.5 | |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

(Viet nhan xet cua ban o day — it nhat 50 tu)

(Hay phan tich cac van de nhu Duplicate IDs, wrong data types, outliers, null values va giai thich tai sao chung anh huong den ket qua cua Agent.)

Voi du lieu "rác", Agent đã bị nhầm lẫn bởi các giá trị không hợp lệ và thiếu tính nhất quán. Ví dụ, các ID trùng lặp khiến Agent không thể xác định được bản ghi nào là chính xác, trong khi các giá trị ngoại lai(outliers) và kiểu dữ liệu sai làm cho việc phân tích trở nên khó khăn hơn. Điều này dẫn đến việc Agent đưa ra quyết định dựa trên thông tin sai lệch, từ đó kết quả trở nên không chính xác. Ngược lại, với dữ liệu "sạch", Agent có thể dễ dàng phân tích và đưa ra quyết định đúng đắn dựa trên thông tin chính xác và đầy đủ.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

Tôi đồng ý rằng "Quality Data > Quality Prompt". Dù một prompt có thể được thiết kế tốt đến đâu, nếu dữ liệu đầu vào không chính xác hoặc không đầy đủ, Agent sẽ không thể đưa ra quyết định đúng đắn. Ngược lại, với dữ liệu chất lượng cao, ngay cả một prompt đơn giản cũng có thể dẫn đến kết quả tốt. Do đó, việc đảm bảo chất lượng dữ liệu là yếu tố quan trọng hơn trong việc xây dựng các hệ thống AI hiệu quả.