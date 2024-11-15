## AS7-
# 1. Thiết kế thuật toán giải phương trình bậc nhất 𝑎𝑥 + 𝑏 = 0, 𝑎 ≠ 0?
#include <iostream>
using namespace std;

int main() {
    // Khai báo các biến a, b và x
    double a, b, x;
    
    // Nhập giá trị cho a và b
    cout << "Nhap a: ";
    cin >> a;
    cout << "Nhap b: ";
    cin >> b;
    
    // Kiểm tra điều kiện a != 0
    if (a == 0) {
        cout << "Phuong trinh vo nghiem hoac khong xac dinh!" << endl;
    } else {
        // Tính nghiệm x = -b / a
        x = -b / a;
        cout << "Nghiem cua phuong trinh la: " << x << endl;
    }

    return 0;
}

 
# 2.Độ phức tạp thời gian của thuật toán là gì? Nêu các định nghĩa 𝑂,Θ,Ω.
-Độ phức tạp thời gian (time complexity) của một thuật toán là một phép đo xác định số bước tính toán mà thuật toán cần để giải quyết một bài toán với kích thước đầu vào nhất định. Nó thường được đo bằng hàm phụ thuộc vào kích thước đầu vào, biểu diễn cách thức thuật toán xử lý vấn đề khi kích thước của dữ liệu đầu vào tăng lên.
-Các định nghĩa 𝑂,Θ,Ω
  + O (Big O) - Độ phức tạp trên cùng (Worst-case complexity): Ký hiệu O(f(n)) mô tả độ phức tạp tối đa của thuật toán, tức là thời gian thực thi trong trường hợp xấu nhất. Nó biểu thị cách mà thời gian hoặc bộ nhớ của thuật toán tăng lên khi kích thước đầu vào n tăng, và không bao giờ vượt quá một hàm nào đó f(n), trong trường hợp xấu nhất.
  + Θ (Theta) - Độ phức tạp chính xác (Tight bound):  Ký hiệu Θ(f(n)) mô tả độ phức tạp chính xác của thuật toán, tức là nó cung cấp một giới hạn chặt chẽ cho độ phức tạp thời gian hoặc bộ nhớ của thuật toán. Điều này có nghĩa là thời gian thực thi của thuật toán sẽ tỷ lệ với f(n) trong cả trường hợp tốt nhất, trung bình và xấu nhất khi kích thước đầu vào 𝑛 đủ lớn.
  + Ω (Omega) - Độ phức tạp dưới cùng (Best-case complexity): Ký hiệu Ω(f(n)) mô tả độ phức tạp tối thiểu của thuật toán, tức là thời gian thực thi trong trường hợp tốt nhất. Nó chỉ ra rằng thời gian thực thi của thuật toán sẽ không ít hơn một giá trị nào đó theo hàm 𝑓(𝑛), trong trường hợp tốt nhất.
# 3

# 4
### **Chứng minh \( \Theta(f(n) + g(n)) = \max\{ \Theta(f(n)), \Theta(g(n)) \}**

**1. Định nghĩa \( \Theta(f(n)) \):**  
Hàm \( f(n) = \Theta(g(n)) \) có nghĩa là tồn tại các hằng số \( C_1, C_2 > 0 \) và một giá trị \( n_0 \) sao cho với mọi \( n \geq n_0 \), ta có:
\[
C_1 \cdot g(n) \leq f(n) \leq C_2 \cdot g(n)
\]

**2. Phân tích \( \Theta(f(n) + g(n)) \):**  
Khi cộng hai hàm \( f(n) + g(n) \), hàm nào tăng trưởng nhanh hơn sẽ chiếm ưu thế, tức là:
\[
f(n) + g(n) = \Theta(\max\{ f(n), g(n) \})
\]

**3. Chứng minh:**

- **\( \Theta(f(n) + g(n)) \subseteq \max\{\Theta(f(n)), \Theta(g(n))\}:**  
  Khi \( n \) đủ lớn, ta có \( f(n) + g(n) = O(\max(f(n), g(n))) \), do đó \( f(n) + g(n) \in \max\{\Theta(f(n)), \Theta(g(n))\} \).

- **\( \max\{\Theta(f(n)), \Theta(g(n))\} \subseteq \Theta(f(n) + g(n)):**  
  Nếu \( f(n) \in \Theta(f(n)) \), thì \( f(n) + g(n) \in \Theta(f(n)) \). Tương tự, nếu \( g(n) \in \Theta(g(n)) \), ta có \( f(n) + g(n) \in \Theta(g(n)) \).

**4. Kết luận:**
\[
\Theta(f(n) + g(n)) = \max\{\Theta(f(n)), \Theta(g(n))\}
\]

# 5 
### **Chứng minh \( T(n) = n^3 + n^2 + 1 \) thuộc \( O(n^3) \), \( \Theta(n^3) \), \( \Omega(n^2) \)**

1. **Chứng minh \( T(n) \in O(n^3) \):**  
   \( T(n) = n^3 + n^2 + 1 \).  
   Với \( n \) đủ lớn, \( n^3 \) là thành phần chiếm ưu thế, do đó:
   \[
   T(n) \leq C \cdot n^3 \quad \text{với} \quad C = 2 \quad \text{và} \quad n \geq 1
   \]
   Vậy \( T(n) \in O(n^3) \).

2. **Chứng minh \( T(n) \in \Theta(n^3) \):**  
   Từ \( T(n) = n^3 + n^2 + 1 \), ta có:
   \[
   n^3 \leq T(n) \leq 2n^3 \quad \text{với} \quad n \geq 1
   \]
   Vậy \( T(n) \in \Theta(n^3) \).

3. **Chứng minh \( T(n) \in \Omega(n^2) \):**  
   \( T(n) = n^3 + n^2 + 1 \), ta có:
   \[
   T(n) \geq n^2 \quad \text{với} \quad n \geq 1
   \]
   Vậy \( T(n) \in \Omega(n^2) \).

### **Kết luận:**
\[
T(n) \in O(n^3), \, \Theta(n^3), \, \Omega(n^2)
\]




