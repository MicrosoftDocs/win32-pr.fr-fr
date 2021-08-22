---
description: Un réseau est considéré comme le mécanisme de transport qui transmet les données d’un point à un autre.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fcfeb01caf9392cea597f0e80132ca0dd2830ea799e84b45775c6e438e0e1de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863086"
---
# <a name="network"></a>Réseau

Un réseau est considéré comme le mécanisme de transport qui transmet les données d’un point à un autre. Les fournisseurs de services TAPI gèrent les protocoles spécifiques requis pour effectuer des opérations telles que l’établissement d’une session de communication sur un réseau donné. Une application de serveur ou d’utilisateur final ne requiert normalement que des informations très générales sur le réseau, telles que le type d’adresse.

Certains types de réseaux courants :

-   **Pots (Plain Old Telephone Service) :** La voix et les données sont transmises au format analogique dans la *boucle locale* et sont transmises numériquement ailleurs. En général, un type de support par appel, un canal par ligne.
-   **RNIS (réseau numérique à intégration de services) :** Transmis numériquement. Vitesses allant jusqu’à 128 Kbits/s sur les lignes BRI-RNIS (Basic Rate Interface) et bien plus élevées sur les lignes PRI-RNIS. Au moins trois canaux et jusqu’à 32 canaux, pour une transmission simultanée et indépendante de la voix et des données. Norme internationale.
-   **T1/E1 :** Transmis numériquement. T1 est un lien de transmission avec une capacité de 1,544 Mbits/s, généralement utilisée pour connecter des réseaux sur des distances distantes. Dans l’Union européenne, T1 est appelé E1.
-   **Commutation 56 :** Signalement à 56 Kbits/s sur des lignes téléphoniques commutées, mais nécessite un équipement spécial. Limité aux appels à d’autres installations spécialement équipées.
-   **Centrex :** Services réseau centralisés par le biais de lignes téléphoniques classiques et utilisant l’équipement de la compagnie téléphonique. Aucun équipement spécial requis.
-   **PBX numériques (échange de branche privée) et systèmes clés :** Voix et données transmises sur des systèmes téléphoniques privés à l’aide d’interfaces propriétaires.
-   **Réseaux IP :** Voix et données transmises sur des réseaux à l’aide du protocole IP (Internet Protocol), comme Internet ou un intranet d’entreprise.

Notez que cette liste n'est pas exhaustive. Tout mécanisme de transport réseau peut être pris en charge, en fonction des fournisseurs de services appropriés.

 

 



