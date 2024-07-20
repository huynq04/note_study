# Merge pull request

## Tạo 1 nhánh mới từ nhánh master

1.  git checkout -b new-branch master
    - tạo 1 nhánh mới từ nhánh cha master
    - lưu ý: với cách tạo branch này sẽ lấy tất cả code trên local của nhánh master lưu vào nhánh new-branch (copy)
2.  git pull origin master
    - kéo code mới nhất từ nhánh master trên github về

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
