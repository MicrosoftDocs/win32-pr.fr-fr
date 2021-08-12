---
description: cette section décrit l’implémentation du protocole de multidiffusion PGM (pragmatic general multicast) dans Windows, souvent appelée diffusion fiable. la multidiffusion fiable est implémentée par le biais de Windows sockets dans Windows Server 2003 et versions ultérieures.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programmation de la multidiffusion fiable (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c34365bdc8db553d24182fcb193dc03177627ccf9b00a03f309ab4cf7bbe01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559951"
---
# <a name="reliable-multicast-programming-pgm"></a>Programmation de la multidiffusion fiable (PGM)

cette section décrit l’implémentation du protocole de multidiffusion PGM (pragmatic general multicast) dans Windows, souvent appelée diffusion fiable. la multidiffusion fiable est implémentée par le biais de Windows sockets dans Windows Server 2003 et versions ultérieures.

**Windows XP :** Le PGM est pris en charge uniquement lorsque Microsoft Message Queuing (MSMQ) 3,0 est installé.

Le protocole PGM est un protocole de multidiffusion fiable et évolutif qui permet aux destinataires de détecter la perte, de demander la retransmission des données perdues ou de notifier une application de perte irrécupérable. Le protocole PGM est un protocole fiable pour le récepteur, ce qui signifie que le récepteur est chargé de vérifier que toutes les données sont reçues, absolving l’expéditeur de la responsabilité de la réception.

Le PGM est approprié pour les applications qui nécessitent la remise de données en multidiffusion sans doublon de plusieurs sources à plusieurs destinataires. Le PGM ne prend pas en charge la livraison reconnue et ne garantit pas le classement des paquets à partir de plusieurs expéditeurs.

Pour plus d’informations sur le PGM, reportez-vous à la RFC 3208 disponible sur [www.ietf.org](https://www.ietf.org/).

Cette section décrit comment utiliser la multidiffusion fiable sur Windows. les rubriques suivantes expliquent les différents aspects de la création d’une application de multidiffusion fiable à l’aide de Windows sockets :

-   [Expéditeurs et destinataires PGM](pgm-senders-and-receivers.md)
-   [Options de l’expéditeur PGM](pgm-sender-options.md)
-   [Envoi et réception de données PGM](sending-and-receiving-pgm-data.md)
-   [Hébergement multiple et PGM](multihoming-and-pgm.md)
-   [Options de socket PGM](pgm-socket-options.md)

 

 



