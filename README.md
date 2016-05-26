# Role Name

------------

ansible-bareos-client

# Description
-------------
Sử dụng role cho việc cài đặt và cấu hình file daemon trên các client node để thực hiện back up dữ liệu từ client về storage backend với sự quản lý tập trung của director 

Role thực hiện cài đặt và cầu hình:
* bareos-fd: file daemon để thực hiện backup dữ liệu trên client node
* Cấu hình client node join vào quản lý của 1 director

# Role Variables

--------------

Toàn bộ biến chương trình được lưu trong  defaults/main.yml

Có thể tùy biến các biến trong file này để phù hợp với các trường hợp cài đặt khác nhau

# Dependencies

------------

* Role viết cho cài đặt bareos trên Ubuntu 14.04
* Các cấu hình và cài đặt chạy với quyền root 

# Example Playbook

----------------

Phụ thuộc vào việc khai vào inventory trrong ansible:

Ví dụ test với VM Vagrant, host khai báo trong /etc/ansible/hosts, group [clients]:

    - hosts: clients
      remote_users: vagrant
      sudo: yes
      roles:
         - ansible-bareos-client


