<!-- Banner -->
<p align="center">
  <a href="https://www.uit.edu.vn/" title="Trường Đại học Công nghệ Thông tin" style="border: none;">
    <img src="https://i.imgur.com/WmMnSRt.png" alt="Trường Đại học Công nghệ Thông tin | University of Information Technology">
  </a>
</p>

<h1 align="center"><b>ĐỒ HOẠ MÁY TÍNH</b></h>

## THÀNH VIÊN NHÓM
| STT    | MSSV          | Họ và Tên              |Chức Vụ    | Github                                                  | Email                   |
| ------ |:-------------:| ----------------------:|----------:|--------------------------------------------------------:|-------------------------:
| 1      | 19521676      | Đỗ Trọng Khánh         |Nhóm trưởng|[trong-khanh-1109](https://github.com/trong-khanh-1109)  |19521676@gm.uit.edu.vn   |
| 2      | 19521383      | Võ Phạm Duy Đức        |Thành viên |[ducducqn123](https://github.com/ducducqn123)            |19521383@gm.uit.edu.vn   |
| 3      | 19521326      | Trịnh Công Danh        |Thành viên |[danhtrinh15092001](https://github.com/danhtrinh15092001)|19521326@gm.uit.edu.vn   |

## GIỚI THIỆU MÔN HỌC
* **Tên môn học:** Đồ hoạ máy tính
* **Mã môn học:** CS105
* **Mã lớp:** CS105.M11.KHCL
* **Năm học:** HK1 (2021 - 2022)
* **Giảng viên**: ThS.Cáp Phạm Đình Thăng

## QUÁ TRÌNH
### Week 1: Các thuật toán vẽ đường thẳng.
#### 1. Thuật toán Digital differential analyzer (DDA)
  - Phương trình đường thẳng: `y = m.x + b`.</br>
  </br>![Phương trình đường thẳng](Image/ptdt.png)
  - Để đơn giản hóa giải thuật ta xét đường thẳng với `min [0,1] , Dx > 0`
  - Tại mỗi bước ta cho `X` tăng lên 1 đơn vị tức là `Xi+1 = Xi + 1 => Yi+1 = Yi + m`
  - Do `m` là số thực nên muốn `Yi+1` là số nguyên ta phải làm tròn trước khi truy xuất tọa độ để đưa ra màn hình.
  - Với đường thẳng có `m > 1` ta sẽ làm ngược lại cho `Y` biến thiên và tính `X` theo `Y` nghĩa là tại mỗi bước ta có Yi+1 = Yi + 1 => Xi+1 = Xi + m
  - Với các đoạn thẳng có `Dx <0` ta sẽ cho `X` giảm xuống chứ không tăng.</br>

<table>
<tr>
  <td>
    <img src="https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/d745acb3dbbf247cb71d60679b1c07f4fd4313f7/Image/DDA.png" />
  </td>
  <td>
    <img src="https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/d745acb3dbbf247cb71d60679b1c07f4fd4313f7/Image/Lu%CC%9Bu%20%C4%91o%CC%82%CC%80%20DDA.png" />
  </td>
</tr>
<table>
  
  - Code: [DDA Algorithm](Progress/Week_1/LineBresenham.cpp)
 
#### 2. Thuật toán Bresenham
  - Với thuật toán Bresenham vẽ đường thẳng có thể xác định được điểm cần tìm dựa vào khoảng cách giữa đường thẳng thực tế với các điểm nằm trong vùng lựa chọn.
  - Để vẽ được đường thẳng trên màn hình máy tính cần xác định được điểm ảnh vẽ tiếp theo trên màn hình. Thuật toán Bresenham có thể xác định được điểm cần tìm dựa vào khoảng cách giữa đường thẳng thực tế với các điểm nằm trong vùng lựa chọn.
<table>
<tr>
  <td width>
    <img src="https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/97306c26556cc8f728ac43947e344b378dffbae1/Image/Bresenham.png" />
  </td>
  <td>
    <img src="https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/15c766e2f10ace0dd4596c5b583db23bf856c912/Image/Lu%CC%9Bu%20%C4%91o%CC%82%CC%80%20Bresenham.png" />
  </td>
</tr>
<table>
  
  - Code: [Bresenham Algorithm](Progress/Week_1/LineBresenham.cpp)</br>
### Week 2: Thuật toán vẽ đường tròn và Các phép biến đổi.

#### 1. Thuật toán Mid-Point.
  - Sử dụng thuật toán Mid-Point để tính toán tất cả các điểm chu vi của vòng tròn trong một cung tròn đầu tiên và sau đó in chúng cùng với các điểm phản chiếu của chúng trong các cung tròn khác. Điều này sẽ hoạt động vì một vòng tròn là đối xứng về tâm của nó.
  <table>
<tr>
  <td width>
    <img src="https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/60875d35522d1be935604f1277d6f1f9c359cf4c/Image/Mid-point.png" />
  </td>
  <td>
    <img src="https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/60875d35522d1be935604f1277d6f1f9c359cf4c/Image/Lu%CC%9Bu-%C4%91o%CC%82%CC%80%20Mid-point.png" />
  </td>
</tr>
<table>
  
- Code: [Mid-Point Algorithm](Progress//Week_2/CircleMidPoint.cpp)
  
#### 2. Các phép biển đổi affine cơ sở.
  - Có 3 phép biến đổi affine cơ sở: Phép tịnh tiến, Phép quay, Phép tỉ lệ.
  - Phép tịnh tiến (translation): Dùng để thay đổi vị trí của đối tượng từ vị trí này sáng vị trí khác.
    + Độ dịch chuyển trên trục Ox : tx.
    + Độ dịch chuyển trên trục Oy : ty.
  - Phép quay (rotation): Dùng để thay đổi hướng của đối tượng.
    + Tâm quay : O.
    + Góc quay : alpha.
  - Phép tỉ lệ (scaling): Dùng để thay đổi kích thước của đối tượng.
    + Tâm tỉ lệ : O.
    + Hệ số tỉ lệ : sx, sy.
  - [Công thức và cài đặt](https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/54c08fb828f6c528f01af235acb269e937e4b6cb/Week_2/lecture_2D_1.pdf)
  
### Week 3: Thuật toán vẽ Ellipse và tô màu.
  - Chia Elip làm 2 phần tại điểm Q nơi có hệ số góc của tiếp tuyến với Elip bằng -1. Tại vùng thứ nhất, x biến thiên nhanh hơn y và tại vùng thứ hai , y biến thiên nhanh hơn x. Nhớ lại công thức hệ số góc của đường cong : `dx/dy = fx/fy = (2b2x) /( 2a2y)`</br>
    
&emsp;&emsp;&emsp;&emsp;<img align='center' src='https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/1c6a52ad61d7b810fd1e1e6f9b12626a5227fbaf/Image/elip.jpeg'></br>
  
  - Code: [Mid-Point Algorithm and Boundary Fill & Scan line fill.](Progress//Week_3/Elip.cpp)
  
### Week 4: Tổng quan về đồ hoạ 3D.
- Bài tập : [Vẽ hình hộp + Mặt phẳng sử dụng thư viện Three.js.](./Progress//Week_4)

### Week 5: Các phép biến đổi trên đồ hoạ 3D.
  - Bài tập : [Phép biến đổi affine trong không gian 3D + Phép biến đổi quan sát.](./Progress//Week_5)</br>
  
  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;![Motion in 3D](https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/d0d28a568f72759b39e0928893c00d1f94e800a6/Image/Bie%CC%82%CC%81n_%C4%91o%CC%82%CC%81i_3D.gif)

### Week 6: Chiếu sáng và Texture trong đồ hoạ 3D.
  - Bài tập: [Light-Animation.](./Progress/Week_6/Light-Animation) and [Textuers-Materials.](./Progress//Week_6/Textuers-Materials)
<table>
  <tr>
    <td><img src='https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/451cfe5a6c9ca44749cfdd95b29a8977b13bb42c/Image/Light-Animation.gif'></td>
    <td><img src='https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/451cfe5a6c9ca44749cfdd95b29a8977b13bb42c/Image/Textuers-Materials.gif'></td>
  </tr>
</table>

### Week 7: Xử lý ảnh.
  - Dò tìm: Khuôn mặt người trong ảnh.
  - Hướng dẫn:
      + Download cascade train sẵn ở đây: https://github.com/opencv/opencv/tree/master/data/haarcascades
      + To detect faces in images
      + Detect in frame in a video
  - Bài tập: [Face Detection.](Progress/Week_7/Face-Detection.ipynb)

### Week 8: Xử lý ảnh 2.
  - Dò tìm các feature của khuôn mặt: mắt, mũi, miệng của khuôn mặt.
  - Dò tìm người đi bộ trong ảnh và video.
  - Dò tìm car trong ảnh.
  - Bài tập: [Object Detection.](Progress/Week_8/Untitled0.ipynb)

## ĐỒ ÁN CUỐI KÌ
### Giới thiệu đề tài
  - Tên đề tài: Mô phỏng hình học 3D cơ bản.
  - File báo cáo: [Final Report.](Final_Project/Final_Report.pdf)
### Thực nghiệm
  - Source code: [Simulate Basic Geometry](https://github.com/Karhdo/geometry-simulation)
  - Demo: [Project Computer Graphics.](https://DoTrOngKhAnh.github.io/Project_Computer-Graphics/)
  <p align='center'><img src='https://github.com/trong-khanh-1109/CS105.M11.KHCL/blob/00a69f6b5414f34d20cfa8faff7c28eda363a11e/Image/final_project.png'></p>
  
<!-- Footer -->
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;`Copyright © 2021 - Đỗ Trọng Khánh`
