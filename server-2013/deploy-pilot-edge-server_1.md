﻿---
title: Развертывание пилотного пограничного сервера
TOCTitle: Развертывание пилотного пограничного сервера
ms:assetid: 11a59c48-0a53-4de1-83ed-875f850febd5
ms:mtpsurl: https://technet.microsoft.com/ru-ru/library/JJ204682(v=OCS.15)
ms:contentKeyID: 49308990
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Развертывание пилотного пограничного сервера

 

_**Дата изменения раздела:** 2012-10-19_

В данной статье рассматриваются параметры конфигурации, о которых необходимо быть осведомленным до развертывания Lync Server 2013  сервер. В этом разделе освещаются только ключевые моменты, которые следует проанализировать как часть развертывания пилотного пограничного пула. Подробное описание действий см. в разделе [Развертывание доступа внешних пользователей в Lync Server 2013](lync-server-2013-deploying-external-user-access.md) в документации по развертыванию, где излагается процедура развертывания, а также приводятся сведения о конфигурации для внешнего пользовательского доступа.

При выполнении инструкций мастера **задания нового пограничного пула** изучите основные параметры конфигурации, представленные в следующих действиях. Обратите внимания, что показаны не все страницы мастера **задания нового пограничного пула** .

**Задание пограничного пула**

1.  Откройте топологию пилотного пула с помощью построителя топологии.

2.  Перейдите к узлу Lync Server 2013. Щелкните правой кнопкой элемент **Edge pools** (Пограничные пулы), а затем выберите **New Edge pool** (Новый пограничный пул).
    
    ![Диалоговое окно назначения нового пограничного пула](images/JJ205306.a90d388c-49ff-4620-a19d-42e2f1bb559c(OCS.15).jpg "Диалоговое окно назначения нового пограничного пула")

3.  Пограничный пул может представлять собой **пул с несколькими компьютерами** или **пул с одним компьютером** .
    
    ![Диалоговое окно назначения полного доменного имени пограничному пулу](images/JJ205306.4904fe8f-537c-4e66-a399-1bd8a316dc10(OCS.15).jpg "Диалоговое окно назначения полного доменного имени пограничному пулу")

4.  На странице **Выбор компонентов** не включайте ни федерацию, ни федерацию XMPP. В настоящее время маршруты к федерации и федерации XMPP прокладываются через унаследованный серверOffice Communications Server 2007 R2. Эти компоненты настраиваются на более позднем этапе миграции.
    
    ![Диалоговое окно выбора компонентов](images/JJ205306.cb0b45a4-2856-45ba-bd97-e49fafbb077e(OCS.15).jpg "Диалоговое окно выбора компонентов")

5.  Далее продолжайте выполнять действия, описываемые на следующих страницах мастера: **Выбор IP-параметров** , **Внешние полные доменные имена** , **Определение внутреннего IP-адреса** и **Определение внешнего IP-адреса** .

6.  На странице **Определение следующего прыжка** выберите Директор для следующего прыжка Lync Server 2013 пул.
    
    ![Диалоговое окно определения нового пограничного пула, список пулов узлов следующего перехода](images/JJ204682.61d963d5-e0bd-4b1f-b437-e37c267347ba(OCS.15).jpg "Диалоговое окно определения нового пограничного пула, список пулов узлов следующего перехода")

7.  На странице **Связывание клиентских пулов** не связывайте в этот раз пул с данным пулом пул. В настоящее время внешний мультимедийный трафик направляется через унаследованный сервер Office Communications Server 2007 R2  сервер. Этот параметр настраивается на более позднем этапе миграции.
    
    ![Диалоговое окно определения нового пограничного пула](images/JJ204682.bb538039-bd2a-40ed-a120-8b80bd2cefc2(OCS.15).jpg "Диалоговое окно определения нового пограничного пула")

8.  Щелкните **Finish** (Готово), а затем **Publish** (Опубликовать), чтобы опубликовать топологию.

9.  Следуйте инструкциям, приведенным в разделе [Установка пограничных серверов для Lync Server 2013](lync-server-2013-install-edge-servers.md) документации по развертыванию, чтобы установить файлы на новом сервер, настроить сертификаты и запустить службы.

Крайне важно следовать инструкциям, приведенным в разделах [Развертывание доступа внешних пользователей в Lync Server 2013](lync-server-2013-deploying-external-user-access.md) документации по развертыванию. В этом разделе указаны просто некоторые рекомендации по заданию параметров конфигурации в ходе установки этих серверных ролей.

Теперь должно быть развертывание унаследованного пограничного сервера Office Communications Server 2007 R2, на присутствие которого указывает BackCompatSite, параллельно с развертыванием пограничного сервера Lync Server 2013. Федерация настроена для использования директора Office Communications Server 2007 R2. До перехода на следующий этап проверьте, чтобы оба развертывания функционировали правильно, службы были запущены и чтобы можно было администрировать каждое развертывание.

![Построитель топологий, отображающий пограничный сервер OCS](images/JJ204682.171363a3-eaf0-4c94-bd41-02b1ab6fa7dc(OCS.15).jpg "Построитель топологий, отображающий пограничный сервер OCS")

