---
title: Indicateurs de requête de table de routage
description: Utilisez ces constantes pour les requêtes de table de routeur.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Indicateurs de requête de table de routage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840910"
---
# <a name="routing-table-query-flags"></a>Indicateurs de requête de table de routage

Utilisez ces constantes pour les requêtes de table de routeur.



| Constante              | Valeur      | Description                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| \_correspondance RTM \_ aucune      | 0x00000000 | Correspond à aucun des critères ; tous les itinéraires pour la destination sont retournés. |
| \_propriétaire de correspondance RTM \_     | 0x00000001 | Correspond aux itinéraires ayant le même propriétaire.                                            |
| RTM \_ match \_ voisin | 0x00000002 | Met en correspondance les itinéraires avec le même voisin.                                     |
| \_correspondance RTM \_ Préférences      | 0x00000004 | Correspond aux itinéraires qui ont la même préférence.                              |
| version RTM \_ match \_ NEXTHOP   | 0x00000008 | Correspond aux itinéraires qui ont le même tronçon suivant.                                |
| \_interface de correspondance RTM \_ | 0x00000010 | Correspond aux itinéraires qui se trouvent sur la même interface.                             |
| mise en \_ correspondance RTM \_ complète      | 0x0000FFFF | Met en correspondance les itinéraires avec tous les critères.                                          |
| \_meilleur \_ protocole RTM   | 0          | Retourne un itinéraire quel que soit le protocole qui le possède.                      |
| RTM \_ ce \_ protocole   | ~0         | Retourne le meilleur itinéraire pour le protocole appelant.                           |



 

 

 




