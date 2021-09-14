---
description: Les structures suivantes prennent en charge les fonctions de l’API de table de routage distribuée (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Structures de table de routage distribué
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013928"
---
# <a name="distributed-routing-table-structures"></a>Structures de table de routage distribué

Les structures suivantes prennent en charge les fonctions de l’API de table de routage distribuée (DRT).



| Structure                                                  | Description                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_données DRT**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Contient un objet blob de données. Cette structure est utilisée par plusieurs fonctions DRT.                                                                                                                   |
| [**\_inscription DRT**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Contient l’enregistrement de la clé. Il s’agit d’un membre de la structure de [**\_ \_ résultat de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) . il s’agit d’un argument passé à [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey). |
| [**\_adresse DRT**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Contient des informations sur le point de terminaison d’un nœud DRT qui a participé à une recherche. Ces informations sont destinées à être utilisées dans le débogage des problèmes de connectivité.                                   |
| [**\_liste d’adresses DRT \_**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Contient un ensemble de structures d' [**\_ adresses DRT**](/windows/desktop/api/drt/ns-drt-drt_address) représentant les nœuds contactés lors de la recherche d’une clé.                                                             |
| [**\_fournisseur de sécurité DRT \_**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Définit l’interface qui doit être implémentée par un fournisseur de sécurité.                                                                                                                   |
| [**\_fournisseur de démarrage DRT \_**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Définit l’interface qui doit être implémentée par un fournisseur de données d’amorçage.                                                                                                                  |
| [**\_paramètres DRT**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Définit les paramètres DRT à l’initialisation. Cette structure est passée comme argument à [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).                                                                           |
| [**\_informations de recherche DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Définit une requête de recherche. Cette structure est passée comme argument à [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).                                                                             |
| [**résultat de la \_ recherche DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Contient un résultat de recherche. Cette structure est retournée par [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).                                                                                |
| [**\_données d’événement DRT \_**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Contient les données d’événement retournées par l’appel de [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) après qu’une application a reçu un signal d’événement.                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumérations de tables de routage distribuées](distributed-routing-table-enumerations.md)
</dt> <dt>

[Fonctions de table de routage distribuée](distributed-routing-table-functions.md)
</dt> <dt>

[Référence de API Table de routage distribué](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



