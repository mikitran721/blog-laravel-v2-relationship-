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

-   ask: chat.openai.com voi `how to define different data types to create table in laravel migrations`

## 3. Bảng có quan hệ với n được định nghĩa ntn trong Laravel

-   ask `how to create tables in laravel migration with one-one relationship`

## 4. Sinh fake data với các bảng có quan hệ

-   ask `how to make seeder with faker for tables in one to many relationship`
-   1. `php artisan make:model Phone -m` make Model with migration same name
-   2. change `Phone` migration with n-relationship
    -   `->unique` danh cho field co gia tri duy nhat | khong lap lai
-   3. Can tao them ModelFactory cho Model moi truoc khi sinh fake data:
    -   `php artisan make:factory PhoneFactory --model=Phone`
-   4. Sua noi dung ModelFactory moi tao
-   5. Tao Seeder chung cho 2 talbes tren
    -   `php artisan make:seeder UserPhoneSeeder`
-   6. Sua noi dung trong file Seeder phu hop
    -   ask `how to random phone number with fixed string length in Laravel faker`
-   7. Chay seeder moi tao `php artisan db:seed --class=UserPhoneSeeder`

# BỔ SUNG

-   Khi thay đổi lại table mà đã có data -> tạo migration có nội dung Update tương ứng với table cần edit & chạy lại. (lưu ý với dữ liệu mặc định hoặc cho phép null để tránh lỗi truy vấn data trước đó)
