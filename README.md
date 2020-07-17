# check_pmg_services
Proxmox MG 服務檢查，支援 Nagios/LibreNMS/Icinga2。  
主要寫給 LibreNMS 使用，以 check_nrpe 進行 Proxmox MG 重要服務檢查。    

Proxmox MG Service Check with Nagios/LibreNMS/Icinga2 support.
Primarily for use with LibreNMS, with check_nrpe for Proxmox MG important service check.  

   
&nbsp;&nbsp;
&nbsp;&nbsp;
  

## 檢查項目 Check items
* `clamav-freshclam.service (ClamAV virus database updater)`
* `pmg-smtp-filter.service (Proxmox SMTP Filter Daemon)`
* `pmgdaemon.service (Proxmox Mail Gateway API Daemon)`
* `pmgmirror.service (Proxmox Mail Gateway Database Mirror Daemon)`
* `pmgpolicy.service (Proxmox Mail Gateway Policy Daemon)`
* `pmgproxy.service (Proxmox Mail Gateway API)`
* `pmgtunnel.service (Proxmox Mail Gateway Cluster Tunnel Daemon)`
* `postfix@-.service (Postfix Mail Transport Agent (instance -))`
* `rsyslog.service (System Logging Service)`
* `ssh.service (OpenBSD Secure Shell server)`


   
&nbsp;&nbsp;
&nbsp;&nbsp;
   
## 使用方式 Usage

請使用以下指令，參數 -c 後任意值皆可。
只要有任一上述檢查項目的服務沒有正常運作，即視為服務異常。
  
```./check_pmg_services -c 1```

   
&nbsp;&nbsp;
&nbsp;&nbsp;
  
