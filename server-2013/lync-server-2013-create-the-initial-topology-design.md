﻿---
title: 'Lync Server 2013: создание начального проекта топологии'
TOCTitle: Создание начального проекта
ms:assetid: f3131153-de14-41be-b1e6-7d4bb0191af1
ms:mtpsurl: https://technet.microsoft.com/ru-ru/library/Gg615047(v=OCS.15)
ms:contentKeyID: 52058504
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Создание начального проекта топологии для Lync Server 2013

 

_**Дата изменения раздела:** 2013-02-21_

После завершения установки планирования Lync Server 2013 вы готовы к запуску планирования и началу разработки предложенной инфраструктуры Lync Server 2013.

> [!NOTE]  
> планирования – это средство на основе мастера с подробными инструкциями, предоставляющими сведения для процесса принятия решений во время разработки сайтов и топологий. Целью данного раздела является не утомительное руководство, а просто помощь в начале работы с планирования во время разработки.

## Начало работы со средством планирования и создание начального дизайна

1.  Запустите средство планирования Lync Server 2013: нажмите кнопку **Пуск**, последовательно выберите пункты **Все программы** и **Microsoft Lync Server 2013** и щелкните элемент **Средство планирования**.

2.  После запуска планирования появится страница **Welcome to the Planning Tool for Microsoft Lync Server 2013 (Вас приветствует средство планирования для Microsoft Lync Server 2013)** . Чтобы начать разработку, выберите один из следующих параметров.
    
      - **Вариант 1. Начало работы**   Если щелкнуть команду **Get Started (начало работы)** , будет предъявлен определенный набор вопросов с соответствующими разделами для задания критериев. После завершения начального интервью **Get Started (начало работы)** откроется раздел **Design Sites (разработка сайтов)** , чтобы задать архитектуру сайта. Для выполнения этого варианта перейдите к шагу 3.
    
      - **Вариант 2. Разработка сайтов**   Если щелкнуть команду **Design Sites (разработка сайтов)** на странице приветствия, вопросы интервью, отображаемые в разделе **Get Started (начало работы)** , будут пропущены. В этом случае сведения, собираемые с помощью вопросов интервью в разделе **Get Started (начало работы)** , будут иметь значения по умолчанию. Щелкнув команду **Design Sites (разработка сайтов)** , опытный разработчик может исключить начальное интервью и изменить значения по умолчанию, если требуется, на начальной странице **Central Sites (центральные сайты)** . Для выполнения этого варианта пропустите шаги 3?5 и начните с шага 6.
    
      - **Вариант 3. Отображение сохраненной топологии**   Если вы уже создали и сохранили топологию при помощи планирования, можно пропустить большую часть шагов и начать с открытия и отображения топологии. Также в топологию можно внести изменения и обновления, пересохранить ее и затем экспортировать в Microsoft Excel или Microsoft Visio. Чтобы выполнить данный вариант, пропустите шаги 3-12 и начните с шага 13.

3.  Щелкните **Get Started (начало работы)** , чтобы начать разработку топологии Lync Server 2013.

4.  Ответьте на вопросы каждого раздела, выбирая соответствующий критерий проекта и затем нажмите кнопку **Далее** , чтобы перейти на следующую страницу мастера. Нажмите кнопку **Назад** , если требуется внести изменения на предыдущих страницах.
    

    > [!TIP]
    > На каждой странице есть описание критериев выбора и рекомендации, основанные на предпочтительных методах и результатах планирования емкости. Если требуются дополнительные сведения, нажмите кнопку <STRONG>Learn more (дополнительные сведения)</STRONG> , чтобы прочитать подробную информацию из документации по планированию Lync Server 2013 на веб-сайте Microsoft TechNet. Чтобы получить доступ к веб-сайту Microsoft TechNet, требуется подключение к Интернету.



5.  Выберите подходящие параметры проекта. После задания начальных критериев будет выдано подтверждение, что обзор свойств завершен.

6.  Нажмите кнопку **Design Sites (разработка сайтов)** , чтобы определить сайт.
    
    > [!NOTE]  
    > Каждая топология Lync Server 2013 будет иметь минимум один сайт. Проект может содержать один сайт, сайт с несколькими сайтами филиалов, несколько центральных сайтов или несколько центральных сайтов с сайтами филиалов, связанными с каждым сайт.

7.  В поле **Site Name (имя сайта)** введите имя, которое будет идентифицировать этот сайт.

8.  В поле **Site Homed Users (пользователи, размещенные на сайте)** введите предполагаемое число локальных пользователей, которые будут одновременно работать с сайтом и которые будут размещены на этом сайт.

9.  В поле **Cloud Homed Users (пользователи, размещенные в облаке)** введите предполагаемое число облачных пользователей, которые будут одновременно работать с сайтом и которые будут размещены на этом сайт.

10. Измените выбранные значения для параметров Online Collaboration (совместная работа в сети), Users (пользователи), Voice (голосовая связь), Additional Deployment Options (дополнительные параметры развертывания) или Server Applications (серверные приложения), если требуется.
    
    > [!IMPORTANT]  
    > На данном этапе разработки можно только выбирать или отменять параметры развертывания. Но большее число параметров можно настроить на последующих этапах работы планирования. Имеются также параметры, которые недоступны и не могут быть отменены. Кроме того, иногда необходимо отменить один параметр, чтобы отменить другой. Например, если отменить параметр <strong>Enterprise Voice (корпоративная голосовая связь)</strong> в разделе Voice (голосовая связь), то параметры <strong>Response Group (группа ответа)</strong> , <strong>Announcement (объявления)</strong> и <strong>Call Park (парковка вызовов)</strong> в разделе Server Applications (серверные приложения) также будут отменены (все эти параметры являются функциями корпоративной голосовой связи).

11. После задания имени сайта и числа пользователей нажмите кнопку **Далее** .

12. На следующих страницах запрашивается информация о доменах SIP, параметрах конференций, параметрах голосовой связи, инфраструктуре, обмена сообщениями Exchange, доступе внешних пользователей, параметрах сохраняемый сеанс беседы, параметрах клиентов, параметрах совмещения функций и сайтов филиалов. Ответьте на эти вопросы соответствующим образом.

13. Последний вопрос о том, требуется ли создать другой сайт. Если выбрать **Да** , то планирования возвращается на страницу центральных сайтов. Если выбрать **Нет** , нажмите кнопку **Далее** и затем кнопку **Draw (нарисовать)** , чтобы отобразить высокоуровневое представление глобальной топологии.

14. Чтобы просмотреть существующую топологию, нажмите кнопку **Display (отобразить)** .

15. Щелкните XML-файл, содержащий ранее сохраненную топологию, а затем нажмите кнопку **Open (открыть)** .

16. планирования отобразит страницу глобальной топологии. Теперь можно начать редактирование, обновление или изменение топологии с помощью инструментов, доступных в планирования.

## См. также

#### Концепции

[Изменение структуры в Lync Server 2013](lync-server-2013-editing-the-design.md)

