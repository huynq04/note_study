# ReactJS

## Render component

1.  Component sẽ re-render khi props hay state của nó thay đổi. vd: component sẽ re-render khi setState

2.  Khi component cha chứa component con thì khi cha re-render thì con cũng re-render theo. Để tránh điều đó. Sử dụng "memo()" bọc ngoài component con.
    Khi dùng memo() thì cha re-render thì thằng con chỉ re-render khi props truyền vào thằng con thay đổi.

3.  Để tránh thực hiện lại 1 đoạn logic phức tạp như tính toán số liệu...Sử dụng useMemo();

4.  Khi truyền 1 props từ component cha sang con thì dùng memo() để tránh việc thằng con re-render không cần thiết. Nhưng nó chỉ đúng với việc các props là kiểu dữ liệu nguyên thủy: string, number, boolean, ...Với các dữ liệu không nguyên thủy như array, object, function thì dù props không thay đổi nhưng component con sẽ vẫn re-render vì nó là kiểu dữ liệu tham chiếu. Để tránh điều đó thì phải dùng useCallback() với những function muốn truyền vào thằng con. Dùng useCallback ở thằng cha thì phải dùng memo() ở thằng con.
