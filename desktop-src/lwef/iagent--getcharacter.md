---
title: IAgent GetCharacter
description: IAgent GetCharacter
ms.assetid: c54e3aa3-49ea-475c-831c-03865438e1d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4653d15c4c0f7143fcc3087f7c5d9f0d3212b8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839870"
---
# <a name="iagentgetcharacter"></a><span data-ttu-id="83069-103">IAgent::GetCharacter</span><span class="sxs-lookup"><span data-stu-id="83069-103">IAgent::GetCharacter</span></span>

<span data-ttu-id="83069-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="83069-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCharacter(
   long dwCharID  // character ID
);
```

<span data-ttu-id="83069-105">Récupère le [**IAgentCharacter**](iagentcharacter.md) pour un caractère chargé.</span><span class="sxs-lookup"><span data-stu-id="83069-105">Retrieves the [**IAgentCharacter**](iagentcharacter.md) for a loaded character.</span></span>

-   <span data-ttu-id="83069-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="83069-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="83069-107"><span id="DwCharID_"></span><span id="dwcharid_"></span><span id="DWCHARID_"></span>*DwCharID*</span><span class="sxs-lookup"><span data-stu-id="83069-107"><span id="DwCharID_"></span><span id="dwcharid_"></span><span id="DWCHARID_"></span>*DwCharID*</span></span> 
</dt> <dd>

<span data-ttu-id="83069-108">ID du caractère.</span><span class="sxs-lookup"><span data-stu-id="83069-108">The character's ID.</span></span>

</dd> </dl>

 

 




