---
description: Utilisez les fonctions suivantes pour vous assurer qu’une application reçoit une notification de certains événements réseau.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Réception des notifications d’événements réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094562"
---
# <a name="receiving-notification-of-network-events"></a>Réception des notifications d’événements réseau

Utilisez les fonctions suivantes pour vous assurer qu’une application reçoit une notification de certains événements réseau.

Utilisez la fonction [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) pour demander une notification des modifications qui se produisent dans le mappage entre les adresses IP et les interfaces sur l’ordinateur local.

De même, la fonction [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) permet à une application de demander la notification de toute modification qui se produit dans la table de routage IP.

Les notifications fournies par ces fonctions ne spécifient pas ce qui a changé ; ils spécifient simplement qu’un événement a changé. Utilisez d’autres fonctions d’assistance IP, telles que [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) et [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), pour déterminer la nature exacte de la modification.

 

 



