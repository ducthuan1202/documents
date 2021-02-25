# Hướng dẫn sử dụng GIT trong dự án

## Ví dụ cơ bản
Bài này yêu cầu nắm rõ về quy tắc đặt bên branch. Nếu chưa nắm rõ vui lòng xem lại bài [Các quy tắc chung](git-convention.md) để hiểu rõ.

Giả sử team của chúng ta sẽ triển khai 01 chức năng về quản lý user trên 01 hệ thống bất kỳ. Chức năng này sẽ bao gồm các tasks như sau:
- Đăng ký (1)
- Đăng nhập (2)
- Cập nhật thông tin user (3)
- Thay đổi ảnh đại diện (4)
- Quên mật khẩu (5)
- Thay đổi mật khẩu (6)

Trong team hiện tại có 3 dev để thực hiện các công việc này và được phân chia như sau:
- **Nguyễn Đức Thuận**: làm task (1) và (2)
- **Trần Quỳnh**: làm task (3) và (4)
- **Nguyễn Thành Name**: làm task (5) và (6)

Do làm đồng thời với nhau nhưng công việc lại độc lập nên chúng ta cần có flow rõ ràng để tránh việc bị đè code, mất code...
Vậy quy trình làm việc với GIT cụ thể như sau:

Sau khi tạo `repository` trên git, từng dev sẽ clone về máy local để bắt đầu thực hiện. Mặc định ban đầu, chúng ta 
sẽ làm việc với git trên nhánh `master`.

Các dev cần tạo ra nhánh `develop` là nơi thực hiện merge code của từng dev sau khi hoàn thành feature.

Mỗi dev sẽ phải tạo ra 1 branch của riêng mình, đây là branch định danh cho mỗi dev và cũng là branch nền tảng cho các branch feature về sau.
Quy ước đặt tên branch như sau:
- Nguyễn Đức Thuận => `thuannd`
- Trần Quỳnh => `quynht`
- Nguyễn Thành Nam => `namnt`

Như vậy, bây giờ git của chúng ta đã có 5 branch:
```git
* master
develop
quynht
thuannd
namnt
```

## Đặt tên nhành feature

Lấy ví dụ về dev Nguyễn Đức Thuận:
- Khi thực hiện task `Đăng ký`: đứng từ branch `thuannd` để tạo ra 1 branch freature như sau: `thuannd/feature/register`
- Khi thực hiện task `Đăng nhập`: đứng từ branch `thuannd` để tạo ra 1 branch freature như sau: `thuannd/feature/login`

Lấy ví dụ về dev Trần Quỳnh:
- Khi thực hiện task `Cập nhật thông tin user`: đứng từ branch `quynht` để tạo ra 1 branch freature như sau: `quynht/feature/update-user-profile`
- Khi thực hiện task `Thay đổi ảnh đại diện`: đứng từ branch `quynht` để tạo ra 1 branch freature như sau: `quynht/feature/update-user-avatar`

Lấy ví dụ về dev Nguyễn Thành Nam:
- Khi thực hiện task `Quên mật khẩu`: đứng từ branch `namnt` để tạo ra 1 branch freature như sau: `namnt/feature/forgot-password`
- Khi thực hiện task `Thay đổi mật khẩu`: đứng từ branch `namnt` để tạo ra 1 branch freature như sau: `namnt/feature/change-password`
