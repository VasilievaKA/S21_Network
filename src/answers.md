## Часть 1 
**1.1.1**  92.167.38.54   
**1.1.2**	  
* 255.255.255.0 - 24, 11111111.11111111.11111111.00000000  
* /15 - 255.254.0.0, 11111111.11111110.00000000.00000000  
* 11111111.11111111.11111111.11110000 - 255.255.255.240, /28  

**1.1.3**	  
/8 - 12.0.0.1  
/16 - 12.167.0.1  
/23 - 12.167.38.1  
/4 - 0.0.0.1  

**1.2**  
194.34.23.100 - нет  
127.0.0.2 - да  
127.1.0.1 - да  
128.0.0.1 - нет  

**1.3.1**  
10.0.0.45 - частный  
134.43.0.2 - публичный  
192.168.4.2 - частный  
172.20.250.4 - частный  
172.0.2.1 - частный  
192.172.0.1 - частный  
172.68.0.2 - частный  
172.16.255.255 - частный  
10.10.10.10 - частный  
192.169.168.1 - частный  

**1.3.2**  
10.0.0.1 - нет  
10.10.0.2 - да  
10.10.10.10 - нет  
10.10.100.1 - нет  
10.10.1.255 - нет  
## Часть 2 

**2.0 С помощью команды ip a посмотреть существующие сетевые интерфейсы**    
2.0.1 Отчет вывода команды ip a для машины ws1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/1wsl2.png)   
2.0.2 Отчет вывода команды ip a для машины ws2     
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/1wsl2.png)   
2.0.3 Установка для машины ws1 адреса 192.168.100.10/16 и для машины ws2 адреса 172.24.116.8/12    
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/2wsl1-2.png)    
2.0.4 Выполнение команды natplan apply для машины ws1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/3wsl1.png)    
2.0.5 Выполнение команды natplan apply для машины ws2    
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/3wsl2.png)   

**2.1. Добавление статического маршрута вручную**   
2.1.1 Добавление статического маршрута от машины ws1 к ws2. Вывод результата пингования   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/4wsl1.png)    
2.1.2 Добавление статического маршрута от машины ws2 к ws1. Вывод результата пингования   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/4wsl2.png)    

**2.2. Добавление статического маршрута с сохранением**    
2.2.1 Добавление статического маршрутка от машины ws1 к ws2 и  от машины ws2 к ws1 после перезапуска
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/5wsl1-2.png)    
2.2.3 Принятие изменений для машины ws1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/6wsl1.png)    
2.2.4 Принятие изменений для машины ws1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/6wsl2.png)    
2.2.5 Вывод результата пингования машины ws2 к ws1 и от машины ws1 к ws2   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/7wsl1-2.png)   

## Часть 3   
**3.1. Скорость соединения** 

* 8 Mpbs = 1 MB/s  
* 100 MB/s = 800000 Kbps  
* 1 Gbps = 1000 Mbps    

**3.2. Утилита iperf3**  
3.2.1 Установка машины ws1 как сервер при помощи команды iperf3 -s с последующим измерением скорости соединения. Установка машины ws2 как принимающего устройства при помощи команды iperf3 -c 192.168.100.10 -p 5201 с последующим измерением скорости соединения    
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/8wsl1-2.png)    


## Часть 4 
**4.1. Утилита iptables**   
4.1.1 Файл firewall.sh с содержимым для машины ws1 и с содержимым для машины ws2   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/9wsl1-2.png)    
4.1.3 Запуск команды sudo chmod +x /etc/firewall.sh && sudo sh /etc/firewall.sh для машин ws1 и ws2   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/10wsl1-2.png)     

