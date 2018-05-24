ĐỀ 01: QUICK NOTE

THÔNG TIN CÁ NHÂN
	Họ và tên: Phùng Thị Hòa
	MSSV: 1512186
	Gmail: phunghoa.h9@gmail.com

CHỨC NĂNG ĐÃ LÀM ĐƯỢC
	- Khi chạy app, một icon được thêm vào khu vực thông báo.

	- Khi kích chuột phải thì sẽ thầy menu gồm: View notes, View statitics, Exit 
		+ Khi nhấn Exit, app được tắt hoàn toàn.
		+ Khi nhấn View notes một cửa sổ xuất hiện với ba thành phần chính. Gồm 1 treeview, 1 list view và 1 phần để hiển thị full note.
		  
		  Tree view chứa 2 root là Note và Tags. Root Note có con là các notes, phần hiển thị là phần title của của các note. 
		  Root Tags có các item con là các tasg, phần hiển thị là phần tên tags và số lượng tags nằm trong cặp dấu (). 
		  Ví dụ: Hòa(3) có nghĩa là tags "Hòa" có số lần xuất hiện là 3 lần. 
		
		  List View: Chứa hai cột là "Date created" (Thời gian tạo) và "Preview" (Hiện thị 50 kí tự đầu tiên của phần content note).

		  Phần hiển thị full note: có 3 phần là Title, Tags, Full content

		  Khi User nhấn vào root Note, một list note sẽ xổ xuống, bên list view cũng hiển thị tương ứng. Khi chọn 1 note  ở treeview hoặc listview, phần hiển thì full content sẽ hiện thị tương ứng.
		  Khi User nhấn vào root Tags, một list tags xổ xuống, khi chọn 1 item là con của Tags, bên listview sẽ hiển thị số note ứng với từng Tags. Chọn vào các note đấy, full content sẽ hiện thị tương ứng.

		+ Khi nhấn vào View Statitics: Dialog chứa biểu đồ tròn thể hiện tần số của các Tags  sẽ xuất hiện. 
		  Biểu đồ tròn được chú giải đầy đủ.

	- Khi User nhấn tổ hợp phím (Windows + N) sẽ xuất hiện dialog thực hiện chức năng AddNote. 
	  Để lưu note thành công, User cần nhập đầy đủ 3 thông tin là Title, Content và Tags. Các Tags được phân biệt với nhau bởi ", "

LUỒNG SỰ KIỆN CHÍNH
	- User chạy app-> click vào root Note-> click vào một item con của Note-> click vào một item bên ListView.
	- User chạy app-> click vào root Tags> click vào một item con của Tags> click vào một item bên ListView.
	- User chạy app, cửa số chính xuất hiện-> user nhấn chuột phải vào icon của app ở vùng notification-> chọn "Hide", cửa sổ chính được ẩn đi.
	- Khi của sổ chính bị ẩn, User nhấn chuột phải vào icon của app ở vùng notification-> Chọn "View Note", cửa sổ chính (cửa số View Note) xuất hiện.
	- Khi chương trình đang được chạy ngầm, user nhấn tổ hợp phím "Windows + N", dialog Add Note xuất hiện, User nhập đấy đủ các thông tin Title, Content, Tags-> nhấn Save, thông tin của note mới sẽ được lưu.
	- User chạy app-> click chuột phải vào icon của app ở vùng notification-> chọn "View Statitics", biểu đồ thể hiện sự xuất hiện của các Tags sẽ xuất hiện-> click button "Close" để tắt dialog.
	- User chọn "Exit" ở Menu, chương trình sẽ tắt hoàn toàn.

LUỒNG SỰ KIỆN PHỤ
	- Khi cửa sổ chính (View Note) bị ẩn, User double click vào icon của app ở vùng notification, cửa sổ sẽ xuất hiện.
	- User nhấn vào dấu X (hủy)  của cửa sổ chính, thay vì tắt chương trình sẽ bị ẩn đi (chương trình chỉ tắt khi chọn "Exit").
	- Đối với việc nhập thông tin của dialog Add Note, khi User nhấn Save, chương trình tiến hành kiểm tra lỗi.
	  Nếu có lỗi xảy ra, MessageBox sẽ xuất hiện, chỉ rõ nội dung vi phạm của User khi nhập.
	  Thông tin không hợp lệ nên note sẽ không được thêm.
	  Để hủy bỏ việc thêm Note nhấn vào button "Cancel"
.
LINK YOUTUBE	 
https://youtu.be/oQ_H_8XtT7g

LINK BITBUCKET
https://phunghoa@bitbucket.org/phunghoa/finalproject_quicknote.git