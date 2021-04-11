---
title: Énumération des entités inscrites
description: Une fois qu’un client est inscrit, le client peut obtenir une liste de tous les autres clients qui se sont inscrits auprès du gestionnaire de tables de routage. Certains clients doivent effectuer certaines opérations si la présence d’un type particulier de client est détectée.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029261"
---
# <a name="enumerating-registered-entities"></a><span data-ttu-id="5314f-104">Énumération des entités inscrites</span><span class="sxs-lookup"><span data-stu-id="5314f-104">Enumerating Registered Entities</span></span>

<span data-ttu-id="5314f-105">Une fois qu’un client est inscrit, le client peut obtenir une liste de tous les autres clients qui se sont inscrits auprès du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="5314f-105">After a client has registered, the client can obtain a list of all the other clients that have registered with the routing table manager.</span></span> <span data-ttu-id="5314f-106">Certains clients doivent effectuer certaines opérations si la présence d’un type particulier de client est détectée.</span><span class="sxs-lookup"><span data-stu-id="5314f-106">Some clients must perform certain operations if the presence of a particular type of client is detected.</span></span>

<span data-ttu-id="5314f-107">Le client peut appeler la fonction [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) .</span><span class="sxs-lookup"><span data-stu-id="5314f-107">The client can call the [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) function.</span></span> <span data-ttu-id="5314f-108">Une mémoire tampon des structures d' [**\_ \_ informations d’entité RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) est retournée.</span><span class="sxs-lookup"><span data-stu-id="5314f-108">A buffer of [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structures is returned.</span></span> <span data-ttu-id="5314f-109">Une fois que le client a traité ces informations, le client doit appeler [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) pour libérer les descripteurs dans les structures d' **\_ \_ informations d’entité RTM** .</span><span class="sxs-lookup"><span data-stu-id="5314f-109">After the client has processed this information, the client should call [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) to release the handles in the **RTM\_ENTITY\_INFO** structures.</span></span>

<span data-ttu-id="5314f-110">Si le client du gestionnaire de table de routage a fourni une fonction de rappel dans l’appel à [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), le client est averti lorsque d’autres clients s’inscrivent ou annulent l’inscription.</span><span class="sxs-lookup"><span data-stu-id="5314f-110">If the routing table manager client supplied a callback function in the call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), the client is notified when any other clients register or unregister.</span></span>

<span data-ttu-id="5314f-111">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [énumérer les entités inscrites](enumerate-the-registered-entities.md) et [utiliser le rappel de notification d’événement](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="5314f-111">For sample code that shows how to use these functions, see [Enumerate the Registered Entities](enumerate-the-registered-entities.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




