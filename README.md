# Настройка NAT для IPv4  
## Топология  

<img width="1041" height="285" alt="image" src="https://github.com/user-attachments/assets/4d96adec-badf-482c-a1cd-49fb5322536e" />   

## Таблица адресации  

Устройство | Интерфейс | IP-адрес | Маска подсети  
--- | --- | --- | ---   
R1 | G0/0/0 | 209.165.200.230 | 255.255.255.248  
--- | G0/0/1 | 192.168.1.1 | 255.255.255.0  
R2 | G0/0/0 | 209.165.200.225 | 255.255.255.248  
--- | Lo1 | 209.165.200.1 | 255.255.255.224  
S1 | VLAN1 | 192.168.1.11 | 255.255.255.0  
S2 | VLAN1 | 192.168.1.12 | 255.255.255.0   
PC-A | NIC | 192.168.1.2 | 255.255.255.0  
PC-B | NIC | 192.168.1.3 | 255.255.255.0  

## Цели  

* Создание сети и настройка основных параметров устройства
* Настройка и проверка NAT для IPv4
* Настройка и проверка PAT для IPv4
* Настройка и проверка статического NAT для IPv4  

## Базовая настройка маршрутизаторов  
_R1_  
<img width="516" height="534" alt="image" src="https://github.com/user-attachments/assets/540e2c79-13d2-4bb6-b94e-433b1d1cb00c" />  
<img width="736" height="548" alt="image" src="https://github.com/user-attachments/assets/6f71d47d-f403-41db-bfda-f2213807af0c" />   
_R2_  
<img width="514" height="444" alt="image" src="https://github.com/user-attachments/assets/5c49ca2f-4758-40d7-b1e9-1747db1d0dd1" />  
<img width="920" height="469" alt="image" src="https://github.com/user-attachments/assets/505ebafd-2cf0-45d0-9288-51dbe086de53" />    
<img width="603" height="442" alt="image" src="https://github.com/user-attachments/assets/6cc81ca6-1847-4e25-aa3f-34565b30c1f7" />

## Настройка базовых параметров коммутаторов  
_S1_  
<img width="547" height="564" alt="image" src="https://github.com/user-attachments/assets/c821d2b7-0995-466b-8252-ddae14bf8e7b" />   
<img width="607" height="415" alt="image" src="https://github.com/user-attachments/assets/bf524908-2749-44f6-9fb4-6a93e00154ff" />  
<img width="693" height="158" alt="image" src="https://github.com/user-attachments/assets/72dc9026-3948-4995-9c01-64775cec6552" />  
Лишний Fa0/1 в диапозон засунул, включил  
_S2_   
<img width="546" height="450" alt="image" src="https://github.com/user-attachments/assets/009b7652-30ea-4e3b-8237-834da00b5aa0" />  
<img width="444" height="116" alt="image" src="https://github.com/user-attachments/assets/34702076-32b4-4e20-99b3-8a4c7592b4d7" />  
<img width="683" height="433" alt="image" src="https://github.com/user-attachments/assets/5666bde2-a430-4cb0-9149-761df1e03229" />  

## Настройка и проверка NAT для IPv4  

<img width="755" height="336" alt="image" src="https://github.com/user-attachments/assets/c6cf480d-7db2-42d8-9c31-d846fb8f4074" />  
<img width="506" height="243" alt="image" src="https://github.com/user-attachments/assets/42106a12-b51d-4638-bf79-92b667bea576" />  
<img width="638" height="118" alt="image" src="https://github.com/user-attachments/assets/9c39e2ab-996f-4a6f-882b-8729354d8c46" />  

_Во что был транслирован внутренний локальный адрес PC-B?_  
**209.165.200.1**   
_Какой тип адреса NAT является переведенным адресом?_  
**




 





  



