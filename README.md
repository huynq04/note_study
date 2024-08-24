# Merge pull request

## Tạo 1 nhánh mới từ nhánh master

1.  git checkout -b new-branch master
    - tạo 1 nhánh mới từ nhánh cha master
    - lưu ý: với cách tạo branch này sẽ lấy tất cả code trên local của nhánh master lưu vào nhánh new-branch (copy)
2.  git pull origin master
    - kéo code mới nhất từ nhánh master trên github về

## Quy trình git trong thực tế

	Khi một developer commit code lên GitLab, thường là thông qua việc tạo một nhánh riêng từ nhánh chính (main/master). Dưới đây là quy trình chuẩn mà nhiều đội phát triển phần mềm thường sử dụng:
	
	1.  **Developer tạo merge request**:
	    
	    -   Developer sau khi hoàn thành công việc trên nhánh riêng của mình, sẽ tạo một **merge request** (MR) tới nhánh chính.
	    -   Merge request này sẽ được xem xét bởi leader hoặc người có quyền review code.
	2.  **Review và xử lý conflict**:
	    
	    -   **Code Review**: Leader hoặc người review sẽ kiểm tra code trong merge request. Họ có thể đưa ra những nhận xét hoặc yêu cầu sửa đổi.
	    -   **Xử lý Conflict**: Nếu có conflict giữa nhánh của developer và nhánh chính, developer chịu trách nhiệm xử lý conflict. Điều này giúp đảm bảo người làm việc trên code có kiến thức sâu nhất về những thay đổi của mình và có thể xử lý conflict một cách hiệu quả nhất.
	    -   Developer sẽ phải cập nhật nhánh của mình để giải quyết conflict, sau đó đẩy lại các thay đổi lên GitLab.
	3.  **Leader hoặc người review merge code**:
	    
	    -   Sau khi conflict đã được giải quyết và code được duyệt, leader hoặc người review sẽ tiến hành merge code vào nhánh chính.
	4.  **Quy trình khi Leader cần xử lý merge**:
	    
	    -   Trong trường hợp đặc biệt mà leader phải tự merge code từ các nhánh khác (ví dụ, khi merge một cách nhanh chóng hoặc vì lý do tổ chức), leader sẽ phải chịu trách nhiệm giải quyết bất kỳ conflict nào xảy ra.
	    -   Tuy nhiên, thông thường, leader sẽ yêu cầu developer giải quyết conflict trước khi merge để đảm bảo tính toàn vẹn và chất lượng của code.
	
	### Tóm lại:
	
	-   Developer là người chịu trách nhiệm tạo merge request và xử lý conflict trên nhánh của họ.
	-   Leader hoặc người review sẽ kiểm tra code, và sau khi mọi thứ được duyệt, họ sẽ thực hiện merge vào nhánh chính.
	-   Việc giải quyết conflict nên do người có kiến thức tốt nhất về thay đổi đó (tức là developer) thực hiện, trừ khi có những tình huống đặc biệt yêu cầu leader phải tự xử lý.

## Merge code ở nhánh master

### Đây là cách merge trên local, ngoài ra có thể thao tác trực tiếp trên gitHub

1. git checkout master

	- chuyển sang nhánh master

2. git merge --no-ff new-branch

	- merge code từ nhánh new-branch vào nhánh master

3. git push origin master

	- đẩy code của nhánh master lên github

# Config git local machine

1.  Mở gitBash rồi
	- cop 2 câu lệnh từ trang: [đây](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)

	- câu lệnh 1 là username của gitHub

	- câu lệnh 2 là email tạo gitHub

	- câu lệnh 3: git config –list (kiểm tra xong git thành công chưa)

3. Vào thư mục chứa sourse code
	
	- Chuột phải chọn GitBash

	-   git init
	    
	-   copy đường dẫn dài nhất ở new reponsitory
	    
	-  git remote -v (kiểm tra đường dẫn git)
	    
	-   git add .
	    
	-  git commit -m”” (để đưa ra nhãn của code - đưa tên muốn đặt vào trong dấu nháy)
	  -  git push origin master (đợi đến master -> master là xong)
