---
title: Modifications apportées au meilleur itinéraire sur un réseau
description: Une modification de l’une des valeurs suivantes pour le meilleur itinéraire vers un réseau de destination donné entraîne la génération par le gestionnaire de tables de routage d’un message de notification envoyé à chaque client inscrit et aux redirecteurs
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fe96a0b339325c2290c346ba581d5b892db24d1cd972f7a83a0b2ec525eeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030359"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Modifications apportées au meilleur itinéraire sur un réseau

**Windows Server 2003 :** cette api a été remplacée par l’api du [gestionnaire de Table de routage Version 2](about-routing-table-manager-version-2.md) et ne sera pas disponible au-delà de Windows Server 2003. Les nouvelles applications doivent utiliser l’API du gestionnaire de table de routage version 2.

Une modification de l’une des valeurs suivantes pour le meilleur itinéraire vers un réseau de destination donné entraîne la génération par le gestionnaire de tables de routage d’un message de notification envoyé à chaque client inscrit et aux redirecteurs :

-   Identificateur de protocole
-   Index d’interface
-   Adresse du routeur du tronçon suivant
-   Données spécifiques à la famille de protocoles qui incluent les métriques d’itinéraire

Une modification de l’identificateur de protocole, de l’index d’interface ou de l’adresse du routeur de saut suivant se produit lorsqu’une nouvelle entrée de routage plus performante est ajoutée, ou lorsque l’entrée la mieux adaptée est supprimée ou obsolète, et laisse un autre itinéraire en tant que nouveau meilleur itinéraire.

 

 




