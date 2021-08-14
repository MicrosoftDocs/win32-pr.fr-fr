---
title: Tronçons suivants
description: Les itinéraires sont associés à un ou plusieurs tronçons suivants.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a8d73a0d553773537ca2efd67457498ff9710cf9e7834d6952fcf2a81c5c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790099"
---
# <a name="next-hops"></a>Tronçons suivants

Les itinéraires sont associés à un ou plusieurs tronçons suivants. Si la destination n’est pas sur un réseau directement connecté, le tronçon suivant est l’adresse du routeur suivant (ou réseau) sur le réseau sortant qui peut mieux acheminer les données vers la destination. Le meilleur itinéraire est l’itinéraire qui a le coût le plus faible, en fonction de la stratégie de routage en cours d’utilisation. Chaque tronçon suivant peut être utilisé pour transférer des données sur le chemin d’accès à la destination. Tous les itinéraires détenus par un client partagent un ensemble commun d’entrées de saut suivant qui ont été ajoutées par le client.

Chaque tronçon suivant est identifié de manière unique par l’adresse du tronçon suivant et l’index d’interface utilisé pour atteindre le tronçon suivant.

Si le tronçon suivant lui-même n’est pas directement connecté, il est marqué comme tronçon suivant « distant ». Dans ce cas, le redirecteur doit effectuer une autre recherche à l’aide de l’adresse réseau du tronçon suivant. Cette recherche est nécessaire pour trouver le tronçon suivant « local » utilisé pour atteindre le tronçon suivant distant et la destination.

Une entrée de saut suivant dans la table de routage comprend les éléments suivants :

-   Adresse réseau du tronçon suivant
-   Propriétaire du tronçon suivant
-   Identificateur de l’interface sortante
-   État du tronçon suivant
-   Indicateurs associés au tronçon suivant
-   Informations privées pour le propriétaire du tronçon suivant
-   Handle vers la destination correspondant au tronçon suivant distant

 

 




