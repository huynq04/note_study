# Merge pull request

## Tạo 1 nhánh mới từ nhánh master

1.  git checkout -b new-branch master
    - tạo 1 nhánh mới từ nhánh cha master
    - lưu ý: với cách tạo branch này sẽ lấy tất cả code trên local của nhánh master lưu vào nhánh new-branch (copy)
2.  git pull origin master
    - kéo code mới nhất từ nhánh master trên github về

## Merge code ở nhánh master

1. git checkout master

- chuyển sang nhánh master

2. git merge --no-ff new-branch

- merge code từ nhánh new-branch vào nhánh master

3. git push origin master

- đẩy code của nhánh master lên github
