---
title: Tables de routage et entrées de table de routage
description: Le gestionnaire de tables de routage gère des tables de routage distinctes pour chaque famille de protocoles.
ms.assetid: 3848d93d-cc54-4a08-bd36-a9700cde6ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f118ec1d0a6f8fe4ef301654e139f217257c3a0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512221"
---
# <a name="route-tables-and-route-table-entries"></a>Tables de routage et entrées de table de routage

**Windows Server 2003 :** Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003. Les nouvelles applications doivent utiliser l’API du gestionnaire de table de routage version 2.

Le gestionnaire de tables de routage gère des tables de routage distinctes pour chaque famille de protocoles. Actuellement, la prise en charge explicite est fournie pour les familles de protocoles de routage IP (Internet Protocol) et IPX (Internet Packet Exchange). Quelle que soit la famille de protocoles, chaque entrée d’itinéraire contient les informations suivantes :

-   Réseau de destination.
-   Identificateur du protocole qui a ajouté l’itinéraire.
-   Index de l’interface par le biais duquel l’itinéraire a été obtenu. Cette valeur d’index est la valeur numérique assignée à une interface réseau (matérielle ou virtuelle) qui transmet les données sur le réseau. (Par exemple, une carte réseau Ethernet ou une carte sans fil 802.1 b.)
-   Adresse du routeur de tronçon suivant. RRAS utilise ce routeur pour transférer les paquets vers le réseau de destination si le réseau n’est pas directement connecté.
-   Heure à laquelle l’itinéraire a été créé ou mis à jour pour la dernière fois.
-   Durée de conservation de l’itinéraire dans la table de routage. Si ce laps de temps est écoulé et que l’itinéraire n’a pas été mis à jour, le gestionnaire de tables de routage supprime l’itinéraire de la table. Dans ce cas, l’itinéraire est réputé avoir *expiré*.
-   Données spécifiques à la famille de protocoles. Ces données sont transparentes en RTMv1. Toutefois, si ces données sont modifiées pour un itinéraire désigné comme « meilleur itinéraire », le gestionnaire de table de routage envoie une notification de changement d’itinéraire.
-   Données spécifiques au protocole de routage. Ces données sont totalement transparentes pour le gestionnaire de tables de routage, dans ce cas, les modifications apportées à ces données n’entraînent pas de notification de modification d’itinéraire.

Les valeurs suivantes, utilisées ensemble, identifient de façon unique un itinéraire dans la table de routage :

-   Réseau de destination
-   Identificateur de protocole
-   Index d’interface
-   Adresse du routeur du tronçon suivant

En général, le gestionnaire de tables de routage crée des entrées distinctes pour les itinéraires qui diffèrent dans l’une de ces valeurs de paramètre. Toutefois, une exception est faite pour les protocoles de routage qui ne conservent pas plus d’une entrée pour chaque réseau de destination. Pour ces protocoles, le gestionnaire de tables de routage ignore les différences dans l’index d’interface ou l’adresse de saut suivant. Un exemple de ce type de protocole est l’implémentation RRAS du chemin d’accès ouvert le plus rapide (OSPF).

 

 




