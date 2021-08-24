---
description: Le paramètre Protocol dans socket et WSASocket est un identificateur qui établit un type de réseau et une méthode pour identifier les différents protocoles de transport qui s’exécutent sur le réseau.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Famille IPX d’identificateurs de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549e1dbdb9d379e87ed8e22871188b0b7762e924a695721f1c860fce14f2a2e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733649"
---
# <a name="ipx-family-of-protocol-identifiers"></a>Famille IPX d’identificateurs de protocole

Le paramètre *Protocol* dans [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) est un identificateur qui établit un type de réseau et une méthode pour identifier les différents protocoles de transport qui s’exécutent sur le réseau. Contrairement à IP, IPX n’utilise pas une seule valeur de protocole pour sélectionner une pile de transport. Étant donné qu’il n’est pas nécessaire d’utiliser une valeur spécifique pour chaque protocole de transport, nous sommes libres de les affecter de manière pratique pour les applications Winsock. Nous évitons les valeurs comprises entre 0 et 255 afin d’éviter les collisions avec les valeurs de protocole inet de PF correspondantes \_ .



| Name         | Valeur       | Types de Sockets              | Description                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| Réservé     | 0-255       |                           | Réservé aux valeurs de protocole de PF \_ inet.              |
| \_IPX NSPROTO | 1000-1255 | \_DGRAM chaussette \_ brute     | Service de datagramme pour IPX.                           |
| NSPROTO \_ SPX | 1256        | \_flux de chaussette \_ SEQPKT | Échange de paquets fiable utilisant des paquets de taille fixe. |



 

> [!Note]  
> Quand NSPROTO \_ SPX est spécifié, le protocole SPX II est utilisé automatiquement si les deux points de terminaison sont en mesure de le faire.

 

 

 