**Стратегия для ws1:**   
* на ws1 применить стратегию когда в начале пишется запрещающее правило, а в конце пишется разрешающее правило (это касается пунктов 3 и 4)
* открыть на машинах доступ для порта 22 (ssh) и порта 80 (http)
* запретить echo reply (машина не должна "пинговаться”, т.е. должна быть блокировка на OUTPUT)
* разрешить echo reply (машина должна "пинговаться")

**Стратегия для ws2:**   
* на ws2 применить стратегию когда в начале пишется разрешающее правило, а в конце пишется запрещающее правило (это касается пунктов 3 и 4)
* открыть на машинах доступ для порта 22 (ssh) и порта 80 (http)
* запретить echo reply (машина не должна "пинговаться”, т.е. должна быть блокировка на OUTPUT)
* разрешить echo reply (машина должна "пинговаться")

**4.2. Утилита nmap**  
Командой ping найти машину, которая не "пингуется", после чего утилитой nmap показать, что хост машины запущен   
4.2.1 Пропинговываем машину ws1. Пропинговываем машину ws2. Вызываем функцию nmap для поверки подключения порта.   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/11wsl1-2.png)      

## Часть 5
**5.1. Настройка адресов машин**   
5.1.1 Содержание файла etc/netplan/00-installer-config.yaml для машины ws11   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/12ws11.png)      
5.1.2 Содержание файла etc/netplan/00-installer-config.yaml для машины ws21   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/ws21-routes.png)    
5.1.3 Содержание файла etc/netplan/00-installer-config.yaml для машины ws22   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/ws22-routes.png)  
5.1.4 Содержание файла etc/netplan/00-installer-config.yaml для машины r1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/r1.png)   
5.1.5 Содержание файла etc/netplan/00-installer-config.yaml для машины r2   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/r2.png)   
5.1.6 Адрес машины ws11 после перезапуска   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/photo_2023-03-08_16-12-39.jpg)   
5.1.7 Адрес машины ws21 после перезапуска   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/photo_2023-03-08_16-12-39(3).jpg)    
5.1.8 Адрес машины ws22 после перезапуска   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/photo_2023-03-08_16-12-39(4).jpg)   
5.1.9 Адрес машины r1 после перезапуска   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/r1_2.png)   
5.1.10 Адрес машины r2 после перезапуска   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/r2_2.png)   

**5.2. Включение переадресации IP-адресов**   
5.2.1 Вызов команды sudo sysctl -w net.ipv4.ip_forward=1 для машин r1 и r2   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/r1-r2.png)   

5.2.2 Скрин с содержание измененного файла /etc/sysctl/conf   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/r1-r2_2.png)   

**5.3. Установка маршрута по-умолчанию**    
5.3.1 Содержание файла etc/netplan/00-installer-config.yaml на машине ws11   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/ws11-gateway.png)    
5.3.2 Содержание файла etc/netplan/00-installer-config.yaml на машине ws21   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/ws21-gateway.png)   
5.3.3 Содержание файла etc/netplan/00-installer-config.yaml на машине ws22   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/ws22-gateway.png)   
5.3.4 Отчет команды ip r на машинах ws11, ws21, ws22   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/photo_2023-03-08_16-12-41(2).jpg)    
5.3.5 Пинг с ws11 роутера r2  
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/photo_2023-03-08_16-12-41(3).jpg)   
5.3.6 Проверка, что пинг доходит до r2   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_1.png)    

**5.4. Добавление статических маршрутов**   
5.4.1 Содержание файла etc/netplan/00-installer-config.yaml для машины r1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_2.png)   
5.4.2 Содержание файла etc/netplan/00-installer-config.yaml для машины r2   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_3.png)  
5.4.3 Вывод команды ip r для машины r2
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_4.png)    
5.4.4 Вывод команды ip r для машины r1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_5.png)   
5.4.5 Вывод команд ip r list 10.10.0.0/18 и ip r list 0.0.0.0/0 на машине ws11   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/photo_2023-03-08_16-12-42.jpg)   

Для адреса 10.10.0.0/[порт сети] был выбран маршрут, отличный от 0.0.0.0/0, потому что маска /18 описывает маршрут к сети точнее, в отличие от маски /0   

**5.5. Построение списка маршрутизаторов**   
5.5.1 Вывод команды traceroute 10.20.0.10 -n на машине ws11   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_6.png)   
5.5.2 Вывод команды tcpdump -tnv -i eth0 на машине r1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_7.png)   

**Принцип работы traceroute**

