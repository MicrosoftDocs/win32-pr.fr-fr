---
title: Informations de référence sur l’API de routage de connexion à la demande
description: Les rubriques suivantes fournissent des détails sur l’application auxiliaire du routage de connexion à la demande.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9e046c1add8703e6603d925d2c80b03aab8d7eae3a352825e56ec907f3adb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685579"
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



 

 

 





