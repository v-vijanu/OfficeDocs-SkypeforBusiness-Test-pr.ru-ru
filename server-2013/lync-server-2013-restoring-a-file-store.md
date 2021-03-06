﻿---
title: Восстановление хранилища файлов
TOCTitle: Восстановление хранилища файлов
ms:assetid: 89916fc6-31d3-4c7f-9eaf-c02584761ef4
ms:mtpsurl: https://technet.microsoft.com/ru-ru/library/Hh202180(v=OCS.15)
ms:contentKeyID: 52058269
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Восстановление хранилища файлов

 

_**Дата изменения раздела:** 2013-02-18_

Хранилища файлов для Standard Edition обычно располагаются на сервере Сервер Standard Edition. Хранилища файлов для Enterprise Edition обычно располагаются на файловом сервере или в кластере. В следующей процедуре описывается восстановление хранилища файлов.

## Восстановление хранилища файлов

1.  Если происходит сбой хранилища файлов, скопируйте соответствующее хранилище файлов из папки $Backup\\ в расположение хранилища файлов на файловом сервер или сервере Сервер Standard Edition, а затем разрешите общий доступ к этой папке.
    
    > [!IMPORTANT]  
    > Путь и имя файла для восстановленного хранилища файлов должны быть точно такими же, как и у хранилища файлов, для которого выполнялось резервное копирование. Это позволит компонентам, использующим данные файлы, получить к ним доступ.

2.  при необходимости задайте для хранилища файлов списки управления доступом (ACL). Введите в командной строке следующее:
    
        Enable-CsTopology
    
    > [!NOTE]  
    > Это действие требуется выполнять только в том случае, если вы еще не запускали построитель топологий во время процесса восстановления.
