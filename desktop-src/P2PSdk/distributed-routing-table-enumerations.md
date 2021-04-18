---
description: Les énumérations suivantes prennent en charge l’API de table de routage distribuée (DRT).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Énumérations de tables de routage distribuées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519905"
---
# <a name="distributed-routing-table-enumerations"></a>Énumérations de tables de routage distribuées

Les énumérations suivantes prennent en charge l’API de table de routage distribuée (DRT).



| Énumération                                                            | Description                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_étendue DRT**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Définit le jeu d’étendues IPv6 dans lequel DRT fonctionne lors de l’utilisation du transport UDP IPv6 créé par [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport). |
| [**\_indicateurs d’adresse DRT \_**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Définit l’ensemble des réponses qui peuvent être retournées par un nœud intermédiaire lors de l’exécution d’une recherche de clé.                                                         |
| [**\_État DRT**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Définit la connectivité possible et les États d’erreur d’un nœud local.                                                                                                   |
| [**\_type de correspondance DRT \_**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Définit l’exactitude des résultats retournés lorsqu’une recherche est effectuée.                                                                                                 |
| [**\_type de \_ modification de clé DRT LEAFSET \_ \_**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Définit l’ensemble des types de modifications qui peuvent être exécutés sur un nœud de groupe feuille local dans le cache DRT local.                                                                |
| [**\_type d’événement DRT \_**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Définit l’ensemble des événements qui peuvent être déclenchés par le DRT.                                                                                                              |
| [**\_mode de sécurité DRT \_**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Définit les modes de sécurité possibles de l’DRT. Cette énumération est un champ de la structure de [**\_ paramètres DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .                                   |
| [**\_État de l’inscription DRT \_**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Définit l’état d’une clé inscrite.                                                                                                                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Structures de table de routage distribué](distributed-routing-table-structures.md)
</dt> <dt>

[Fonctions de table de routage distribuée](distributed-routing-table-functions.md)
</dt> <dt>

[Référence de API Table de routage distribué](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



