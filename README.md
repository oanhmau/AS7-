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
# 
