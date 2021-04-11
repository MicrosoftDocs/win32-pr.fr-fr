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
# <a name="on-demand-connection-routing-helper-api-reference"></a><span data-ttu-id="7044b-103">Informations de référence sur l’API de routage de connexion à la demande</span><span class="sxs-lookup"><span data-stu-id="7044b-103">On Demand Connection Routing Helper API reference</span></span>

<span data-ttu-id="7044b-104">Les rubriques suivantes fournissent des détails sur l’application auxiliaire du routage de connexion à la demande.</span><span class="sxs-lookup"><span data-stu-id="7044b-104">The following topics provide details for the On Demand Connection Routing Helper.</span></span>



| <span data-ttu-id="7044b-105">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7044b-105">Reference</span></span>                                                                          | <span data-ttu-id="7044b-106">Description</span><span class="sxs-lookup"><span data-stu-id="7044b-106">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7044b-107">**OnDemandGetRoutingHint**</span><span class="sxs-lookup"><span data-stu-id="7044b-107">**OnDemandGetRoutingHint**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | <span data-ttu-id="7044b-108">Recherchez une destination dans le cache de demande d’itinéraire et, si une correspondance est trouvée, retourne l’ID d’interface correspondant.</span><span class="sxs-lookup"><span data-stu-id="7044b-108">Look up a destination in the Route Request cache and, if a match is found, returns the corresponding Interface ID.</span></span><br/>                                               |
| [<span data-ttu-id="7044b-109">**OnDemandRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="7044b-109">**OnDemandRegisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | <span data-ttu-id="7044b-110">Inscrivez-vous pour être informé de la modification du cache des demandes de routage.</span><span class="sxs-lookup"><span data-stu-id="7044b-110">Register to be notified when the Route Requests cache is modified.</span></span><br/>                                                                                               |
| [<span data-ttu-id="7044b-111">**OnDemandUnregisterNotification**</span><span class="sxs-lookup"><span data-stu-id="7044b-111">**OnDemandUnregisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | <span data-ttu-id="7044b-112">Annulez l’inscription pour les notifications et nettoyez les ressources.</span><span class="sxs-lookup"><span data-stu-id="7044b-112">Unregister for notifications and clean up resources.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="7044b-113">**contexte de l' \_ interface NET \_**</span><span class="sxs-lookup"><span data-stu-id="7044b-113">**NET\_INTERFACE\_CONTEXT**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | <span data-ttu-id="7044b-114">Contexte d’interface qui fait partie de la structure de la table de contexte de l' [**\_ interface \_ \_ net**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) .</span><span class="sxs-lookup"><span data-stu-id="7044b-114">The interface context that is part of the [**NET\_INTERFACE\_CONTEXT\_TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) structure.</span></span><br/>                                       |
| [<span data-ttu-id="7044b-115">**TABLE de contexte de l' \_ interface NET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7044b-115">**NET\_INTERFACE\_CONTEXT\_TABLE**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | <span data-ttu-id="7044b-116">Tableau des structures [**de \_ \_ contexte d’interface net**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .</span><span class="sxs-lookup"><span data-stu-id="7044b-116">The table of [**NET\_INTERFACE\_CONTEXT**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) structures.</span></span><br/>                                                                                |
| [<span data-ttu-id="7044b-117">**GetInterfaceContextTableForHostName**</span><span class="sxs-lookup"><span data-stu-id="7044b-117">**GetInterfaceContextTableForHostName**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | <span data-ttu-id="7044b-118">Cette fonction récupère une table de contexte d’interface pour le nom d’hôte et le filtre de profil de connexion donnés.</span><span class="sxs-lookup"><span data-stu-id="7044b-118">This function retrieves an interface context table for the given hostname and connection profile filter.</span></span><br/>                                                         |
| [<span data-ttu-id="7044b-119">**FreeInterfaceContextTable**</span><span class="sxs-lookup"><span data-stu-id="7044b-119">**FreeInterfaceContextTable**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | <span data-ttu-id="7044b-120">Cette fonction libère la table de contexte d’interface récupérée à l’aide de la fonction [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .</span><span class="sxs-lookup"><span data-stu-id="7044b-120">This function frees the interface context table retrieved using the [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) function.</span></span><br/> |



 

 

 





