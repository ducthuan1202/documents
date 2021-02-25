## Các branch cơ bản

![gitwordflow](https://wac-cdn.atlassian.com/dam/jcr:b5259cce-6245-49f2-b89b-9871f9ee3fa4/03%20(2).svg?cdnVersion=966)

- `master`: là nhánh chính, sử dụng để lưu lại từng cột mốc trong dự án.
- `develop`: là nhánh phát triển, nhánh này sẽ gốc khi chúng ta tạo 01 nhánh mới để code tính năng. Và cũng là nơi chúng ta sẽ gộp (merge) code sau khi đã hoàn thành.
- `user_branch`: là nhánh cá nhân của từng người, hoặc có thể là nhánh của 01 feature, hotfix, ... đây là nhánh chúng ta sẽ code trực tiếp.

## Tag
- Tag trong git sử dụng để đánh dấu 01 phiên bản ở một thời điểm nào đó. Nó là cột mốc cho một giai đoạn phát triển của sản phẩm. Nếu sử dụng tag, chúng ta có thể checkout về đúng thời điểm đánh dấu để hotfix issue hay fix bug cho bản release đó.

## Quy trình

Clone dự án từ git về máy
```bash
# dùng ssh
git clone git@github.com:ducthuan1202/golang.git

# dùng https
https://github.com/ducthuan1202/golang.git
```

Checkout tới branch cá nhân từ develop branch
```bash
# chuyển sang nhánh develop
git checkout develop 

# tạo mới nhánh của bản thân
git checkout -b user_branch

# hoặc checkout sang nếu branch đã tồn tại
git checkout user_branch
```

Sau mỗi khi hoàn thành chức năng hoặc đơn giản là cần lấy code mới nhất
```bash

# kéo code từ nhánh develop trên server về và merge với nhánh hiện tại
git pull origin develop 
```

_Nếu như xảy ra conflict, chúng ta có thể kiểm tra từng file để chắc chắn việc sẽ lấy code của mình hay của người khác_
```bash
# lấy code của người khác 
git checkout --theirs

# lấy code của mình 
git checkout ours
```

Đẩy code mới nhất lên develop 
```bash
git push origin develop
```

> Trường hợp checkout để xử lý conflict code chỉ nên dùng cho những lần conflict đơn giản. 

**Khuyến cáo nên kiểm tra conflict bằng mắt thường kỹ lưỡng và xử lý thủ công để đảm bảo không bị mất code, lỗi code sau khi xử lý merge**
