---
description: Utilisation des e/s bloquantes, des e/s non bloquantes avec notification asynchrone des événements réseau et des e/s avec chevauchement avec indication d’achèvement dans Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: E/s de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113002"
---
# <a name="socket-io"></a>E/s de socket

Il existe trois façons principales d’exécuter des e/s dans Windows Sockets 2 :

-   Blocage des e/s.
-   Des e/s non bloquantes, ainsi que des notifications asynchrones d’événements réseau.
-   E/s avec chevauchement avec indication d’achèvement.

Nous décrivons chaque méthode dans les sections suivantes. Le blocage des e/s est le comportement par défaut, le mode non bloquant peut être utilisé sur n’importe quel Socket placé en mode non bloquant, et les e/s avec chevauchement peuvent se produire uniquement sur les sockets créés avec l’attribut Overlapped. Il est également intéressant de noter que les deux appels pour l’envoi de : [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) et [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) et les deux appels pour la réception : [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) et [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) implémentent chacun les trois méthodes d’e/s. Les fournisseurs de services déterminent comment effectuer l’opération d’e/s en fonction des modes de socket, des attributs et des valeurs de paramètre d’entrée.

 

 
