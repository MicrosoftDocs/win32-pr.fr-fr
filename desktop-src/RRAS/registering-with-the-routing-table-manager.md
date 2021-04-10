---
title: Inscription auprès du gestionnaire de tables de routage
description: Pour qu’un client puisse accéder à la table de routage, il doit d’abord s’inscrire auprès du gestionnaire de tables de routage à l’aide de la fonction RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Gestionnaire de table de routage, version 2 RRAS, inscription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196700"
---
# <a name="registering-with-the-routing-table-manager"></a><span data-ttu-id="a5f87-104">Inscription auprès du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="a5f87-104">Registering with the Routing Table Manager</span></span>

<span data-ttu-id="a5f87-105">Pour qu’un client puisse accéder à la table de routage, il doit d’abord s’inscrire auprès du gestionnaire de tables de routage à l’aide de la fonction [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .</span><span class="sxs-lookup"><span data-stu-id="a5f87-105">Before a client can access the routing table, it first must register with the routing table manager using the [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function.</span></span>

<span data-ttu-id="a5f87-106">Lorsqu’un client s’inscrit, il passe au gestionnaire de table de routage une structure d' [**\_ \_ informations d’entité RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) .</span><span class="sxs-lookup"><span data-stu-id="a5f87-106">When a client registers, it passes to the routing table manager an [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structure.</span></span> <span data-ttu-id="a5f87-107">Cette structure contient les informations qui identifient de façon unique un client, la famille d’adresses et l’instance du gestionnaire de tables de routage avec lequel le client est inscrit.</span><span class="sxs-lookup"><span data-stu-id="a5f87-107">This structure contains the information that uniquely identifies a client, the address family, and the instance of the routing table manager with which the client is registering.</span></span> <span data-ttu-id="a5f87-108">Un client peut également établir le rappel de [**\_ \_ rappel d’événement RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) .</span><span class="sxs-lookup"><span data-stu-id="a5f87-108">A client can also establish the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback.</span></span> <span data-ttu-id="a5f87-109">Le gestionnaire de tables de routage utilise ce rappel pour notifier au client des événements tels que les notifications de modifications et les inscriptions des clients.</span><span class="sxs-lookup"><span data-stu-id="a5f87-109">The routing table manager will use this callback to notify the client of events such as change notifications and client registrations.</span></span>

<span data-ttu-id="a5f87-110">Le gestionnaire de table de routage termine son traitement d’inscription et retourne un descripteur au client.</span><span class="sxs-lookup"><span data-stu-id="a5f87-110">The routing table manager completes its registration processing and returns a handle to the client.</span></span> <span data-ttu-id="a5f87-111">Le client doit utiliser ce handle pour tous les appels suivants aux fonctions RTMv2.</span><span class="sxs-lookup"><span data-stu-id="a5f87-111">The client must use this handle for all subsequent calls to RTMv2 functions.</span></span>

<span data-ttu-id="a5f87-112">La fonction [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) utilisée dans RTMv2 est analogue à la fonction [**RtmRegisterClient**](rtmregisterclient.md) utilisée dans RTMv1.</span><span class="sxs-lookup"><span data-stu-id="a5f87-112">The [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function that is used in RTMv2 is analogous to the [**RtmRegisterClient**](rtmregisterclient.md) function that is used in RTMv1.</span></span> <span data-ttu-id="a5f87-113">La fonction **RtmRegisterClient** est obsolète, sauf pour les clients utilisant IPX.</span><span class="sxs-lookup"><span data-stu-id="a5f87-113">The **RtmRegisterClient** function is obsolete, except for clients using IPX.</span></span>

<span data-ttu-id="a5f87-114">Une fois qu’un client a terminé l’interaction avec le gestionnaire de tables de routage, il doit appeler [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span><span class="sxs-lookup"><span data-stu-id="a5f87-114">Once a client has finished interacting with the routing table manager, it must call [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span></span> <span data-ttu-id="a5f87-115">Le gestionnaire de tables de routage détruit le descripteur associé au client.</span><span class="sxs-lookup"><span data-stu-id="a5f87-115">The routing table manager destroys the handle associated with the client.</span></span> <span data-ttu-id="a5f87-116">Pour éviter les fuites de mémoire, le client doit s’assurer qu’il libère tous les descripteurs et supprime tous les itinéraires et tronçons suivants qu’il détient avant d’appeler **RtmDeregisterEntity**.</span><span class="sxs-lookup"><span data-stu-id="a5f87-116">To avoid memory leaks, the client must ensure that it releases all handles and deletes all the routes and next hops that it owns before calling **RtmDeregisterEntity**.</span></span>

<span data-ttu-id="a5f87-117">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [s’inscrire auprès du gestionnaire de tables de routage](register-with-the-routing-table-manager.md) et [utiliser le rappel de notification d’événement](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="a5f87-117">For sample code that shows how to use these functions, see [Register with the Routing Table Manager](register-with-the-routing-table-manager.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




