---
title: Récupération de l’état des modifications et ignorer les modifications
description: Le client peut interroger le gestionnaire de table de routage pour déterminer si une notification de modification apportée à une destination est en attente en appelant RtmGetChangeStatus. Cette fonction retourne la valeur TRUE jusqu’à ce que l’appelant récupère cette modification en appelant RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672269"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a><span data-ttu-id="95abb-104">Récupération de l’état des modifications et ignorer les modifications</span><span class="sxs-lookup"><span data-stu-id="95abb-104">Retrieving Change Status and Ignoring Changes</span></span>

<span data-ttu-id="95abb-105">Le client peut interroger le gestionnaire de table de routage pour déterminer si une notification de modification apportée à une destination est en attente en appelant [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span><span class="sxs-lookup"><span data-stu-id="95abb-105">The client can query the routing table manager to find out if a notification of a change to a destination is pending by calling [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus).</span></span> <span data-ttu-id="95abb-106">Cette fonction retourne la **valeur true** jusqu’à ce que l’appelant récupère cette modification en appelant [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span><span class="sxs-lookup"><span data-stu-id="95abb-106">This function returns **TRUE** until the caller retrieves this change by calling [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).</span></span>

<span data-ttu-id="95abb-107">Un client peut utiliser cette requête pour éviter d’effectuer une action qui devrait être annulée après la réception et le traitement de la notification de modification.</span><span class="sxs-lookup"><span data-stu-id="95abb-107">A client can use this query to avoid performing an action that would have to be undone after the change notification is received and processed.</span></span> <span data-ttu-id="95abb-108">L’utilisation de cette fonctionnalité permet au client de travailler efficacement en reportant certaines opérations à un moment ultérieur.</span><span class="sxs-lookup"><span data-stu-id="95abb-108">Using this feature allows the client to work efficiently by deferring certain operations to a later time.</span></span>

<span data-ttu-id="95abb-109">Le client peut également ignorer une notification de modification en attente pour une destination en appelant [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="95abb-109">The client can also ignore a pending change notification for a destination by calling [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span> <span data-ttu-id="95abb-110">Un appel ultérieur à [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) ne retourne pas cette destination, sauf si une autre modification survient après l’appel à [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span><span class="sxs-lookup"><span data-stu-id="95abb-110">A later call to [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) does not return this destination unless another change occurs after the call to [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).</span></span>

 

 




