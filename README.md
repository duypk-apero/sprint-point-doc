# Hướng Dẫn Phân Tích Rủi Ro Trong Sprint Point

## Mục Lục
1. [Tổng Quan](#tổng-quan)
2. [Các Loại Rủi Ro](#các-loại-rủi-ro)
3. [Thang Điểm Đánh Giá](#thang-điểm-đánh-giá)
4. [Quy Trình Phân Tích](#quy-trình-phân-tích)
5. [Ví Dụ Thực Tế](#ví-dụ-thực-tế)

## Tổng Quan

Phân tích rủi ro là một phần quan trọng trong việc ước lượng sprint point. Nó giúp team:
- Dự đoán được các vấn đề có thể xảy ra
- Chuẩn bị phương án dự phòng
- Ước lượng thời gian chính xác hơn
- Giảm thiểu việc underestimate tasks

## Các Loại Rủi Ro

### 1. Rủi Ro Kỹ Thuật
- Công nghệ mới/chưa có kinh nghiệm
- Tích hợp với hệ thống bên thứ 3
- Vấn đề về performance
- Khó khăn trong testing
- Dependencies với các components khác

### 2. Rủi Ro Nghiệp Vụ
- Yêu cầu không rõ ràng
- Logic nghiệp vụ phức tạp
- Thay đổi requirements
- Phụ thuộc vào quyết định của stakeholders
- Vấn đề về compliance/legal

### 3. Rủi Ro Team
- Thiếu kinh nghiệm với domain
- Member có thể vắng mặt
- Phối hợp với teams khác
- Cần support từ teams khác
- Conflict trong resource allocation

### 4. Rủi Ro Môi Trường
- Vấn đề về infrastructure
- Môi trường development/testing
- Network/security constraints
- Giới hạn về performance
- Deployment challenges

## Thang Điểm Đánh Giá

### Risk Factor (1-5)

1. **Minimal Risk (1 point)**
   - Công nghệ quen thuộc
   - Requirements rõ ràng
   - Team có kinh nghiệm
   - Không có dependencies

2. **Low Risk (2 points)**
   - Một vài unknowns nhỏ
   - Dependencies đơn giản
   - Cần một ít research
   - Testing đơn giản

3. **Medium Risk (3 points)**
   - Công nghệ mới cho team
   - Dependencies phức tạp
   - Cần research kỹ
   - Nhiều test cases

4. **High Risk (4 points)**
   - Công nghệ hoàn toàn mới
   - Nhiều dependencies
   - Yêu cầu phức tạp
   - Cần POC

5. **Critical Risk (5 points)**
   - Chưa có precedent
   - Dependencies không kiểm soát được
   - Có thể fail hoàn toàn
   - Ảnh hưởng critical system

## Quy Trình Phân Tích

1. **Identify Risks**
   - List tất cả rủi ro có thể
   - Phân loại theo categories
   - Đánh giá likelihood
   - Đánh giá impact

2. **Analyze Impact**
   - Ảnh hưởng đến timeline
   - Ảnh hưởng đến resources
   - Ảnh hưởng đến quality
   - Ảnh hưởng đến systems khác

3. **Plan Mitigation**
   - Strategies giảm thiểu rủi ro
   - Backup plans
   - Resource allocation
   - Monitoring points

4. **Calculate Risk Points**
   ```
   Risk Points = Base Risk + (Sum of Risk Factors * Weight)
   ```
   - Base Risk: Điểm rủi ro cơ bản (1-5)
   - Risk Factors: Các yếu tố rủi ro phụ
   - Weight: Trọng số của từng loại rủi ro

## Ví Dụ Thực Tế

### Task: Implement Payment Integration

**1. Risk Analysis:**
- Tích hợp với payment gateway mới (4 points)
- Security requirements cao (3 points)
- Team chưa có kinh nghiệm với payment (3 points)
- Cần compliance với PCI DSS (4 points)

**2. Risk Calculation:**
- Base Risk: 4 (High complexity integration)
- Additional Factors: (4 + 3 + 3 + 4) * 0.5 = 7
- Total Risk Points: 4 + 7 = 11

**3. Mitigation Plan:**
- POC với payment gateway
- Security audit
- Team training
- Phân phase triển khai
- Extensive testing plan

### Task: UI Update

**1. Risk Analysis:**
- Design đã rõ ràng (1 point)
- Sử dụng existing components (1 point)
- Responsive requirements (2 points)
- Browser compatibility (2 points)

**2. Risk Calculation:**
- Base Risk: 1 (Low complexity)
- Additional Factors: (1 + 1 + 2 + 2) * 0.5 = 3
- Total Risk Points: 1 + 3 = 4

**3. Mitigation Plan:**
- Browser testing matrix
- Responsive testing checklist
- Design review
- UAT với stakeholders 