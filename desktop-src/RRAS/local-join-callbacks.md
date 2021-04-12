---
title: Rappels de jointure locale
description: Une fois que le gestionnaire de groupe de multidiffusion est averti par IGMP que de nouveaux récepteurs sont présents pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le \_ rappel de rappel de jointure locale PMGM \_ \_ au protocole de routage qui possède l’interface, le cas échéant.
ms.assetid: 136f86e0-380d-4158-a9dd-c6de1c7f6689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c97f0e16e08bc3781b946a51f69d2b0d65b3272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462362"
---
# <a name="local-join-callbacks"></a><span data-ttu-id="d0eb9-103">Rappels de jointure locale</span><span class="sxs-lookup"><span data-stu-id="d0eb9-103">Local Join Callbacks</span></span>

<span data-ttu-id="d0eb9-104">Une fois que le gestionnaire de groupe de multidiffusion est averti par IGMP que de nouveaux récepteurs sont présents pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ \_ \_ rappel de jointure locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) au protocole de routage qui possède l’interface, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d0eb9-104">After the multicast group manager is notified by IGMP that new receivers are present for a group on an interface, the multicast group manager invokes the [**PMGM\_LOCAL\_JOIN\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback) callback to the routing protocol that owns the interface if one exists.</span></span> <span data-ttu-id="d0eb9-105">Ce rappel avertit le protocole de routage de la modification.</span><span class="sxs-lookup"><span data-stu-id="d0eb9-105">This callback notifies the routing protocol of the change.</span></span>

<span data-ttu-id="d0eb9-106">Ce rappel et le rappel de rappel de la [**\_ \_ sortie \_ locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) sont utilisés pour synchroniser le transfert entre les protocoles IGMP et de routage.</span><span class="sxs-lookup"><span data-stu-id="d0eb9-106">This callback and the [**PMGM\_LOCAL\_LEAVE\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback) callback are used to synchronize forwarding between IGMP and routing protocols.</span></span>

 

 




