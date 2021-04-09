---
title: Services système critiques
description: Les services système critiques ne peuvent pas être arrêtés et redémarrés par le gestionnaire de redémarrage sans redémarrage du système. Les mises à jour d’un fichier ou d’une ressource en cours d’utilisation par l’un de ces services nécessitent un redémarrage du système.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029903"
---
# <a name="critical-system-services"></a>Services système critiques

Les services système critiques ne peuvent pas être arrêtés et redémarrés par le gestionnaire de redémarrage sans redémarrage du système. Les mises à jour d’un fichier ou d’une ressource en cours d’utilisation par l’un de ces services nécessitent un redémarrage du système.

**Pour déterminer si un processus est un service système critique.**

1.  Inscrivez le processus à l’aide de la fonction [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .
2.  Appelez la fonction [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) pour accéder à la structure des informations sur le [**\_ processus \_ RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .
3.  Le membre **ApplicationType** de la structure [**d' \_ \_ informations de processus RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) retournée contient une valeur d’énumération de [**\_ \_ type d’application RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) . Cette valeur est définie sur **RmCriticial** pour un processus système critique.

Les services système critiques incluent smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe avec RPCSS et svchost.exe avec DCOM/PnP.

 

 




