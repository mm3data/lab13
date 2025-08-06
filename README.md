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
<img width="533" height="505" alt="image" src="https://github.com/user-attachments/assets/1c160b5e-5ea7-4d46-a64c-039612d4fa59" />  
<img width="776" height="782" alt="image" src="https://github.com/user-attachments/assets/56f49518-a54d-4dd1-909f-99570d17c933" />  
  
_R2_  
<img width="538" height="521" alt="image" src="https://github.com/user-attachments/assets/574fd221-d474-4573-b251-c538e9a75109" />  
<img width="753" height="716" alt="image" src="https://github.com/user-attachments/assets/5f4521ce-72b5-4eb2-9695-93e46296a1eb" />  

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

<img width="756" height="402" alt="image" src="https://github.com/user-attachments/assets/e903f939-6f87-4c8e-9df0-bdfc52cc8de7" />  
<img width="538" height="298" alt="image" src="https://github.com/user-attachments/assets/7523a4f2-300b-4cc8-b840-c93344f948d1" />  
 
_Во что был транслирован внутренний локальный адрес PC-B?_  
**209.165.200.226**   
_Какой тип адреса NAT является переведенным адресом?_  
**inside global**  

<img width="622" height="140" alt="image" src="https://github.com/user-attachments/assets/ea803a5b-f916-499d-8b4d-a6b5a7b212ab" />  
<img width="698" height="418" alt="image" src="https://github.com/user-attachments/assets/9b5a9096-d1fe-47c9-b69e-fca455b1aa22" />  
<img width="621" height="240" alt="image" src="https://github.com/user-attachments/assets/a8fd0297-d9d5-47e9-a229-e5fed0b6727f" />    
<img width="579" height="120" alt="image" src="https://github.com/user-attachments/assets/cf318cf1-b63f-46e4-bbdb-04fa4abebc0b" />   




 




 





  



