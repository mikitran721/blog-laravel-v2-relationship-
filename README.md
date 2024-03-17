# CLONE: LARAVEL-BLOG-V2 (WITH RELATIONSHIP)

# TÌNH HUỐNG:

## 1. Tạo bảng (DB) có tên khác với tên Model

-   1. Tạo model với lệnh `php artisan make:model Post`
    -   Bo sung vao model moi tao ten tuong ung voi Tables `protected $table='blog_entries'`
-   2. Tạo Migration với tên bảng trong DB: `php artisan make:migration create_blog_entries_table`
-   3. Thực thi các migration `php artisan migrate`
-   4. Tao controller cho Post `php artisan make:controller PostController`
    -   khi nay can tu dinh nghia cac phuong thuc can thiet (do ko su dung tham so --resource)
    -   Co the xoa di tao lai

## 2. Các kiểu dữ liệu cần khai báo trong Migration

## 3. Bảng có quan hệ với n được định nghĩa ntn trong Laravel

## 4. Sinh fake data với các bảng có quan hệ