Для определения промежуточных маршрутизаторов traceroute отправляет серию пакетов данных целевому узлу, при этом каждый раз увеличивая на 1 значение поля TTL («время жизни»). Это поле обычно указывает максимальное количество маршрутизаторов, которое может быть пройдено пакетом. Первый пакет отправляется с TTL, равным 1, и поэтому первый же маршрутизатор возвращает обратно сообщение ICMP, указывающее на невозможность доставки данных. Traceroute фиксирует адрес маршрутизатора, а также время между отправкой пакета и получением ответа (эти сведения выводятся на монитор компьютера). Затем traceroute повторяет отправку пакета, но уже с TTL, равным 2, что позволяет первому маршрутизатору пропустить пакет дальше.  
Процесс повторяется до тех пор, пока при определённом значении TTL пакет не достигнет целевого узла. При получении ответа от этого узла процесс трассировки считается завершённым.   

**5.6. Использование протокола ICMP при маршрутизации**   
5.6.1 Вывод команды ping -c 1 10.30.0.111 на машине ws11   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_9.png)   
5.6.2 Вывод команды tcpdump -n -i eth0 icmp на машине r1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/new.png)   

## Часть 6  
6.1 Изменение файла /etc/dhcp/dhcpd.conf   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_12.png)   
6.2 Изменение файла /etc/resolv.conf   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_13.png)    
6.3 Перезагрузка службы DHCP при помощи команды systemctl restart isc-dhcp-server   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_14.png)   
6.4 После перезагрузки машины ws21 проверяем получение адресса   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_15.png)   
6.5 Результат пинга машины ws22 с ws21   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_16.png)   
6.6 Изменение файла etc/netplan/00-installer-config.yaml для машины ws11   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_17.png)   
6.7 Изменение файла /etc/dhcp/dhcpd.conf для машины r1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_19.png)    
6.8 Перезагрузка службы DHCP при помощи команды systemctl restart isc-dhcp-server   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_18.png)   
6.9 После перезагрузки машины ws11 проверяем получение адресса   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_20.png)   
6.10  ip машины ws21 до обновления   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_21.png)   
6.11 Обновление адреса для машины ws21 при помощи запроса его у dhcp сервера при помощи команды sudo dhclient eth0. ip машины ws21 после обновления.   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_22.png)   

## Часть 7   

7.1 Изменение файла /etc/apache2/ports.conf на машинах ws22 и r1
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_23.png)   
7.2 Вызов команды service apache2 start на машинах ws22 и r1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_24.png)   
7.3 Добавление файла firewall.sh на машине r2
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/firewall1.png)   
7.4 Запуск измененного файла firewall.sh на машине r2
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/firewall3.png)   
7.5 Проверка соединения между ws22 и r1. Соединение не проходит
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_27.png)     
7.6 Добавление правила на разрешение маршрутизации в файл firewall.sh на машине r2.    
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/firewall2.png)   
7.7 Проверка соединения между ws22 и r1 после добавления правила на разрешение маршрутизации пакетов протокола ICMP. Соединение проходит   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_29.png)   
7.8 Добавление правил:
* Включить SNAT, а именно маскирование всех локальных ip из локальной сети, находящейся за r2 (по обозначениям из Части 5 - сеть 10.20.0.0)
Совет: стоит подумать о маршрутизации внутренних пакетов, а также внешних пакетов с установленным соединением   
* Включить DNAT на 8080 порт машины r2 и добавить к веб-серверу Apache, запущенному на ws22, доступ извне сети   

![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_30.png)      
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_31.png)   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_32.png)   
7.9 Проверка соединения машины ws22 с r1   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_33.png)   
7.7 Проверка соединения машины r1 с ws22   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_34.png)

## Часть 8 
8.1 Включила apache на машине ws22 и проверила статус   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_35.png)   
8.2 Выполнение Local TCP forwarding   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_36.png)   
8.3 Выполнение Remote TCP forwarding   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_38.png)   
8.4 Проверка подключения   
![](https://repos.21-school.ru/students/DO2_LinuxNetwork.ID_356275/biancara_student.21_school.ru/DO2_LinuxNetwork-0/-/raw/develop/src/pictures/Screenshot_37.png)   
 
