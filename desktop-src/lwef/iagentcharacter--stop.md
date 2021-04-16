---
title: IAgentCharacter arrêter
description: IAgentCharacter arrêter
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380196"
---
# <a name="iagentcharacterstop"></a><span data-ttu-id="85179-103">IAgentCharacter :: Stop</span><span class="sxs-lookup"><span data-stu-id="85179-103">IAgentCharacter::Stop</span></span>

<span data-ttu-id="85179-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85179-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

<span data-ttu-id="85179-105">Arrête l’animation spécifiée (requête) et la supprime de la file d’attente d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="85179-105">Stops the specified animation (request) and removes it from the character's animation queue.</span></span>

-   <span data-ttu-id="85179-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="85179-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="85179-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="85179-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="85179-108">ID de la demande à arrêter.</span><span class="sxs-lookup"><span data-stu-id="85179-108">The ID of the request to stop.</span></span>

</dd> </dl>

<span data-ttu-id="85179-109">L' **arrêt** peut également être utilisé pour arrêter les appels [**Prepare**](iagentcharacter--prepare.md) en attente.</span><span class="sxs-lookup"><span data-stu-id="85179-109">**Stop** can also be used to halt any queued [**Prepare**](iagentcharacter--prepare.md) calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="85179-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85179-110">See Also</span></span>

<span data-ttu-id="85179-111">[**IAgentCharacter ::P reparenthèse**](iagentcharacter--prepare.md), [ **IAgentCharacter :: stopAll**](iagentcharacter--stopall.md)</span><span class="sxs-lookup"><span data-stu-id="85179-111">[**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md)</span></span>


 

 




