---
description: Un réseau est considéré comme le mécanisme de transport qui transmet les données d’un point à un autre.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485313"
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

 

 



