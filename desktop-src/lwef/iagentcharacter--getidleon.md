---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675929"
---
# <a name="iagentcharactergetidleon"></a><span data-ttu-id="424aa-103">IAgentCharacter::GetIdleOn</span><span class="sxs-lookup"><span data-stu-id="424aa-103">IAgentCharacter::GetIdleOn</span></span>

<span data-ttu-id="424aa-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="424aa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

<span data-ttu-id="424aa-105">Indique l’état de traitement automatique de l’inactivité d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="424aa-105">Indicates the automatic idle processing state for a character.</span></span>

-   <span data-ttu-id="424aa-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="424aa-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="424aa-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="424aa-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="424aa-108">Adresse d’une variable qui reçoit la **valeur true** si le serveur Microsoft Agent lit automatiquement les animations d’état de **ralenti** pour un caractère et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="424aa-108">Address of a variable that receives **True** if the Microsoft Agent server automatically plays **Idling** state animations for a character and **False** if not.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="424aa-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="424aa-109">See Also</span></span>

[<span data-ttu-id="424aa-110">**IAgentCharacter::SetIdleOn**</span><span class="sxs-lookup"><span data-stu-id="424aa-110">**IAgentCharacter::SetIdleOn**</span></span>](iagentcharacter--setidleon.md)


 

 




