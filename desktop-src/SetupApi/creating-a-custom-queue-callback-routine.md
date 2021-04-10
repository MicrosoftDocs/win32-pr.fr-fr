---
description: En plus d’utiliser le rappel de file d’attente par défaut, vous pouvez écrire une routine de rappel personnalisée.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Création d’une routine de rappel de file d’attente personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866941"
---
# <a name="creating-a-custom-queue-callback-routine"></a>Création d’une routine de rappel de file d’attente personnalisée

En plus d’utiliser le rappel de file d’attente par défaut, vous pouvez écrire une routine de rappel personnalisée. Cette fonction doit avoir la même forme que [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Cela est utile si vous avez besoin d’une routine de rappel pour gérer une notification de manière différente de celle fournie par la routine de rappel de file d’attente par défaut.

Si seule une petite partie du comportement de la routine de rappel de la file d’attente par défaut doit être modifiée, vous pouvez créer une routine de rappel personnalisée pour filtrer les notifications, en gérant uniquement celles qui requièrent un comportement spécial et en appelant [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) pour les autres.

Par exemple, si vous souhaitez gérer les erreurs de suppression de fichier personnalisées, vous pouvez créer une fonction de rappel personnalisée, *MyCallBack*. Cette fonction intercepte et traite les notifications [**\_ DELETEERROR SPFILENOTIFY**](spfilenotify-deleteerror.md) et appelle la fonction de rappel de file d’attente par défaut pour toutes les autres notifications. *MyCallBack* retourne une valeur pour les notifications d’erreur de suppression. Pour toutes les autres notifications, *MyCallBack* transmet la valeur que la routine de rappel de file d’attente par défaut a renvoyée à la file d’attente.

Ce déroulement du contrôle est illustré dans le diagramme suivant.

![flèches et zones présentant le workflow pour une fonction de rappel personnalisée](images/callback.png)

> [!IMPORTANT]
> Si la fonction de rappel personnalisé appelle la routine de rappel de file d’attente par défaut, elle doit passer le pointeur void retourné par [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) à la routine de rappel par défaut.

 

 

 
