---
description: Utilisez les fonctions suivantes pour vous assurer qu’une application reçoit une notification de certains événements réseau.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Réception des notifications d’événements réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28225654bc7e4119f76eff21425e96dda83f628b88d16be9cdfc370d9fa63712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146612"
---
# <a name="receiving-notification-of-network-events"></a>Réception des notifications d’événements réseau

Utilisez les fonctions suivantes pour vous assurer qu’une application reçoit une notification de certains événements réseau.

Utilisez la fonction [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) pour demander une notification des modifications qui se produisent dans le mappage entre les adresses IP et les interfaces sur l’ordinateur local.

De même, la fonction [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) permet à une application de demander la notification de toute modification qui se produit dans la table de routage IP.

Les notifications fournies par ces fonctions ne spécifient pas ce qui a changé ; ils spécifient simplement qu’un événement a changé. Utilisez d’autres fonctions d’assistance IP, telles que [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) et [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), pour déterminer la nature exacte de la modification.

 

 



