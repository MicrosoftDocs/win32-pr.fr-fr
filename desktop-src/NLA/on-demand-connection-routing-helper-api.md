---
title: Informations de référence sur l’API de routage de connexion à la demande
description: Les rubriques suivantes fournissent des détails sur l’application auxiliaire du routage de connexion à la demande.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049c62d7784af6430e8b93240ec79464b098043
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100805"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a>Informations de référence sur l’API de routage de connexion à la demande

Les rubriques suivantes fournissent des détails sur l’application auxiliaire du routage de connexion à la demande.



| Informations de référence                                                                          | Description                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnDemandGetRoutingHint**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | Recherchez une destination dans le cache de demande d’itinéraire et, si une correspondance est trouvée, retourne l’ID d’interface correspondant.<br/>                                               |
| [**OnDemandRegisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | Inscrivez-vous pour être informé de la modification du cache des demandes de routage.<br/>                                                                                               |
| [**OnDemandUnregisterNotification**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | Annulez l’inscription pour les notifications et nettoyez les ressources.<br/>                                                                                                             |
| [**contexte de l' \_ interface NET \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | Contexte d’interface qui fait partie de la structure de la table de contexte de l' [**\_ interface \_ \_ net**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) .<br/>                                       |
| [**TABLE de contexte de l' \_ interface NET \_ \_**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | Tableau des structures [**de \_ \_ contexte d’interface net**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .<br/>                                                                                |
| [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | Cette fonction récupère une table de contexte d’interface pour le nom d’hôte et le filtre de profil de connexion donnés.<br/>                                                         |
| [**FreeInterfaceContextTable**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | Cette fonction libère la table de contexte d’interface récupérée à l’aide de la fonction [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .<br/> |



 

 

 





