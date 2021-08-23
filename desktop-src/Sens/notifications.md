---
description: Le service de notification d’événements système permet aux applications mobiles de recevoir des notifications d’événements système qui effectuent des analyses. Lorsque l’événement demandé se produit, SENS notifie l’application.
ms.assetid: 19311dec-4611-4104-b6e4-ff8f7c8af0e7
title: Notifications (service de notification d’événements système)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db908c48c38ccd39c6c9a427b77e3cefffc7b9bf8fad6e464ebdf146a138e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003967"
---
# <a name="notifications-system-event-notification-service"></a>Notifications (service de notification d’événements système)

Le service de notification d’événements système permet aux applications mobiles de recevoir des notifications d’événements système qui effectuent des analyses. Lorsque l’événement demandé se produit, SENS notifie l’application.

SENS peut notifier les applications de trois classes d’événements système :

-   Événements de réseau TCP/IP, tels que l’état d’une connexion réseau TCP/IP ou la qualité de la connexion.
-   Événements d’ouverture de session utilisateur.
-   Les événements de batterie et d’alimentation secteur.

Par exemple, une application peut s’abonner à l’un des événements système suivants :

-   Établissement de la connectivité réseau
-   Notification quand une destination spécifiée peut être atteinte dans les paramètres QOC (Quality of Connection) spécifiés
-   L’ordinateur a basculé sur la batterie
-   Le pourcentage de la puissance de la batterie restante est compris dans un paramètre spécifié
-   Les événements planifiés à l’aide du gestionnaire de synchronisation se produisent

**Windows Server 2008 R2 et Windows 7 :** L’abonné a un maximum de 3 minutes pour répondre à une notification sur les interfaces [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon) et [**ISensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2) . Au bout de 3 minutes, SENS annule l’appel aux abonnés et débloque le thread de notification. Si une longue opération est nécessaire pour répondre à la notification, retournez à partir de **ISensLogon** ou de **ISensLogon2** aussi rapidement que possible et ouvrez un autre thread pour le traitement.

 

 



