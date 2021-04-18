---
title: IAgentCharacter Wait
description: IAgentCharacter Wait
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310746"
---
# <a name="iagentcharacterwait"></a><span data-ttu-id="e172d-103">IAgentCharacter :: wait</span><span class="sxs-lookup"><span data-stu-id="e172d-103">IAgentCharacter::Wait</span></span>

<span data-ttu-id="e172d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e172d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="e172d-105">Contient la file d’attente d’animation du caractère à l’animation (demande) spécifiée jusqu’à ce qu’une autre demande d’un autre caractère se termine.</span><span class="sxs-lookup"><span data-stu-id="e172d-105">Holds the character's animation queue at the specified animation (request) until another request for another character completes.</span></span>

-   <span data-ttu-id="e172d-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e172d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e172d-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="e172d-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="e172d-108">ID de la demande à attendre.</span><span class="sxs-lookup"><span data-stu-id="e172d-108">The ID of the request to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="e172d-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="e172d-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="e172d-110">Adresse d’une variable qui reçoit l’ID de demande d' **attente** .</span><span class="sxs-lookup"><span data-stu-id="e172d-110">Address of a variable that receives the **Wait** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="e172d-111">Utilisez cette méthode uniquement lorsque vous prenez en charge plusieurs caractères (simultanés) et que vous souhaitez séquencer leur interaction.</span><span class="sxs-lookup"><span data-stu-id="e172d-111">Use this method only when you support multiple (simultaneous) characters and want to sequence their interaction.</span></span> <span data-ttu-id="e172d-112">(Pour un caractère unique, chaque demande d’animation est lue de manière séquentielle, à l’issue de la requête précédente.) Si vous avez deux caractères et que vous souhaitez que la demande d’animation d’un caractère soit attendue jusqu’à la fin de l’animation de l’autre caractère, définissez la méthode d' **attente** sur l’ID de demande d’animation de l’autre caractère.</span><span class="sxs-lookup"><span data-stu-id="e172d-112">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and want one character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation request ID.</span></span>

 

 




