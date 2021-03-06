﻿---
title: Сведения о настройке расписаний
TOCTitle: Сведения о настройке расписаний
ms:assetid: 39ca6fff-2c15-4347-9f1f-6c8687a39a49
ms:mtpsurl: https://technet.microsoft.com/ru-ru/library/JJ204823(v=OCS.15)
ms:contentKeyID: 49309478
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Сведения о настройке расписаний

 

_**Дата изменения раздела:** 2012-10-04_

После проверки отсутствия другого запланированного собрания на запрашиваемое время, персонал поддержки, который обрабатывает запрос, планирует собрание в пуле больших собраний. Рекомендуется выполнять эту задачу с помощью надстройки конференц-связи для собраний по сети для Lync, которая устанавливается с клиентом Lync Server 2013, используя учетные данные пользователя с включенной поддержкой Lync Server в выделенном пуле больших собраний.

Чтобы обеспечить наилучшее взаимодействие с пользователями, важно запланировать большое собрание с правильными уровнями доступа и параметрами, соответствующими потребностям организатора собрания. Далее приводятся рекомендации по настройке параметров Lync.

  - Используйте новое место собрания для каждого большого собрания вместо повторного использования выделенного места собрания.

  - Указывайте уровень доступа к собранию следующим образом.
    
      - Если хотя бы один приглашенный является внешним по отношению к организации, установите тип доступа к собранию **Все (без исключений)**. Это позволит исключить необходимость управления потенциально большим "залом ожидания" во время проведения собрания.
    
      - Если собрание только внутреннее, установите тип доступа к собранию **Все во организации**.
        
        > [!NOTE]  
        > Избегайте устанавливать тип доступа к собранию <strong>Приглашенные пользователи из организации</strong>, поскольку при использовании этого параметра придется добавлять адреса электронной почты всех пользователей в список приглашенных. Кроме того, при использовании этого параметра не работает приглашение групп рассылки.<br />        Избегайте устанавливать тип доступа <strong>Только организатор</strong>, поскольку при использовании этого параметра во время проведения собрания в &quot;зал ожидания&quot; должны помещаться все участники собрания, включая выступающих. Лицо, отвечающее за проведение собрания, должно затем постоянно наблюдать за реестром &quot;зала ожидания&quot; и допускать новых пользователей из &quot;зала ожидания&quot;.

  - Разрешите пользователям автоматически присоединяться к собранию путем вызова с телефонного аппарата, включив параметр **Вызывающие абоненты присоединяются напрямую**.

  - Явным образом приглашайте следующих пользователей:
    
      - организатор собрания и делегат (инициатор запроса);
    
      - список выступающих, предоставленный инициатором запроса на собрание.
    
    > [!NOTE]  
    > Если установлен тип доступа к собранию <strong>Выбранные пользователи</strong>, то требуется явно добавлять каждого участника большого собрания как приглашенного на собрание.

  - Явно управляйте докладчиками вместо определения параметра докладчика в качестве одного из значений автоматического продвижения. Убедитесь, что следующие пользователи добавлены в качестве докладчиков:
    
      - организатор собрания и делегат (инициатор запроса);
    
      - список выступающих, предоставленный инициаторами запроса на большое собрание.
    
    > [!NOTE]  
    > Явное управление выступающими позволяет контролировать количество докладчиков, чтобы можно было сузить количество докладчиков до количества, достаточного для проведения эффективного большого собрания. Если большинство участников имеет роль участника, это помогает уменьшить вероятность случайного получения контроля над выступлением, удаления презентации PowerPoint, включения или отключения микрофона выступающих и других нарушений в собрании.

  - Проверьте параметр **Отключить всех участников**, чтобы было слышно только докладчиков.

  - Проверьте параметр **Заблокировать видео участников**, чтобы было видно только докладчиков.

На следующем рисунке показаны рекомендуемые параметры для надстройки конференц-связи для собраний по сети для Lync.

![Параметры собрания для конференции](images/JJ204823.54e4e70d-06b0-45cd-8d94-bab649cd5dc0(OCS.15).jpg "Параметры собрания для конференции")

