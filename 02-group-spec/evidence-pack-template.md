# Template — Evidence Pack

Nộp kèm thin SPEC cuối Day 05.

## 1. Nhóm và track

**Tên nhóm: 7**  
**Track: Healthcare**  
**Product/app đã chọn: NEO**  
**Build slice đang nghĩ: Giải thích đơn thuốc**  
```
Giải thích đơn thuốc
PainPoint: Bạn nhổ răng khôn xong và không bị bất kỳ tình trạng khác thường nào nhưng bác sĩ dặn uống thuốc đều đặn. Bạn muốn tiết kiệm tiền nên bạn muốn tìm cách để giảm số thuốc phải mua nhằm tiết kiệm tiền -> Bạn cần biết các thuốc trong đơn thuốc của bạn có tác dụng gì để ra quyết định mua hay không .  
Điểm trừ:
-giải thích sai ý nghĩa thuốc
-giải thích sai đối tượng sử dụng thuốc
-
Điểm cộng:
+Cảnh báo được liều lượng thuốc cho người dùng
+Giải thích công dụng của thuốc theo đối tượng sử dụng

story: Bệnh nhân vừa được kê 1 đơn thuốc . Người bệnh sử dụng thuốc cảm thấy dấu hiệu lạ nhưng biểu hiện nhẹ nên người dùng đưa đơn thuốc cho bot để giải thích . Bot giải thích liều lượng dành cho đối tượng sử dụng thông thường (người khỏe mạnh không có tiền sử bệnh) và đề xuất người dùng đi hỏi ngay các bác sĩ chuyên khoa về liều lượng thuốc . 

current-flow : Người bệnh thấy dấu hiệu lạ -> Tìm các tiệm thuốc -> dược sĩ trả lời không chắc chắn -> người bệnh không nắm rõ được tình trạng 
future-flow : Người bệnh thấy dấu hiệu lạ -> Hỏi Bot -> Bot kiểm tra loại thuốc,đối tượng sử dụng, tình trạng hiện tại ->  Bot cảnh báo hiện trạng và đề xuất hướng bệnh nhân đến các bác sĩ chuyên môn .

risk : Tự lựa chọn thuốc cho user, Khẳng định user không bị gì dù user có tình trạng bất thường, Tự cung cấp các thông tin không rõ, Cung cấp các giá thuốc ảo dù không có data.
Thuốc được kê cho trẻ em nhưng bot giải thích theo liều người lớn.
Thuốc cho phụ nữ có thai hoặc cho con bú nhưng bot không nhận diện.
Thuốc cần điều chỉnh liều theo tuổi (người già) nhưng bot không cảnh báo.
Thuốc cần điều chỉnh liều theo cân nặng nhưng bot dùng liều mặc định.
Bot không phát hiện các triệu chứng cần chuyển viện khẩn cấp.
Không phân biệt tác dụng phụ thông thường và biến chứng nặng
Không nhận diện tương tác thuốc
```

## 2. Self-use evidence

Nhóm tự dùng app/workflow và ghi lại điểm gãy.

| Observation | Screenshot/link | Path liên quan | Điều học được |
|---|---|---|---|
| Đơn thuốc rõ nét |  | Happy / Low-confidence / Failure / Correction |  |
| Đơn thuốc mờ |  | Happy / Low-confidence / Failure / Correction |  |
| User hỏi "Thuốc nào bỏ được?" |  | Happy / Low-confidence / Failure / Correction |  |
| User có tác dụng phụ nhẹ như buồn ngủ, chóng mặt |  | Happy / Low-confidence / Failure / Correction |  |
| User có dấu hiệu nguy hiểm như khó thở, sưng môi (Critical Failure). |  | Happy / Low-confidence / Failure / Correction |  |

## 3. User / review / social evidence

Nguồn có thể là review App Store/Play, group, comment, phỏng vấn nhanh, hoặc nguồn public khác.

| Quote / review / observation | Nguồn | User là ai? | Pain/failure mode |
|---|---|---|---|
| "Nearly half of the participants misunderstood one or more of the prescription drug labels." | Northwestern University study (2006) - https://www.sciencedaily.com/releases/2006/11/061129093308.htm | Bệnh nhân sử dụng thuốc kê đơn | Hiểu sai hướng dẫn dùng thuốc mặc dù đã đọc nhãn thuốc, dẫn tới uống sai liều hoặc sai thời điểm. |
| "Misunderstanding rates ranged from 8% to 33% across common prescription instructions." | Davis et al., Journal of General Internal Medicine - https://pubmed.ncbi.nlm.nih.gov/17587533/ | Bệnh nhân ngoại trú nhận đơn thuốc | Hướng dẫn trên đơn thuốc khó hiểu, cách diễn đạt thời gian uống thuốc không rõ ràng. |
| Medical abbreviations such as BID, TID, PRN and PO are frequently misunderstood by patients because they are designed for healthcare professionals rather than patients. | Wolf et al. - https://pmc.ncbi.nlm.nih.gov/articles/PMC2680452/ | Người bệnh tự đọc đơn thuốc | Không hiểu ký hiệu và thuật ngữ y khoa trên đơn thuốc, phải hỏi lại bác sĩ hoặc dược sĩ. |
| Elderly patients reported difficulty reading medication labels because of small text, English language usage, and unclear symbols. | Community discussion & observations from elderly medication users - https://www.reddit.com/r/singapore/comments/decrd3 | Người cao tuổi | Không đọc được hoặc không hiểu thông tin trên thuốc do hạn chế thị lực và ngôn ngữ. |
| Patients commonly ask "What should I do if I miss a dose?" and often do not receive clear guidance from prescription instructions. | Medication Question Answering research - https://arxiv.org/abs/2102.05442 | Người dùng thuốc dài ngày | Không biết xử lý khi quên liều, dễ tự ý uống bù hoặc bỏ qua liều thuốc. |
| Older adults taking multiple medications often struggle to remember what each medication is for and how they should be taken. | Polypharmacy risk analysis - https://www.washingtonpost.com/health/2025/06/29/polypharmacy-old-people-risks/ | Người cao tuổi dùng nhiều thuốc | Dễ nhầm thuốc, uống sai thuốc hoặc không nhớ công dụng của từng loại thuốc. |

Nếu chưa có nguồn ngoài nhóm, ghi rõ:

```text
Đây là giả định. Nhóm sẽ kiểm bằng [cách] trước checkpoint M1 Day 06.
```

## 4. Competitor / analog evidence

| App / mô hình tham khảo | Họ xử lý task này thế nào? | Pattern học được | Có áp dụng trong 1 ngày không? |
|---|---|---|---|
|  |  |  |  |

## 5. Evidence -> Insight

```text
Evidence nổi bật nhất:

Insight:
User không chỉ gặp [surface problem].
Thật ra họ cần [deeper need / decision support / trust / recovery].

Opportunity:
AI có thể giúp bằng cách [augment/automate hành động hẹp].
```

## 6. Evidence đổi SPEC như thế nào?

- [ ] Đổi user chính.
- [ ] Đổi pain statement.
- [ ] Đổi build slice.
- [ ] Đổi Auto/Aug decision.
- [ ] Đổi 4 paths.
- [ ] Đổi failure mode.
- [ ] Đổi owner/test plan.

Ghi rõ 1-2 thay đổi quan trọng:

```text
Trước evidence, nhóm định...
Sau evidence, nhóm đổi thành...
Lý do:
```
