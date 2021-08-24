---
description: Les applications peuvent mieux adapter leur comportement à l’état d’alimentation actuel de l’ordinateur en s’inscrivant pour les événements d’alimentation.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Inscription pour les événements d’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c360905800ad3fdce047e16a0244cd3dbf1ca312f18154f0be0c36b75e546d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143322"
---
# <a name="registering-for-power-events"></a>Inscription pour les événements d’alimentation

Les applications peuvent mieux adapter leur comportement à l’état d’alimentation actuel de l’ordinateur en s’inscrivant pour les événements d’alimentation. Une application doit s’inscrire à chaque événement de changement d’alimentation qui peut avoir un impact sur son comportement.

Une application ou un service utilise la fonction [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) pour s’inscrire aux notifications. Lorsque le paramètre d’alimentation correspondant change, le système envoie des notifications comme suit :

-   Une application reçoit un [**message WM \_ POWERBROADCAST**](wm-powerbroadcast.md) avec un *wParam* de [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) et un *lParam* qui pointe vers une structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .
-   Un service reçoit un appel à la fonction de rappel [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) qu’il a inscrit en appelant la fonction [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) . Le paramètre *lpEventData* envoyé à la fonction de rappel *HandlerEx* pointe vers une structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

Dans la structure de [**\_ paramètre POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) , le membre **PowerSetting** contient le GUID qui identifie la notification et le membre de **données** contient la nouvelle valeur du paramètre d’alimentation.

Pour obtenir la liste des GUID des paramètres d’alimentation pour les notifications les plus utiles pour les applications, consultez [**GUID des paramètres d’alimentation**](power-setting-guids.md).

 

 
