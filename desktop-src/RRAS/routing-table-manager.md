---
title: Gestionnaire de table de routage
description: Le gestionnaire de tables de routage est le référentiel central des informations de routage pour tous les protocoles de routage qui fonctionnent sous le service de routage et d’accès à distance (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511812"
---
# <a name="routing-table-manager"></a>Gestionnaire de table de routage

Le gestionnaire de tables de routage est le référentiel central des informations de routage pour tous les protocoles de routage qui fonctionnent sous le service de routage et d’accès à distance (RRAS). Elle avertit les clients lorsque des modifications ont eu lieu et permet aux clients d’échanger des informations privées.

Le gestionnaire de tables de routage fournit des informations de routage à tous les clients concernés, tels que les protocoles de routage, les programmes de gestion et les programmes de surveillance. Le gestionnaire de tables de routage détermine également le meilleur itinéraire vers chaque réseau de destination connu des protocoles de routage. Le gestionnaire de tables de routage détermine cet itinéraire en fonction des priorités de protocole de routage et des métriques associées aux itinéraires. La personne qui administre le routeur peut configurer des priorités de protocole de routage à l’aide de la console de gestion RRAS.

Le gestionnaire de tables de routage transmet les informations les plus bonnes aux redirecteurs (une par famille d’adresses, ou une par interface) et à tous les clients intéressés.

Chaque client s’inscrit auprès du gestionnaire de tables de routage et, en retour, il reçoit un descripteur utilisé par le client pour ajouter ou supprimer des itinéraires. Les clients peuvent récupérer les informations stockées dans la table de routage. En outre, les clients peuvent s’inscrire auprès du gestionnaire de tables de routage pour recevoir la notification des modifications apportées au meilleur itinéraire vers une destination.

 

 




