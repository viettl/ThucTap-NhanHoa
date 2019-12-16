# OSQUERY TABLES SCHEMA

## LINUX
### User and Group
- [users](Linux.md#users): Chứa các thông tin về các tài khoản
- [last](Linux.md#last): Chứa thông tin về lịch sử đăng nhập của user
- [logged_in_users](Linux.md#logged_in_users): Lịch sử của những user có quyên shell hoạt động trên hệ thống.
- [user_events]()(EVENTED TABLE): Theo dõi các sự kiện của người dùng từ audit framework.
- [groups](Linux.md#groups): Chứa thông tin về các group trong hệ thống
- [user_groups](Linux.md#user_groups): Chứa mối quan hệ giữa các user và group



### Network
- [arp_cache](Linux.md#arp_cache): Chứa thông tin về cache phân giải địa chỉ, cả tĩnh và động (từ ARP, NDP).
- [interface_addresses](Linux.md#interface_addresses): Chứa thông tin về các network interface
- [interface_details](Linux.md#interface_details): Thông tin chi tiết và số liệu thống kê của các network interface
- [interface_ipv6](Linux.md#interface_ipv6): Thông tin về cấu hình IPv6 và số liệu thống kê về network interface
- [routes](Linux.md#routes): Bảng route hoạt động trên hệ thống
- [socket_events](Linux.md#socket_events): Thông tin sự kiện của các kết nối socket.
- [dns_resolvers](Linux.md#dns_resolvers): Danh sách DNS được phân giải bởi hệ thống.



### System Info
- [cpuid](Linux.md#cpuid): Useful CPU features from the cpuid ASM call.
- [cpu_time](Linux.md#cpu_time): Hiển thị thông tin từ tập tin `/Proc/stat` về thời gian các lõi cpu dành cho các phần khác nhau của hệ thống.
- [kernel_info](Linux.md#kernel_info): Thông tin cơ bản về kernel
- [kernel_modules](Linux.md#kernel_modules): Thông tin về các mô-đun hạt nhân Linux được tải.
- [load_average](Linux.md#load_average): Thông tin về mức trung bình tải của hệ thống.
- [os_version](Linux.md#os_version): Một hàng duy nhất chứa tên và phiên bản hệ điều hành.
- [system_info](Linux.md#system_info): Chứa thông tin về hệ thống.



### Firewall
- [iptables](Linux.md#iptables): Thông tin về iptable filtering và NAT tool



### Process
- [processes](Linux.md#processes): Thông tin về tất cả các tiến trình đang chạy trên hệ thống.
- [process_envs](Linux.md#process_envs): Bảng chứa key/value của các biến môi trường của mỗi process
- [process_events](Linux.md#process_events): Theo dõi thời gian và hành động của process.
- [process_file_events](Linux.md#process_file_events): Thông tin giáp sát sợ toàn vẹn của file sử dụng audit.
- [process_memory_map](Linux.md#process_memory_map): Thông tin về bộ nhớ của process được map với file và device/regions giả.
- [process_namespaces](Linux.md#process_namespaces): Linux namespaces của các tiến trình đang chạy trên hệ thống
- [process_open_files](Linux.md#process_open_files): Mô tả file cho mỗi process.
- [process_open_sockets](Linux.md#process_open_sockets): Thông tin về các tiến trình có sockets đang mở trên hệ thống.
- [listening_ports](Linux.md#listening_ports): Thông tin về cổng lắng nghe hoặc sockets của các tiến trình.



### Repository and Packages
- [apt_sources](Linux.md#apt_sources): Danh sách hiện tại của kho APT hoặc kênh phần mềm.
- [deb_packages](Linux.md#deb_packages): Dữ liệu về các gói deb đã được cài đặt.
- [rpm_packages](Linux.md#rpm_packages): Các gói RPM hiện đang được cài đặt trên hệ thống máy.
- [rpm_package_files](Linux.md#rpm_package_files): Các gói RPM hiện đang được cài đặt trên hệ thống máy.
- [python_packages](Linux.md#python_packages): Danh sách các gói Python được cài đặt trong hệ thống.
- [npm_packages](Linux.md#npm_packages): Liệt kê tất cả các gói npm trong một thư mục hoặc được cài đặt trên toàn cầu trong một hệ thống.
- [portage_packages](Linux.md#portage_packages): Danh sách các gói portage đã cài đặt.
- [atom_packages](Linux.md#atom_packages): Liệt kê tất cả các atom packages trong một thư mục hoặc được cài đặt trên toàn cầu trong một hệ thống.



### Security
- [authorized_keys](Linux.md#authorized_keys): Chứa thông tin của file authorized_keys được phân tích.
- [known_hosts](Linux.md#known_hosts): Chứa thông tin của file known_hosts được phân tích.
- [user_ssh_keys](Linux.md#user_ssh_keys): Chứa private keys trong thư mục `~/.ssh` và thông tin nó có được mã hóa hay không.
- [carves](Linux.md#carves): Forensic Carves.
- [shadow](Linux.md#shadow): Thông tin về mật khẩu của các user trong hệ thống được mã hóa và các thông tin liên quan.
- [sudoers](Linux.md#sudoers): Quy tắc (rules) chạy lệnh như những người dùng khác thông qua sudo.
- [selinux_events](Linux.md#selinux_events): Thông tin theo dõi các sự kiện của Selinux



### Configure
- [augeas](Linux.md#augeas): Các tập tin cấu hình được phân tích cú pháp bởi augeas.
- [crontab](Linux.md#crontab): Thông tin về cron/tab có trên hệ thống.
- [etc_hosts](Linux.md#etc_hosts): File `/etc/hosts` được phân tích.
- [etc_protocols](Linux.md#etc_protocols): File `/etc/protocols` được phân tích.
- [etc_services](Linux.md#etc_services): File `/etc/services` được phân tích.
- [ssh_configs](Linux.md#ssh_configs): Chứa thông tin cấu hình trong ssh_configs.



### Device and Storage
- [acpi_tables](Linux.md#acpi_tables): Bảng chức năng phổ biến và thông tin về Firmware ACPI.
- [block_devices](Linux.md#block_devices): Chặn (buffered access) các nút tệp thiết bị: disks, ramdisks, và DMG containers
- [carbon_black_info](Linux.md#carbon_black_info): Thông tin về cài đặt cảm biến Carbon Black.
- [device_file](Linux.md#device_file): Lưu trữ thông tin về các file thiết bị (device file)
- [device_hash](Linux.md#device_hash): Lưu trữ hàm băm của các file thiết bị
- [device_partitions](Linux.md#device_partitions): Sử dụng TSK để liệt kê chi tiết về các phân vùng trên thiết bị đĩa.
- [md_devices](Linux.md#md_devices): Thông tin về RAID
- [md_drives](Linux.md#md_drives): Thông tin về các drive thiết bị được sử dụng trong RAID.
- [md_personalities](Linux.md#md_personalities): Thông tin về cài đặt RAID phần mềm được hỗ trợ bởi kernel.



<details>
<summary>Ví dụ:</summary>

```

```
</details>