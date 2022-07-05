# Домашнее задание к занятию «Протокол обмена данными OPC»

### Цель задания

Опыт работы с ПО Modbustools полезен для осваивания скиллсета инженера по автоматизации по следующим задачам:

- настройка подключения устройств Modbus Slave к серверу OPC
- подключение программы-клиента OPC к серверу OPC и вывод данных из сервера.

Выполнив это задание, вы сможете:

1. Создать проект для обмена данными в программе MasterOPC Universal Modbus Server.
2. Произвести подключение программы-клиента MatrikonOPC Explorer к имеющимся в системе серверам OPC и проанализировать полученные данные.

------

### Чеклист готовности к домашнему заданию

1. Скачаны и установлены программы ModbusSlave, MasterOPC Universal Modbus Server, Matrikon OPC Explorer, UaExpert.

Ссылки на скачивание:

- [Modbus Slave Install 64bit](https://www.modbustools.com/download/ModbusSlaveSetup64Bit.exe "ModbusSlave Install 64bit") 
- [Modbus Slave Install 32bit](https://www.modbustools.com/download/ModbusSlaveSetup32Bit.exe "ModbusSlave Install 32bit")
- [MasterOPC Universal Modbus Server](https://insat.ru/products/Universal_MasterOPC/MODBUS_OPC_SERVER_32TAGS.ZIP "MasterOPC Universal Modbus Server (Zip)")
- [Matrikon OPC Explorer](https://www.matrikonopc.com/portal/downloads/product_software/MatrikonOPCExplorer.exe "Matrikon OPC Explorer")
- [Matrikon OPC HDA Explorer](https://www.matrikonopc.com/portal/downloads/product_software/MatrikonOPCHDAExplorer.exe "Matrikon OPC HDA Explorer")
- [UaExpert](https://www.unified-automation.com/fileadmin/files/client/uaexpert-bin-win32-x86-vs2008sp1-v1.6.2-438.zip)
 
**ВНИМАНИЕ!** Для программы Modbus Slave устанавливается демо-версия. Ее функционал будет ограничен спустя 30 дней после установки.
Производите установку программы **только** непосредственно перед началом выполнения задания.

Для большего удобства вы можете воспользоваться [инструкцией по работе с указанными программами](https://docs.google.com/presentation/d/11QxV0l43DA9arg-Cgt5VHUGv37IJ5phe7rsWiCeGaxE/edit?usp=sharing)

------

### Инструкция к выполнению домашнего задания

1. Сделайте копию [Шаблона для домашнего задания](https://docs.google.com/document/d/1VGv-wuG66a4pt6AyYub6ZOLp9t5KcV-U-1s5zsVD4-M/edit?usp=sharing) себе на Google Диск.
2. В названии файла введите корректное название лекции и вашу фамилию и имя.
3. Зайдите в «Настройки доступа» и выберите доступ «Просматривать могут все в Интернете, у кого есть ссылка».
 Ссылка на инструкцию [Как предоставить доступ к файлам и папкам на Google Диске](https://support.google.com/docs/answer/2494822?hl=ru&co=GENIE.Platform%3DDesktop)
4. Скопируйте текст задания в свой документ.
5. Выполните домашнее задание, запишите ответы и приложите необходимые скриншоты в свой Google Doc.
6. Для проверки домашнего задания преподавателем отправьте ссылку на ваш документ в личном кабинете.
7. Любые вопросы по решению задач задавайте в чате учебной группы.

------

### Инструменты/ дополнительные материалы, которые пригодятся для выполнения задания

1. [Google Drive](https://www.google.com/intl/ru/drive/)
2. Программы ModbusSlave, MasterOPC Universal Modbus Server, Matrikon OPC Explorer, UaExpert:
- [Modbus Slave Install 64bit](https://www.modbustools.com/download/ModbusSlaveSetup64Bit.exe "ModbusSlave Install 64bit") 
- [Modbus Slave Install 32bit](https://www.modbustools.com/download/ModbusSlaveSetup32Bit.exe "ModbusSlave Install 32bit")
- [MasterOPC Universal Modbus Server](https://insat.ru/products/Universal_MasterOPC/MODBUS_OPC_SERVER_32TAGS.ZIP "MasterOPC Universal Modbus Server (Zip)")
- [Matrikon OPC Explorer](https://www.matrikonopc.com/portal/downloads/product_software/MatrikonOPCExplorer.exe "Matrikon OPC Explorer")
- [Matrikon OPC HDA Explorer](https://www.matrikonopc.com/portal/downloads/product_software/MatrikonOPCHDAExplorer.exe "Matrikon OPC HDA Explorer")
- [UaExpert](https://www.unified-automation.com/fileadmin/files/client/uaexpert-bin-win32-x86-vs2008sp1-v1.6.2-438.zip)
3. [Инструкция по работе с программами ModbusSlave, MasterOPC Universal Modbus Server, Matrikon OPC Explorer, UaExpert]((https://docs.google.com/presentation/d/11QxV0l43DA9arg-Cgt5VHUGv37IJ5phe7rsWiCeGaxE/edit?usp=sharing)
4. [Шаблон для домашнего задания](https://docs.google.com/document/d/1VGv-wuG66a4pt6AyYub6ZOLp9t5KcV-U-1s5zsVD4-M/edit?usp=sharing)

------

### Задание 1

Производитель комплексного прибора, измеряющего параметры окружающей среды (температуру воздуха, атмосферное давление, относительную влажность, скорость ветра), предоставил данные для связи с этим устройством по Modbus TCP:

- температура - 30005
- давление - 30006
- влажность - 30008
- скорость ветра - 30009.

Инженеру АСУ ТП в программе MasterOPC Universal Modbus Server необходимо создать новый рабочий проект с конфигурацией, позволяющей установить связь с двумя экземплярами виртуальной модели этого прибора с указанными ниже параметрами. Получите данные о температуре, давлении и проч. с каждого из приборов:

Экземпляр 1:

- Протокол - Modbus TCP
- Slave ID = 7
- Port = 504

Экземпляр 2:

- Протокол - Modbus TCP
- Slave ID = 8
- Port = 505

Для проверки работоспособности этой конфигурации необходимо запустить два экземпляра программы Modbus Slave, в каждом из которых необходимо создать виртуальное устройство с указанными выше параметрами. Присвойте им следующие значения (единицы измерения не вносятся в конфигурацию, они даны для пояснения):

Экземпляр 1:

- температура = 18 (градусов)
- давление = 99 (кПа)
- влажность = 60 (%)
- скорость ветра = 2 (м/с)

Экземпляр 2: 

- температура = 22 (градуса)
- давление = 101 (кПа)
- влажность = 80 (%)
- скорость ветра = 4 (м/с)

Убедитесь в работоспособности схемы «Сервер OPC - два экземпляра виртуальных приборов», произведя их соединение (для сервера - выбором команды «Старт», для каждого из экземпляров Modbus Slave - переводом в статус «Connected») и проверив идентичность отправляемых и получаемых данных.

Ответ приведите в виде файлов конфигурации, созданных в программах MasterOPC Universal Modbus Server и Modbus Slave (каждого из экземпляров).

Файлы конфигурации необходимо сохранить в Google Drive, сделав их доступными для загрузки.

В шаблоне для домашнего задания приведите ссылки на данные файлы.

В названиях файлов конфигурации укажите свою фамилию, имя и тему занятия следующим образом: StudentName_LectureN_xxx.*
(например, IvanovPetr_Lecture2_5_001.mbs).

------

### Задание 2

1. Внесите изменения в рабочий проект MasterOPC Universal Modbus Server из задания 1, сделав теги температуры каждого из приборов архивируемыми.
2. При помощи программы Matrikon OPC Explorer произведите подключение к доступному серверу OPC DA, выведя значения всех тегов.
3. Спустя 5 минут при помощи программы Matrikon OPC HDA Explorer произведите подключение к доступному серверу OPC HDA, выведя значения тегов температуры с обоих приборов за последние 5 минут.
4. Ответ приведите в виде скриншотов программ Matrikon OPC Explorer, Matrikon OPC HDA Explorer.

------

### Задание 3 * (необязательное)

1. В программе MasterOPC Universal Modbus Server в рабочий проект внесите изменения, позволяющие включить в работу сервер OPC UA.
2. Скачайте и установите программу UaExpert.
3. Подключитесть с ее помощью к серверу OPC UA.
4. Ответ приведите в виде скриншота программы UaExpert.

------

### Правила приёма работы

1. Отправлена ссылка на документ (Google Doc) с выполненным заданием в личном кабинете.
2. Документ размещён на личном Google Диске.
3. К документу настроены права доступа «Просматривать могут все в Интернете, у кого есть ссылка».

------

### Критерии оценки

1. Задание 1 считается выполненным, если при загрузке конфигураций в программы MasterOPC Universal Modbus Server, Modbus Slave (оба экземпляра) и включении режимов «Старт» и «Connect» соответственно происходит корректное чтение данных сервером OPC из устройств Modbus Slave, а на основных экранах этих программ выдаются указанные в условии значения параметров.
2. Задание 2 считается выполненным, если после настройки программ-клиентов OPC на них отображаются те же данные, что и на сервере OPC.
