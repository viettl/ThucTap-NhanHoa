# Managing VMs With Virsh
Dưới đây là một số lệnh để quản lý VM với virsh phổ biến:

## Xem trợ giúp
- Cú pháp: `virsh help <command>`
- Ví dụ: `virsh help list` - Hiển thị trợ giúp dưới dạng danh sách



## Hiển thị thông tin về hypervisor
- Cú pháp: `virsh nodeinfo`



## Liệt kê VM
- Cú pháp: `virsh list <command>`
- Ví dụ: `virsh list −−all`



## Bật VM
- Cú pháp: `virsh start <vmname>`
- Ví dụ: `virsh start CentOS-7_1908`



## Tắt VM
- Cú pháp: `virsh shutdown <vmname|id>`
- Ví dụ: `virsh shutdown CentOS-7_1908`



## Tắt nguồn VM
- Cú pháp: `virsh destory <vmname>`
- Ví dụ: `virsh destory CentOS-7_1908`



## Suspend/pause VM
- Cú pháp: `virsh suspend <vmname|id>`
- Ví dụ: `virsh suspend CentOS-7_1908`



## Tiếp tục VM
- Cú pháp: `virsh resume <vmname|id>`
- Ví dụ: `virsh resume CentOS-7_1908`

## Lưu một VM ra file
- Cú pháp: `virsh save <vmname>`
- Ví dụ: `virsh save CentOS-7_1908`



## Khôi phục VM từ file
- Cú pháp: `virsh restore <vmname>`
- Ví dụ: `virsh restore CentOS-7_1908`



## Xem thông tin VM
- Cú pháp: `virsh dominfo <vmname>`
- Ví dụ: `virsh dominfo CentOS-7_1908`

## Change the maximum memory allocation limit in the guest VM (Thay đổi giới hạn cấp phát bộ nhớ tối đa trong máy khách VM)
- Cú pháp: `virsh setmaxmem <vmname> <newmemsize> −−config`
- Ví dụ: `virsh setmaxmem CentOS-7_1908 4096M −−config`
- Ví dụ: `virsh setmaxmem CentOS-7_1908 4G −−config`



## Change the current memory allocation in the guest VM (Thay đổi cấp phát bộ nhớ hiện tại trong máy khách VM)
- Cú pháp: `virsh setmem <vmname> <newmemsize> −−config`
- Ví dụ: `virsh setmem CentOS-7_1908 4096M −−config`
- Ví dụ: `virsh setmem CentOS-7_1908 4G −−config`



## Edit the XML configuration for a guest VM (Chỉnh sửa cấu hình XML cho máy khách VM)
- Cú pháp: `virsh edit <vmname>`
- Ví dụ: `virsh edit CentOS-7_1908`



## Clone VM (Nhân bản VM)
- Cú pháp: `virt-clone -o <sourcevm> -n <destinationvm> -f <destination_disk_file>`
- Ví dụ: `virt-clone -o CentOS-7_1908 -n CentOS-7_1908-clone -f CentOS-7_1908-Clone.qcow2`



# Tài liệu tham khảo
- [kallesplayground.wordpress.com](https://kallesplayground.wordpress.com/useful-stuff/commands-for-kvm-management/)
- [libvirt.org](https://libvirt.org/sources/virshcmdref/html-single/)

# Missing
...