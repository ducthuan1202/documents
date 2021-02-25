# Các quy tắc chung

![gitwordflow](https://wac-cdn.atlassian.com/dam/jcr:b5259cce-6245-49f2-b89b-9871f9ee3fa4/03%20(2).svg?cdnVersion=966)


## Branch
- `master`: là nhánh chính, sử dụng để lưu lại từng cột mốc trong dự án. Đây là nhánh mặc định khi tạo mới 01 repository trên git.
- `develop`: là nhánh phát triển, nhánh này sẽ gốc khi chúng ta tạo 01 nhánh mới để code tính năng. Và cũng là nơi chúng ta sẽ gộp (merge) code sau khi đã hoàn thành.
- `user_branch`: là nhánh cá nhân của từng dev khi tham gia vào dự án.
- `feature_branch`: là nhánh mà chúng ta sẽ code trực tiếp 01 tính năng cụ thể nào đó.
- `hotfix_branch`: là nhánh fix bug tại 1 thời điểm nào đó sau khi chúng ta đã commit tính năng này trước đó.

## Tag
- Tag trong git sử dụng để đánh dấu 01 phiên bản ở một thời điểm nào đó. 
- Nó là cột mốc cho một giai đoạn phát triển của sản phẩm. Nếu sử dụng tag, chúng ta có thể checkout về đúng thời điểm đánh dấu để hotfix issue hay fix bug cho bản release đó.

## Quy ước đặt tên chung
Có nhiều quy ước đặt tên khác nhau, tùy theo từng người đứng đầu dự án quy định, nhưng cơ bản nó vẫn tuân theo các quy tắc sau:

- Tên branch chỉ nên bao gồm các chữ cái viết thường từ a-z, các số từ 0-9 và dấu gạch chéo (/) và gạch ngang (-)
- Các nhánh các nhân là tên người + chữ cái đầu tiền của họ và tên đệm. Ví dụ: Nguyễn Đức Thuận => `thuannd`
- Các nhánh feature cần có tiền tố `feature` phía trước. Ví dụ: tính năng login => `feature/login`
- Các nhánh hotfix cần có tiền tố `hotfix` phía trước. Ví dụ: tính năng thay đổi thời gian remember login => `hotfix/fix-remember-login`
