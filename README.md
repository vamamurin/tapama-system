# Multi-layered SOC & Virtualization Architecture

## 🚧 Project Status
![Under Construction](https://img.shields.io/badge/status-under%20construction-yellow?style=for-the-badge)

> ⚠️ This project is currently in progress. Documentation may be incomplete or subject to change.


## Tổng quan
Dự án mô phỏng một môi trường SOC (Security Operations Center) quy mô nhỏ sử dụng ảo hóa và phân vùng mạng. Mục tiêu là minh họa cách giám sát và phát hiện tấn công trên nhiều lớp trong một hệ thống thực tế.

## Kiến trúc hệ thống
- Hypervisor: Proxmox VE (VM & LXC)
- Phân vùng mạng:
  - LAN
  - DMZ
  - Database Zone
  - Management Zone
- Firewall: pfSense (DHCP, DNS, NAT, VLAN trunking)

## Hệ thống bảo mật
- IDS: Snort (triển khai tại gateway)
- SIEM: Wazuh Server
- Giám sát endpoint: Wazuh Agent trên các máy ảo

![SOC Architecture](./images/soc_model.jpg)

## Tính năng chính
- Phân tách mạng bằng VLAN để cô lập các vùng quan trọng
- Áp dụng mô hình defense-in-depth (nhiều lớp bảo vệ)
- Thu thập và phân tích log tập trung qua SIEM
- Phát hiện các tấn công mô phỏng:
  - Quét mạng (Nmap)
  - SSH brute-force

## Ứng dụng
- Phân tích log và cảnh báo
- Mô phỏng quy trình phát hiện sự cố (SOC workflow)
- Hiểu cách hoạt động của hệ thống giám sát an ninh
- 
## Tài liệu
Xem chi tiết tại: [https://github.com/vamamurin/tapama-system/blob/main/TTDACN.pdf]
## 👥 Team Members
- Nguyen Duc Manh
- Luong Minh Tan
- Trinh Vo Tan Phat

