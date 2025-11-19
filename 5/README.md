# Домашнее задание к занятию «Протокол обмена данными OPC»

### Цель задания

Опыт работы с ПО ModbusTools полезен для осваивания скиллсета инженера по автоматизации по следующим задачам:

- настройка подключения устройств Modbus Slave к серверу OPC,
- подключение программы-клиента OPC к серверу OPC и вывод данных из сервера.

Выполнив это задание, вы сможете:

1. Создать проект для обмена данными в программе MasterOPC Universal Modbus Server.
2. Произвести подключение программы-клиента MatrikonOPC Explorer к имеющимся в системе серверам OPC и проанализировать полученные данные.

------

### Чеклист готовности к домашнему заданию

1. Скачаны и установлены программы ModbusSlave, MasterOPC Universal Modbus Server, Matrikon OPC Explorer, UaExpert.

Ссылки на скачивание:

- [Modbus Slave Install 64bit](https://www.modbustools.com/download/ModbusSlaveSetup64Bit.exe "ModbusSlave Install 64bit"),
- [Modbus Slave Install 32bit](https://www.modbustools.com/download/ModbusSlaveSetup32Bit.exe "ModbusSlave Install 32bit"),
- [MasterOPC Universal Modbus Server](https://insat.ru/products/Universal_MasterOPC/MODBUS_OPC_SERVER_32TAGS.ZIP "MasterOPC Universal Modbus Server (Zip)"),
- [Matrikon OPC Explorer](https://www.matrikonopc.com/portal/downloads/product_software/MatrikonOPCExplorer.exe) (требуется предварительная регистрация),
- [Matrikon OPC HDA Explorer](https://www.matrikonopc.com/portal/downloads/product_software/MatrikonOPCHDAExplorer.exe) (требуется предварительная регистрация),
- [UaExpert](https://www.unified-automation.com/fileadmin/files/client/uaexpert-bin-win32-x86-vs2008sp1-v1.6.3-448.zip) (требуется предварительная регистрация).

<details>
 <summary> Если у вас возникают сложности с установкой указанных программ, воспользуйтесь ссылками ниже (нажмите на эту строку) </summary>

 
 
 [MatrikonOPCExplorer](https://disk.360.yandex.ru/d/yY3Vv3aE2Y3vXA)
 
 [MatrikonOPCHDAExplorer](https://disk.360.yandex.ru/d/K9mq9_Q-t5p7ew)
 
 [uaexpert-bin-win32-x86-vs2008sp1-v1.6.1-424](https://disk.360.yandex.ru/d/vv2DjSGKpGJCEw)
 

 </details>
 
**ВНИМАНИЕ!** Для программы Modbus Slave устанавливается демоверсия. Её функционал будет ограничен спустя 30 дней после установки.
Производите установку программы **только** непосредственно перед началом выполнения задания.

Для большего удобства вы можете воспользоваться [инструкцией по работе с указанными программами](https://u.netology.ru/backend/uploads/lms/content_assets/file/5630/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D1%8F_%D0%BF%D0%BE_%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B5_%D1%81_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%D0%BC%D0%B8_Modbus_Slave__MasterOPC___Matrikon_OPC__HDA__Explorer__UaExpert.pptx).

------

### Инструкция к выполнению домашнего задания

1. Скачайте [Шаблон для домашнего задания](https://u.netology.ru/backend/uploads/lms/content_assets/file/5631/%D0%A8%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD_%D0%B4%D0%BB%D1%8F_%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%B3%D0%BE_%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D1%8F__%D0%9F%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB_%D0%BE%D0%B1%D0%BC%D0%B5%D0%BD%D0%B0_%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8_OPC__-_%D0%A4%D0%B0%D0%BC%D0%B8%D0%BB%D0%B8%D1%8F_%D0%98%D0%BC%D1%8F__%D0%A1%D0%94%D0%95%D0%9B%D0%90%D0%99%D0%A2%D0%95_%D0%9A%D0%9E%D0%9F%D0%98%D0%AE_.docx) на своё устройство.
2. Откройте скачанный файл на личном диске в Google.
3. В названии файла введите корректное название лекции и ваши фамилию и имя.
4. Зайдите в «Настройки доступа» и выберите доступ «Просматривать могут все в интернете, у кого есть ссылка». Инструкция «Как предоставить доступ к файлам и папкам на Google Диске» [по ссылке](https://support.google.com/docs/answer/2494822?hl=ru&co=GENIE.Platform%3DDesktop).
5. Скопируйте текст задания в свой документ.
6. Выполните задание, запишите ответы и приложите необходимые скриншоты в свой Google-документ.
7. Для проверки домашнего задания отправьте ссылку на ваш Google-документ в личном кабинете.
8. Любые вопросы по решению задач можно задать в [чате поддержки](https://netology.ru/profile?modal=support&type=new-ticket) или в разделе «Вопросы по заданию» при выполнении практических заданий.
9. Подробнее о работе с Google-документами и загрузке решения на проверку можно найти в [«Руководстве по работе с материалами для обучения»](https://l.netology.ru/instruktsiya-po-materialami-dlya-obucheniya)


------

### Инструменты и дополнительные материалы, которые пригодятся для выполнения задания:

1. [Google Drive](https://www.google.com/intl/ru/drive/).
2. Программы Modbus Slave, MasterOPC Universal Modbus Server, Matrikon OPC Explorer, UaExpert:
- [Modbus Slave Install 64bit](https://www.modbustools.com/download/ModbusSlaveSetup64Bit.exe "ModbusSlave Install 64bit"),
- [Modbus Slave Install 32bit](https://www.modbustools.com/download/ModbusSlaveSetup32Bit.exe "ModbusSlave Install 32bit"),
- [MasterOPC Universal Modbus Server](https://insat.ru/products/Universal_MasterOPC/MODBUS_OPC_SERVER_32TAGS.ZIP "MasterOPC Universal Modbus Server (Zip)"),
- [Matrikon OPC Explorer](https://www.matrikonopc.com/portal/downloads/product_software/MatrikonOPCExplorer.exe) (требуется предварительная регистрация),
- [Matrikon OPC HDA Explorer](https://www.matrikonopc.com/portal/downloads/product_software/MatrikonOPCHDAExplorer.exe) (требуется предварительная регистрация),
- [UaExpert](https://www.unified-automation.com/fileadmin/files/client/uaexpert-bin-win32-x86-vs2008sp1-v1.6.3-448.zip) (требуется предварительная регистрация).
3. [Инструкция по работе с программами Modbus Slave, MasterOPC Universal Modbus Server, Matrikon OPC Explorer, UaExpert](https://u.netology.ru/backend/uploads/lms/content_assets/file/5630/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D1%8F_%D0%BF%D0%BE_%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B5_%D1%81_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%D0%BC%D0%B8_Modbus_Slave__MasterOPC___Matrikon_OPC__HDA__Explorer__UaExpert.pptx).
4. [Шаблон для домашнего задания](https://u.netology.ru/backend/uploads/lms/content_assets/file/5631/%D0%A8%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD_%D0%B4%D0%BB%D1%8F_%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%B3%D0%BE_%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D1%8F__%D0%9F%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB_%D0%BE%D0%B1%D0%BC%D0%B5%D0%BD%D0%B0_%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8_OPC__-_%D0%A4%D0%B0%D0%BC%D0%B8%D0%BB%D0%B8%D1%8F_%D0%98%D0%BC%D1%8F__%D0%A1%D0%94%D0%95%D0%9B%D0%90%D0%99%D0%A2%D0%95_%D0%9A%D0%9E%D0%9F%D0%98%D0%AE_.docx).

------

### Задание 1

Производитель комплексного прибора, измеряющего параметры окружающей среды — температуру воздуха, атмосферное давление, относительную влажность, скорость ветра, — предоставил данные для связи с этим устройством по Modbus TCP:

- температура — 30005;
- давление — 30006;
- влажность — 30007;
- скорость ветра — 30008.

Инженеру АСУ ТП в программе MasterOPC Universal Modbus Server необходимо создать новый рабочий проект с конфигурацией, позволяющей установить связь с двумя экземплярами виртуальной модели этого прибора с указанными ниже параметрами. Получите данные о температуре, давлении и проч. с каждого из приборов:

Экземпляр 1:

- Протокол — Modbus TCP;
- Slave ID = 7;
- Port = 504.

Экземпляр 2:

- Протокол — Modbus TCP;
- Slave ID = 8;
- Port = 505.

Для проверки работоспособности этой конфигурации необходимо запустить два экземпляра программы Modbus Slave, в каждом из которых необходимо создать виртуальное устройство с указанными выше параметрами. Присвойте им следующие значения (единицы измерения не вносятся в конфигурацию, они даны для пояснения):

Экземпляр 1:

- температура = 18 (градусов);
- давление = 99 (кПа);
- влажность = 60 (%);
- скорость ветра = 2 (м/с).

Экземпляр 2: 

- температура = 22 (градуса);
- давление = 101 (кПа);
- влажность = 80 (%);
- скорость ветра = 4 (м/с).

Убедитесь в работоспособности схемы «Сервер OPC — два экземпляра виртуальных приборов», произведя их соединение (для сервера — выбором команды «Старт», для каждого из экземпляров Modbus Slave — переводом в статус Connected) и проверив идентичность отправляемых и получаемых данных.

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

1. Задание 1 считается выполненным, если при загрузке конфигураций в программы MasterOPC Universal Modbus Server, Modbus Slave (оба экземпляра) и включении режимов «Старт» и Connect соответственно происходит корректное чтение данных сервером OPC из устройств Modbus Slave, а на основных экранах этих программ выдаются указанные в условии значения параметров.
2. Задание 2 считается выполненным, если после настройки программ-клиентов OPC на них отображаются те же данные, что и на сервере OPC.
