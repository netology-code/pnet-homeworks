# Домашнее задание к занятию «Полевые шины и протоколы»

### Цель задания

Опыт работы с ПО Modbustools полезен для осваивания скиллсета инженера по автоматизации по следующим задачам:
- конфигурирование Modbus Poll для подключения и проверки правильности работы ведомых устройств Modbus;
- создание симулятора ведомого устройства Modbus с использованием Modbus Slave, что может пригодиться в процессе разработки при отсутствии требуемого прибора;
- построения сетей Profibus и Profinet.

В результате выполнения задания вы сможете:

1. Настроить и оценить подключение по протоколу Modbus к ведомым устройствам.
2. Получить опыт проверки проекта подключения полевых приборов Profibus и Profinet на предмет соответствия протоколам.

------

### Чеклист готовности к домашнему заданию

1. Скачаны и установлены программы Modbus Poll и Modbus Slave.

Ссылки на скачивание:

- [Modbus Poll Install 64bit](https://www.modbustools.com/download/ModbusPollSetup64Bit.exe "ModbusPoll Install 64bit"),
- [Modbus Poll Install 32bit](https://www.modbustools.com/download/ModbusPollSetup32Bit.exe "ModbusPoll Install 32bit"),
- [Modbus Slave Install 64bit](https://www.modbustools.com/download/ModbusSlaveSetup64Bit.exe "ModbusSlave Install 64bit"),
- [Modbus Slave Install 32bit](https://www.modbustools.com/download/ModbusSlaveSetup32Bit.exe "ModbusSlave Install 32bit").
 
 **ВНИМАНИЕ!** Устанавливаются демоверсии программ. Их функционал будет ограничен спустя 30 дней после установки.
 Производите установку программ **только** непосредственно перед началом выполнения задания.

2. Скачан графический файл Profibus_Profinet.png, имеется программа для просмотра этого файла с возможностью увеличения отдельных фрагментов изображения.

Ссылка на скачивание: [Profibus_Profinet.png](https://u.netology.ru/backend/uploads/lms/content_assets/file/828/Profibus_Profinet.png).

------

### Инструкция к выполнению домашнего задания

1. Скачайте [Шаблон для домашнего задания](https://u.netology.ru/backend/uploads/lms/content_assets/file/829/%D0%A8%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD_%D0%B4%D0%BB%D1%8F_%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%B3%D0%BE_%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D1%8F__%D0%9F%D0%BE%D0%BB%D0%B5%D0%B2%D1%8B%D0%B5_%D1%88%D0%B8%D0%BD%D1%8B_%D0%B8_%D0%BF%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB%D1%8B__-_%D0%A4%D0%B0%D0%BC%D0%B8%D0%BB%D0%B8%D1%8F_%D0%98%D0%BC%D1%8F__%D0%A1%D0%94%D0%95%D0%9B%D0%90%D0%99%D0%A2%D0%95_%D0%9A%D0%9E%D0%9F%D0%98%D0%AE_.docx) на своё устройство.
2. Откройте скачанный файл на личном диске в Google.
3. В названии файла введите корректное название лекции и ваши фамилию и имя.
4. Зайдите в «Настройки доступа» и выберите доступ «Просматривать могут все в интернете, у кого есть ссылка». Инструкция «Как предоставить доступ к файлам и папкам на Google Диске» [по ссылке](https://support.google.com/docs/answer/2494822?hl=ru&co=GENIE.Platform%3DDesktop).
5. Скопируйте текст задания в свой документ.
6. Выполните задание, запишите ответы и приложите необходимые скриншоты в свой Google-документ.
7. Для проверки домашнего задания отправьте ссылку на ваш Google-документ в личном кабинете.
8. Любые вопросы по решению задач можно задать в чате учебной группы, в чате поддержки или в разделе «Вопросы по заданию» в личном кабинете.
9. Подробнее о работе с Google-документами и загрузке решения на проверку можно найти в [«Руководстве по работе с материалами для обучения»](https://l.netology.ru/instruktsiya-po-materialami-dlya-obucheniya)


------

### Инструменты и дополнительные материалы, которые пригодятся для выполнения задания:

1. [Google Drive](https://www.google.com/intl/ru/drive/).
2. Программы Modbus Poll, Modbus Slave:
- [Modbus Poll Install 64bit](https://www.modbustools.com/download/ModbusPollSetup64Bit.exe "ModbusPoll Install 64bit"),
- [Modbus Poll Install 32bit](https://www.modbustools.com/download/ModbusPollSetup32Bit.exe "ModbusPoll Install 32bit"),
- [Modbus Slave Install 64bit](https://www.modbustools.com/download/ModbusSlaveSetup64Bit.exe "ModbusSlave Install 64bit"),
- [Modbus Slave Install 32bit](https://www.modbustools.com/download/ModbusSlaveSetup32Bit.exe "ModbusSlave Install 32bit").
3. [Инструкция по работе с программами Modbus Poll, Modbus Slave](https://u.netology.ru/backend/uploads/lms/content_assets/file/830/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D1%8F_%D0%BF%D0%BE_%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B5_%D1%81_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%D0%BC%D0%B8_ModbusPoll__ModbusSlave.pptx).
4. [Графический файл Profibus_Profinet.png](https://u.netology.ru/backend/uploads/lms/content_assets/file/828/Profibus_Profinet.png).
5. [Шаблон для домашнего задания](https://u.netology.ru/backend/uploads/lms/content_assets/file/829/%D0%A8%D0%B0%D0%B1%D0%BB%D0%BE%D0%BD_%D0%B4%D0%BB%D1%8F_%D0%B4%D0%BE%D0%BC%D0%B0%D1%88%D0%BD%D0%B5%D0%B3%D0%BE_%D0%B7%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D1%8F__%D0%9F%D0%BE%D0%BB%D0%B5%D0%B2%D1%8B%D0%B5_%D1%88%D0%B8%D0%BD%D1%8B_%D0%B8_%D0%BF%D1%80%D0%BE%D1%82%D0%BE%D0%BA%D0%BE%D0%BB%D1%8B__-_%D0%A4%D0%B0%D0%BC%D0%B8%D0%BB%D0%B8%D1%8F_%D0%98%D0%BC%D1%8F__%D0%A1%D0%94%D0%95%D0%9B%D0%90%D0%99%D0%A2%D0%95_%D0%9A%D0%9E%D0%9F%D0%98%D0%AE_.docx).

<details>
  <summary> Что делать, если возникают вопросы или сложности по установке и работе с программным обеспечением? (доступно по клику)</summary>
  
  
1. Напишите в чат группы или обратиться к координатору в системе обращений студентов на сайте по [ссылке](netology.ru/profile?modal=support&type=new-ticket)

2. Можете написать о своей проблеме в разделе «Вопросы и ответы» к домашнему заданию
  
  ![image](https://github.com/netology-code/pwin-homeworks/blob/homeworks-pae-7/5.1/Q%26A.png)
    ---
  
</details>

------

### Задание 1

Производитель комплексного прибора, измеряющего параметры окружающей среды — температуру воздуха, атмосферное давление, относительную влажность, скорость ветра, — предоставил данные для связи с этим устройством по Modbus RTU:

- температура — 30005;
- давление — 30006;
- влажность — 30007;
- скорость ветра — 30008.

Инженеру АСУ ТП в программе Modbus Poll необходимо создать конфигурацию, позволяющую установить связь с виртуальной моделью этого прибора.

Для проверки работоспособности этой конфигурации в программе Modbus Slave необходимо создать виртуальное устройство с указанными выше параметрами, присвоив им следующие значения (единицы измерения не вносятся в конфигурацию, они даны для пояснения):

- температура = 20 (градусов);
- давление = 100 (кПа);
- влажность = 70 (%);
- скорость ветра = 1 (м/с).

Ответ приведите в виде файлов конфигурации, созданных в программах Modbus Poll и Modbus Slave. Файлы конфигурации необходимо сохранить в Google Drive, сделав их доступными для загрузки. В шаблоне для домашнего задания приведите ссылки на эти файлы. В названиях файлов конфигурации укажите фамилию, имя студента и лекцию, к которой относится ДЗ, следующим образом: StudentName_LectureN_xxx.* (например, IvanovPetr_Lecture2_4_001.mbp).

Для большего удобства вы можете воспользоваться [инструкцией по работе с программами Modbus Poll, Modbus Slave](https://u.netology.ru/backend/uploads/lms/content_assets/file/830/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%86%D0%B8%D1%8F_%D0%BF%D0%BE_%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B5_%D1%81_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%D0%BC%D0%B8_ModbusPoll__ModbusSlave.pptx).

------

### Задание 2

Инженер АСУ ТП получил от разработчика эскиз схемы ([Profibus_Profinet.png](https://u.netology.ru/backend/uploads/lms/content_assets/file/828/Profibus_Profinet.png)) автоматизированной системы управления с использованием устройств, подключаемых по протоколам Profibus и Profinet.
Не владея в полной мере информацией, разработчик допустил несколько ошибок.

Ответ приведите в виде списка найденных ошибок для корректировки схемы.

------

### Правила приёма работы:

1. Отправлена ссылка на документ (Google Doc) с выполненным заданием в личном кабинете.
2. Документ размещён на личном Google Диске.
3. К документу настроены права доступа «Просматривать могут все в Интернете, у кого есть ссылка».

------

### Критерии оценки

1. Задание 1 считается выполненным, если при загрузке конфигураций в программы Modbus Poll, Modbus Slave и включении режима Connect происходит корректный обмен запросами от Master и ответами от Slave, а на основных экранах выдаются указанные в условии значения параметров.
2. Задание 2 считается выполненным, если найдено 10 и более ошибок в схеме.
