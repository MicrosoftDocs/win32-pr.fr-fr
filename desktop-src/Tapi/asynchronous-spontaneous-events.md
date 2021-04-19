---
description: Outre celles décrites ci-dessus, il existe une autre classe d’événements asynchrones.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Événements spontanés asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533977"
---
# <a name="asynchronous-spontaneous-events"></a><span data-ttu-id="18fd4-103">Événements spontanés asynchrones</span><span class="sxs-lookup"><span data-stu-id="18fd4-103">Asynchronous Spontaneous Events</span></span>

<span data-ttu-id="18fd4-104">Outre celles décrites ci-dessus, il existe une autre classe d’événements asynchrones.</span><span class="sxs-lookup"><span data-stu-id="18fd4-104">There is another class of asynchronous events besides those described above.</span></span> <span data-ttu-id="18fd4-105">Ces événements sont « spontanés » dans la mesure où ils ne sont pas des résultats directs des demandes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="18fd4-105">These events are "spontaneous" in the sense that they are not direct results of corresponding requests.</span></span> <span data-ttu-id="18fd4-106">Ces événements sont détectés dans de tels cas lorsqu’un appel entrant arrive ou lorsqu’un appel sortant passe d’une « sonnerie » à l’état « réponse ».</span><span class="sxs-lookup"><span data-stu-id="18fd4-106">These events are detected in such cases as when an incoming call arrives, or when an outbound call goes from a "ringing" to an "answering" state.</span></span> <span data-ttu-id="18fd4-107">Lorsque TAPI initialise d’abord les interactions avec le TSPI pour un appareil particulier, il passe un pointeur vers une procédure de rappel à appeler pour signaler ces événements spontanés.</span><span class="sxs-lookup"><span data-stu-id="18fd4-107">When TAPI first initializes interactions with the TSPI for a particular device, it passes a pointer to a callback procedure to be called for reporting such spontaneous events.</span></span> <span data-ttu-id="18fd4-108">Ce pointeur de procédure est un handle d’appareil que le fournisseur de services comprend comme l’un des paramètres réels du rappel.</span><span class="sxs-lookup"><span data-stu-id="18fd4-108">Along with this procedure pointer is a device handle that the service provider includes as one of the actual parameters to the callback.</span></span>

 

 



