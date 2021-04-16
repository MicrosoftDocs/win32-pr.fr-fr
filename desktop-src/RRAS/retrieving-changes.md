---
title: Récupération des modifications
description: Une fois qu’un client s’est inscrit pour la notification de certaines modifications et qu’une ou plusieurs de ces modifications se produisent, le client reçoit une notification de la part du gestionnaire de tables de routage.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ccf66d8a1df671cbd9059c444cf26321911bb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507135"
---
# <a name="retrieving-changes"></a><span data-ttu-id="ba114-103">Récupération des modifications</span><span class="sxs-lookup"><span data-stu-id="ba114-103">Retrieving Changes</span></span>

<span data-ttu-id="ba114-104">Une fois qu’un client s’est inscrit pour la notification de certaines modifications et qu’une ou plusieurs de ces modifications se produisent, le client reçoit une notification de la part du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="ba114-104">Once a client has registered for notification of certain changes and one or more of these changes occurs, the client receives a notification from the routing table manager.</span></span> <span data-ttu-id="ba114-105">Le gestionnaire de table de routage utilise le rappel de [**\_ \_ rappel d’événement RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) fourni dans un appel précédent à [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span><span class="sxs-lookup"><span data-stu-id="ba114-105">The routing table manager uses the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback that was supplied in a previous call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity).</span></span> <span data-ttu-id="ba114-106">Le gestionnaire de tables de routage indique qu’un \_ événement de notification de modification RTM s’est \_ produit.</span><span class="sxs-lookup"><span data-stu-id="ba114-106">The routing table manager indicates that a RTM\_CHANGE\_NOTIFICATION event has occurred.</span></span>

<span data-ttu-id="ba114-107">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [utiliser le rappel de notification d’événement](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="ba114-107">For sample code that shows how to use these functions, see [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




