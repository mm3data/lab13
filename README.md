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

## Запрос с PC-B на R2   

<img width="693" height="409" alt="image" src="https://github.com/user-attachments/assets/1e48a946-0dfd-4bac-8251-f32b86c17708" />  
<img width="627" height="163" alt="image" src="https://github.com/user-attachments/assets/7cb5f0f3-c91f-4157-bc52-35799f1d36c7" />  

*Во что был транслирован внутренний локальный адрес PC-B?*  
_209.165.200.226_   
*Какой тип адреса NAT является переведенным адресом?*  
_Inside global_  

## Запрос с PC-A на R2  

<img width="709" height="418" alt="image" src="https://github.com/user-attachments/assets/01f1b48e-7142-40b5-bc2b-93bd75dd6df4" />  
<img width="627" height="173" alt="image" src="https://github.com/user-attachments/assets/a9ec1137-45f7-4ea0-9b26-ddedc9066db9" />  

<img width="604" height="144" alt="image" src="https://github.com/user-attachments/assets/1dc375b9-9721-4515-9541-dade9a0e13e5" />  
<img width="624" height="270" alt="image" src="https://github.com/user-attachments/assets/bb3ba286-a7e7-4049-bb07-c97eb17b208d" />  
<img width="620" height="135" alt="image" src="https://github.com/user-attachments/assets/725238ac-d763-4e66-945e-5b2e8de92c54" />  
<img width="398" height="243" alt="image" src="https://github.com/user-attachments/assets/917fc027-ddd9-471d-b1b7-e7fb04065396" />  

## Настройка PAT    

<img width="566" height="63" alt="image" src="https://github.com/user-attachments/assets/b19cf742-7bbb-44d7-89cf-1d3bdfa44760" />  

## Ping с PC-A и PC-B   

<img width="624" height="262" alt="image" src="https://github.com/user-attachments/assets/932d6d6b-063d-4f6d-9177-f8f4e2c3f41d" />   

## Во что был транслирован внутренний локальный адрес PC-B?    

_209.165.200.226_  

## Какой тип адреса NAT является переведенным адресом?   

_Inside global_  


<img width="673" height="821" alt="image" src="https://github.com/user-attachments/assets/fda14ccb-ba99-4889-b1f7-f50660319dd2" />   

## Как маршрутизатор отслеживает, куда идут ответы?  

_Присваиваеться номер порта_  

<img width="570" height="174" alt="image" src="https://github.com/user-attachments/assets/0af142e3-0454-4cb4-8e89-56e94973c61e" />  
<img width="496" height="209" alt="image" src="https://github.com/user-attachments/assets/807d75d7-a438-4350-a8bf-dfb86b98f9a8" />  
<img width="669" height="130" alt="image" src="https://github.com/user-attachments/assets/41d97a9a-93d1-498b-833c-a1ca2b737fff" />  
<img width="1080" height="671" alt="image" src="https://github.com/user-attachments/assets/3ce1e18a-9e44-402e-84d8-87491140bd4f" />  
<img width="674" height="675" alt="image" src="https://github.com/user-attachments/assets/eba67739-8f03-49be-ad10-d3a96e3607ee" />   

## Настройка статического NAT для IPv4      

<img width="553" height="66" alt="image" src="https://github.com/user-attachments/assets/b9d31715-9082-4590-8714-3dbde9d4fe1e" />  
<img width="646" height="81" alt="image" src="https://github.com/user-attachments/assets/84fae1ea-b63e-4527-a7e8-5b2c7684de01" />  
<img width="604" height="132" alt="image" src="https://github.com/user-attachments/assets/e0972261-9af9-4d93-bc34-3e20e9fa8e55" />  
<img width="657" height="125" alt="image" src="https://github.com/user-attachments/assets/2bb24ac6-eeda-4f56-a4ae-3efa9cd3fd33" />  







  














 




 





  



