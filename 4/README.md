# Домашнее задание к занятию «Полевые шины и протоколы»

### Цель задания

Опыт работы с ПО Modbustools полезен для осваивания скиллсета инженера по автоматизации по следующим задачам:
- конфигурирование Modbus Poll для подключения и проверки правильности работы ведомых устройств Modbus
- создание симулятора ведомого устройства Modbus с использованием Modbus Slave, что может пригодиться в процессе разработки при отсутствии требуемого прибора
- построения сетей Profibus и Profinet.

В результате выполнения задания вы сможете:

1. Настроить и оценить подключение по протоколу Modbus к ведомым устройствам.
2. Получить опыт проверки проекта подключения полевых приборов Profibus / Profinet на предмет соответствия протоколам.

------

### Чеклист готовности к домашнему заданию

1. Скачаны и установлены программы ModbusPoll, ModbusSlave.

Ссылки на скачивание:

- [Modbus Poll Install 64bit](https://www.modbustools.com/download/ModbusPollSetup64Bit.exe "ModbusPoll Install 64bit")
- [Modbus Poll Install 32bit](https://www.modbustools.com/download/ModbusPollSetup32Bit.exe "ModbusPoll Install 32bit")
- [Modbus Slave Install 64bit](https://www.modbustools.com/download/ModbusSlaveSetup64Bit.exe "ModbusSlave Install 64bit")
- [Modbus Slave Install 32bit](https://www.modbustools.com/download/ModbusSlaveSetup32Bit.exe "ModbusSlave Install 32bit")
 
 **ВНИМАНИЕ!** Устанавливаются демо-версии программ. Их функционал будет ограничен спустя 30 дней после установки.
 Производите установку программ **только** непосредственно перед началом выполнения задания.

2. Скачан графический файл Profibus_Profinet.png, имеется программа для просмотра данного файла с возможностью увеличения отдельных фрагментов изображения.

Ссылка на скачивание: [Profibus_Profinet.png](https://drive.google.com/file/d/1Gtwuw8rEgn4vgHE1r3Kd3ztujE-Nw1PD/view?usp=sharing)

------

### Инструкция к выполнению домашнего задания

1. Сделайте копию [Шаблона для домашнего задания](https://docs.google.com/document/d/1O_qG2tp0vKnsrQRLqTzLgUbjcpf-wRs0N4r21e-tUKA/edit?usp=sharing) себе на Google Диск.
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
2. Программы ModbusPoll, ModbusSlave.
- [Modbus Poll Install 64bit](https://www.modbustools.com/download/ModbusPollSetup64Bit.exe "ModbusPoll Install 64bit")
- [Modbus Poll Install 32bit](https://www.modbustools.com/download/ModbusPollSetup32Bit.exe "ModbusPoll Install 32bit")
- [Modbus Slave Install 64bit](https://www.modbustools.com/download/ModbusSlaveSetup64Bit.exe "ModbusSlave Install 64bit")
- [Modbus Slave Install 32bit](https://www.modbustools.com/download/ModbusSlaveSetup32Bit.exe "ModbusSlave Install 32bit")
3. [Инструкция по работе с программами Modbus Poll, Modbus Slave](https://docs.google.com/presentation/d/10FJtSidtjtJFQqDTVSlwccb-mRfMvL-lXBGHUfZ5pWY/edit#slide=id.g1144c4bf944_0_529)
4. [Графический файл Profibus_Profinet.png](https://drive.google.com/file/d/1Gtwuw8rEgn4vgHE1r3Kd3ztujE-Nw1PD/view?usp=sharing)
5. [Шаблон для домашнего задания](https://docs.google.com/document/d/1O_qG2tp0vKnsrQRLqTzLgUbjcpf-wRs0N4r21e-tUKA/edit?usp=sharing)

------

### Задание 1

Производитель комплексного прибора, измеряющего параметры окружающей среды (температуру воздуха, атмосферное давление, относительную влажность, скорость ветра), предоставил данные для связи с этим устройством по Modbus RTU:

- Температура - 30005
- Давление - 30006
- Влажность - 30008
- Скорость ветра - 30009

Инженеру АСУ ТП в программе Modbus Poll необходимо создать конфигурацию, позволяющую установить связь с виртуальной моделью этого прибора.

Для проверки работоспособности этой конфигурации в программе Modbus Slave необходимо создать виртуальное устройство с указанными выше параметрами, присвоив им следующие значения (единицы измерения не вносятся в конфигурацию, они даны для пояснения):

- Температура = 20 (градусов)
- Давление = 100 (кПа)
- Влажность = 70 (%)
- Скорость ветра = 1 (м/с)

Ответ приведите в виде файлов конфигурации, созданных в программах Modbus Poll и Modbus Slave. Файлы конфигурации необходимо сохранить в Google Drive, сделав их доступными для загрузки. В шаблоне для домашнего задания приведите ссылки на эти файлы. В названиях файлов конфигурации укажите фамилию, имя студента и лекцию, к которой относится ДЗ, следующим образом: StudentName_LectureN_xxx.* (например, IvanovPetr_Lecture2_4_001.mbp).

Для большего удобства вы можете воспользоваться [инструкцией по работе с программами Modbus Poll, Modbus Slave](https://docs.google.com/presentation/d/10FJtSidtjtJFQqDTVSlwccb-mRfMvL-lXBGHUfZ5pWY/edit#slide=id.g1144c4bf944_0_529)

------

### Задание 2

Инженер АСУ ТП получил от разработчика эскиз схемы ([Profibus_Profinet.png](https://drive.google.com/file/d/1Gtwuw8rEgn4vgHE1r3Kd3ztujE-Nw1PD/view?usp=sharing)) автоматизированной системы управления с использованием устройств, подключаемых по протоколам Profibus и Profinet.
Не владея в полной мере информацией, разработчик допустил несколько ошибок.

Ответ приведите в виде списка найденных ошибок для корректировки схемы.

------

### Правила приёма работы

1. Отправлена ссылка на документ (Google Doc) с выполненным заданием в личном кабинете.
2. Документ размещён на личном Google Disk.
3. К документу настроены права доступа «Просматривать могут все в Интернете, у кого есть ссылка».

------

### Критерии оценки

1. Задание 1 считается выполненным, если при загрузке конфигураций в программы Modbus Poll, Modbus Slave и включении режима «Connect» происходит корректный обмен запросами от Master и ответами от Slave, а на основных экранах выдаются указанные в условии значения параметров.
2. Задание 2 считается выполненным, если найдено 10 и более ошибок в схеме.
